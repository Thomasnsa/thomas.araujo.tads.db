SELECT
    c.nome,
    c.cidade
FROM CLIENTES c
LEFT JOIN VENDAS v
    ON c.id_cliente = v.id_cliente
WHERE v.id IS NULL;