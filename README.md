# Controle de Estoque

Aplicação para gerenciar produtos e registrar movimentações de entrada e saída (CRUD).

### Entidades:
1. Produto (id, nome, sku, categoria, preco, estoque_minimo)
2. Lote (id, produto_id, quantidade, data_validade, data_entrada)
3. Movimentacao (id, produto_id, tipo, quantidade, data, observacao)

### Funcionalidades:
- CRUD de produtos
- Cadastro de lotes (entrada de mercadoria)
- Registro de movimentações (entrada/saída)
- Endpoint "estoque crítico" (produtos abaixo do mínimo)
- Listagem de produtos próximos ao vencimento
- Dashboard simples (total em estoque, produtos críticos)



