MER

Entidades:
Cupom (id PK, descricao, codigo, valor, ativo e data_validade)
Cliente (id PK, nome, CPF, data_nascimento e endereco)
Produto (Id PK, descricao, valor, Tipo_Produto FK e Estoque Fk)
Estoque (id PK, Produto FK e qtd)
Pedido (id PK, Cliente FK, Cupom FK valor_total e data_hora)
Item_Pedido (id PK, pedido FK, produto FK, qtd e valor_unitario)
Tipo_Produto (ID PK e descricao)
Login_Vendedor (id PK, usuario, email e senha)
Log (Id PK, operação, data_hora, descricao e Login_Vendedor FK)

Relacionamentos: 
Cupom 1:1 Pedido
Produto N:1 Tipo_Produto
Produto 1:1 Estoque
Pedido N:1 Cliente
Item_Pedido N:1 pedido
Item_Pedido N:1 produto
Log N:1 Login_Vendedor
