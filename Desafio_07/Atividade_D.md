SELECT
    c.nome AS cliente,
    v.categoria,
    SUM(v.valor) AS total_categoria
FROM VENDAS v
INNER JOIN CLIENTES c
    ON v.id_cliente = c.id_cliente
GROUP BY c.nome, v.categoria
HAVING SUM(v.valor) = (
    SELECT MAX(SUM(v2.valor))
    FROM VENDAS v2
    WHERE v2.id_cliente = c.id_cliente
    GROUP BY v2.categoria
);

