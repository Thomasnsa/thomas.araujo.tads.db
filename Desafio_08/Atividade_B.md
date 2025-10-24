SELECT 
    NVL(c.nome, 'Sem Cliente') AS cliente,
    v.produto,
    v.valor
FROM CLIENTES c
RIGHT JOIN VENDAS v
ON c.id_cliente = v.id_cliente;