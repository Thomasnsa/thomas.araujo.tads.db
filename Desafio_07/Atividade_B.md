SELECT
    c.ESTADO,
    SUM(v.valor) AS total_vendas
FROM VENDAS v
INNER JOIN CLIENTES c
    ON v.id_cliente = c.id_cliente
GROUP BY c.ESTADO;