Crie uma procedure chamada total_vendas_vendedor que recebe o nome do vendedor e
 retorna o total de vendas realizadas por ele.
 
 CREATE OR REPLACE PROCEDURE total_vendas_vendedor
 (
	p_vendedor IN VARCHAR2,
	p_total_vendas OUT NUMBER
 )
 IS
 BEGIN
	SELECT COUNT(*) INTO p_total_vendas from LOG_VENDAS WHERE vendedor = p_vendedor;


DBMS_OUTPUT.PUT_LINE('Vendedor ' || p_vendedor || ' realizou ' || p_total_vendas || ' vendas.');

end total_Vendas_vendedor;
/