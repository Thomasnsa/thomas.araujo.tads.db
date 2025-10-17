SELECT
    c.CIDADE,
    SUM(v.valor) AS total_vendas
FROM VENDAS v
INNER JOIN CLIENTES c
    ON v.id_cliente = c.id_cliente  
GROUP BY c.CIDADE
HAVING SUM(V.VALOR) > 2000;