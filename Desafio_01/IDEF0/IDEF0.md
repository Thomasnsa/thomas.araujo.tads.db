IDEF0

A-0
Para ver o IDEF0 A-0, segue a imagem em anexo na pasta "IDEF0_GERENCIAR_VENDAS_CUPOM.png".

A0
  A1[[A1: Definir regras de cupom]]
  A2[[A2: Publicar/gerar cupons]]
  A3[[A3: Validar e aplicar cupom]]
  A4[[A4: Auditar e reportar]]

  A1 -->|Regras aprovadas| A2
  A2 -->|Cupons ativos| A3
  A3 -->|Logs de aplicação| A4

  A2 --> OUT1[Cupons publicados]
  A3 --> OUT2[Pedido com desconto]
  A4 --> OUT3[Relatórios]