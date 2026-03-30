# Especificação de Requisitos (SRS)

## 1. Requisitos Funcionais (RF)

| ID | Descrição |
|----|-----------|
| RF01 | O sistema deve permitir cadastro de usuários |
| RF02 | O sistema deve permitir login de usuários |
| RF03 | O sistema deve permitir cadastro de produtos |
| RF04 | O sistema deve exibir produtos disponíveis |
| RF05 | O sistema deve permitir adicionar produtos ao carrinho |
| RF06 | O sistema deve permitir finalizar compra |
| RF07 | O sistema deve processar pagamento via PIX |
| RF08 | O sistema deve processar pagamento via cartão |
| RF09 | O sistema deve calcular frete |
| RF10 | O sistema deve registrar pedidos |
| RF11 | O sistema deve atualizar estoque automaticamente |
| RF12 | O sistema deve permitir gerenciamento de pedidos |
| RF13 | O sistema deve armazenar histórico de compras |
| RF14 | O sistema deve permitir visualização de clientes |
| RF15 | O sistema deve integrar pixel de rastreamento |
| RF16 | O sistema deve exibir um dashboard administrativo com visão geral de vendas, estoque, pedidos e clientes |


---

## 3. Casos de Uso

### UC01 – Comprar Produto

**Ator:** Cliente

**Pré-condição:** Usuário autenticado, produto com estoque disponível

**Fluxo principal:**
1. Usuário acessa a listagem de produtos
2. Seleciona um produto e visualiza seus detalhes
3. Adiciona o produto ao carrinho
4. Acessa o carrinho e revisa os itens
5. Informa endereço de entrega e visualiza o frete calculado
6. Escolhe a forma de pagamento (PIX ou cartão parcelado)
7. Confirma o pedido
8. Sistema registra o pedido, debita o estoque e envia confirmação

**Fluxos alternativos:**
- Produto sem estoque → sistema exibe aviso e impede a compra
- Pagamento falha → sistema notifica o usuário e permite nova tentativa
- Usuário remove item do carrinho → carrinho é atualizado

---

### UC02 – Cadastrar e Gerenciar Produtos

**Ator:** Admin

**Pré-condição:** Admin autenticado no painel

**Fluxo principal:**
1. Admin acessa a seção de produtos no painel
2. Cria novo produto informando nome, descrição, imagens, preço de venda, preço de custo e quantidade em estoque
3. Define se o produto é um drop (data de liberação)
4. Publica o produto, tornando-o visível na loja

**Fluxos alternativos:**
- Editar produto → admin altera campos e salva
- Remover produto → sistema solicita confirmação e remove da listagem
- Produto esgotado → sistema marca automaticamente como indisponível

---

### UC03 – Gerenciar Pedidos

**Ator:** Admin

**Pré-condição:** Admin autenticado no painel

**Fluxo principal:**
1. Admin acessa a listagem de pedidos
2. Filtra pedidos por status (aguardando pagamento, pago, em separação, enviado, entregue)
3. Seleciona um pedido e visualiza seus detalhes (itens, cliente, pagamento, endereço)
4. Atualiza o status do pedido conforme andamento
5. Registra código de rastreamento quando o pedido é enviado

**Fluxo alternativo:**
- Pedido com pagamento não confirmado → admin pode cancelar o pedido manualmente

---

### UC04 – Cadastrar-se e Fazer Login

**Ator:** Usuário (cliente)

**Fluxo principal (cadastro):**
1. Usuário acessa a página de cadastro
2. Informa nome, e-mail e senha
3. Sistema valida os dados e cria a conta
4. Usuário é redirecionado para a home autenticado

**Fluxo principal (login):**
1. Usuário acessa a página de login
2. Informa e-mail e senha
3. Sistema autentica e redireciona para a home

**Fluxos alternativos:**
- E-mail já cadastrado no cadastro → sistema exibe aviso
- Credenciais inválidas no login → sistema exibe mensagem de erro
- Esqueceu a senha → usuário solicita redefinição por e-mail

---

### UC05 – Visualizar Dashboard Administrativo

**Ator:** Admin

**Pré-condição:** Admin autenticado no painel

**Fluxo principal:**
1. Admin acessa o painel e visualiza o dashboard
2. Dashboard exibe resumo de vendas do período (total, ticket médio)
3. Dashboard exibe alertas de produtos com estoque baixo
4. Dashboard exibe pedidos recentes e seus status
5. Dashboard exibe número de clientes cadastrados e novos no período

**Fluxo alternativo:**
- Sem dados no período → dashboard exibe estado vazio com orientações

---

### UC06 – Acompanhar Pedido

**Ator:** Cliente

**Pré-condição:** Usuário autenticado com pedido realizado

**Fluxo principal:**
1. Usuário acessa "Meus Pedidos"
2. Visualiza a lista de pedidos com status atual
3. Seleciona um pedido para ver detalhes
4. Visualiza itens, valor, forma de pagamento e status de entrega
5. Acessa o código de rastreamento quando disponível

---

### UC07 – Gerenciar Clientes (CRM)

**Ator:** Admin

**Pré-condição:** Admin autenticado no painel

**Fluxo principal:**
1. Admin acessa a seção de clientes
2. Visualiza a lista de clientes cadastrados com dados básicos
3. Seleciona um cliente e visualiza seu histórico de compras
4. Analisa métricas do cliente (frequência, valor total gasto, última compra)

**Fluxo alternativo:**
- Admin filtra clientes por frequência ou data de cadastro

---

## 4. Regras de Negócio

| ID | Regra |
|----|-------|
| RN01 | Produtos são vendidos por drops limitados |
| RN02 | Produto esgotado não pode ser comprado |
| RN03 | Frete é cobrado separadamente |
| RN04 | Estoque é atualizado automaticamente após compra |
| RN05 | Pedidos devem ser registrados com status |
| RN06 | Pagamento deve ser confirmado para validar pedido |
| RN07 | (Futuro) Produtos exclusivos para membros |
| RN08 | (Futuro) Comissão por indicação (afiliados) |

---

## 5. Modelo de Dados (simplificado)

```
Usuário         Produto         Pedido
--------        -------         ------
id              id              id
nome            nome            usuário_id
email           descrição       status
senha           preço           valor_total
                estoque

ItemPedido      Pagamento
----------      ---------
id              id
pedido_id       pedido_id
produto_id      tipo (PIX/cartão)
quantidade      status
```
