CREATE OR REPLACE TRIGGER validacao_valor

BEFORE INSERT ON VENDAS

FOR EACH ROW

BEGIN

	IF :NEW.VALOR < 0 THEN

	RAISE_APPLICATION_ERROR(-20001, 'O valor da venda não pode ser negativo.') 
	
		END IF; 
		END;
		/