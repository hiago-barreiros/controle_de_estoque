# Conceitos do Projeto

O sistema se baseia em um CRUD que permitirá gerenciar produtos e registrar movimentações de entrada e saída. 
- Create: Cadastrar produto (Nome, SKU, Preço, Quantidade, Validade)
- Read: Listar o estoque
- Update: Editar informações do produto ou ajustar manualmente a quantidade.
- Delete: Remover produtos do catálogo

## Implementações

- Lógica de "Estoque Critico": Cria um ENDPOINT que retorne os produtos onde a quantidade < estoque.
- Validação de SKU: Não pode existir produtos com o mesmo SKU.
- Histórico de movimentação: adiciona uma tela secundária apenas para registrar "Entrada" ou "Saida" toda vez que a quantidade for alterada. 