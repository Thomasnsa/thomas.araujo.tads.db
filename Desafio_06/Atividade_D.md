SELECT *
FROM (
    SELECT
        vendedor,
        produto,
        valor,
        ROW_NUMBER() OVER (PARTITION BY vendedor ORDER BY valor DESC) AS ranking
    FROM VENDAS
) t
WHERE ranking <= 3;