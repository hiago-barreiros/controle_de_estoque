## Regras de negócio

### Armazenamento de senha

As senha deverão ser salva no banco de dados utilizando o Algoritmo Argon2ID com a tecnica PEPPER

### Usuários

- Administrador: Acessor total a aplicação.
- Vendedor: Acesso apenas a aplicação de vendas
    - Registra
    - Cancelamento
    - Devolução

### Estoque

- **Registro**: Toda mercadoria que entra ou sai deve ser registrada. Como venda, compra e devolução.
- **Gestão por nível de Estoque**: Definir quantidades minimas (ponto de pedido) para repor e máximas para estoque muito cheio. 
-  Produtos diferentes não podem ter o mesmo **SKU** (Código de barras/identificador).
- Não é permitido cadastrar o mesmo produto mais de uma vez.
- Produtos com **SKU** tem que haver uma relação entre a **data de validade** e a **quantidade em estoque**.
- **Saldo do estoque**: Representa o valor total(R$) da soma das mercadorias.

### Loja

- Toda venda feita, a quantidade em estoque deve ser atualizada, assim como produtos devolvidos, juntamento com o saldo representado no **estoque**
    - Os items de para venda devem ser registrados no painel, para apuração: valor, quantidade e total.
    - Antes de finalizar a apuração é possível cancelar todo o processo ou os items um por um
    - Cada venda finalizada deve ser gerado um **cupom de venda** 
- A venda só pode acontecer de acordo com a quantidade em estoque
- Devoluções só pode acontecer referente a numeração do cupom de venda
