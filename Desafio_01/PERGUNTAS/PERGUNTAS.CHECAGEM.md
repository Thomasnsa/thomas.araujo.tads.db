PERGUNTAS DE CHECAGEM

1) Quais controles do A-0 impedem abuso de cupons?
- Politica de desconto.

2) Onde está a fronteira entre `CouponService` e `OrderService`?
- "CouponService" cria o cupom e manipula o mesmo, já o "OrderService" cria o pedido e segue os passos até sua finalização. O primeiro tem o limite de manipular só o cupom, enquanto o outro pode utilizar o cupom, mas não manipula, por conseguinte pode seguir os passos até finalizar a venda.

3) Que índices no DER suportam as consultas críticas?
- PK, FK, WHERE (para selecionar quais serão os dados de consulta e filtro), não usar "*" e por fim pode ser usado o INDEX.

4) O que quebra se remover o cache de cupons?
- Ele pode demorar mais para consultar, e se tirar o cache pode até mesmo não salvar dados de login.

5) Que dado pessoal precisa de minimização conforme LGPD?
- Só o essencial, se é para venda e cupom, o ideal seria nome, CPF e e-mail.