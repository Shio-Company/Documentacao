# Ata de Reunião — Projeto E-commerce SHIO

**Data:** 11/05/2026  
**Participantes:** Equipe de desenvolvimento + cliente  
**Objetivo:** Validação do protótipo de alta fidelidade e alinhamento técnico/comercial do MVP da plataforma.
**Link:** (https://drive.google.com/file/d/1xrmmFLlzcEyGvifZvgkfVOnvKuRn9-zI/view?usp=drive_link)[https://drive.google.com/file/d/1xrmmFLlzcEyGvifZvgkfVOnvKuRn9-zI/view?usp=drive_link]

---

# 1. Contexto da Reunião

A reunião teve como foco:

- apresentação do ambiente do projeto;
- demonstração do protótipo navegável web e mobile;
- validação funcional do MVP;
- alinhamento sobre integrações de pagamento;
- definição de próximos passos.

Foi informado ao cliente que:

- o cronograma segue em dia;
- o projeto está estruturado em ambiente privado no GitHub;
- existem repositórios separados para:
  - frontend;
  - backend;
  - documentação.

Também foi apresentada a documentação inicial contendo:

- visão de produto;
- escopo do MVP;
- requisitos;
- casos de uso;
- guia de estilo;
- documentação de abertura do projeto.

---

# 2. Escopo Validado do MVP

## Funcionalidades principais aprovadas

### E-commerce

- catálogo de produtos;
- visualização de produtos;
- sistema de drops;
- carrinho de compras;
- checkout;
- aplicação de cupons;
- cálculo de frete;
- pagamento via PIX e cartão;
- confirmação de pedido;
- rastreamento de pedidos;
- histórico de pedidos.

### Área do usuário

- cadastro/login;
- gerenciamento de dados pessoais;
- gerenciamento de endereços;
- visualização de pedidos;
- acompanhamento de status.

### Painel administrativo

- dashboard com indicadores;
- gestão de drops;
- gestão de produtos;
- gestão de pedidos;
- gestão de clientes;
- controle de estoque;
- status de publicação;
- duplicação de drops;
- relatórios básicos e métricas.

### Mobile

Foi validada também a versão responsiva/mobile:

- mesma estrutura funcional do web;
- dashboard adaptado;
- gerenciamento administrativo mobile;
- navegação responsiva.

---

# 3. Funcionalidades Fora do Escopo Inicial

As seguintes funcionalidades foram consideradas mais complexas para a primeira entrega e ficaram para evolução futura:

- clube de assinaturas;
- conteúdos exclusivos;
- funcionalidades avançadas de comunidade;
- integrações mais profundas com marketing;
- automações adicionais.

---

# 4. Integrações Externas

## Pagamentos

O cliente informou que está avaliando:

- Hypercash;
- InfinitePay.

A tendência inicial é utilização da Hypercash.

### Pendências técnicas

Validar com o provedor:

- disponibilidade de APIs;
- consulta de status de pagamento;
- rastreamento de pedidos;
- suporte a estorno;
- tipos de pagamento;
- política de cancelamento;
- webhook/eventos.

### Estratégia inicial definida

Inicialmente poderá ser utilizado:

- redirecionamento para páginas externas do gateway/logística;
- integração completa posteriormente.

---

# 5. Decisões Técnicas

## Autenticação

Foi aprovada autenticação social:

- Google Login inicialmente;
- Apple Login posteriormente.

### Objetivo

- reduzir fricção no checkout;
- facilitar cadastro/login.

---

# 6. Feedback do Cliente

O cliente:

- aprovou o protótipo;
- validou o fluxo apresentado;
- demonstrou satisfação com:
  - organização;
  - detalhamento;
  - experiência visual;
  - funcionalidades;
  - dashboard administrativo.

Não foram solicitadas alterações críticas no fluxo atual.

---

# 7. Próximos Passos

## Equipe de desenvolvimento

- continuar implementação do MVP;
- priorizar funcionalidades essenciais;
- levantar custos técnicos/plataformas;
- enviar protótipo ao cliente;
- alinhar APIs com gateway de pagamento;
- iniciar construção funcional do sistema.

## Cliente

- conectar equipe com fornecedor de pagamentos;
- adicionar responsáveis financeiros e operacionais no grupo;
- validar custos futuros;
- acompanhar próximas entregas.

---

# 8. Novos Participantes no Fluxo

Serão adicionadas ao grupo:

- Amanda → financeiro;
- Lavine → prazos e campanhas/drops.

### Objetivo

- agilizar decisões;
- reduzir ruído de comunicação;
- facilitar validações.

---

# Resumo Executivo

O projeto do e-commerce SHIO avançou para a fase de validação do protótipo de alta fidelidade, contemplando versões web e mobile. A solução apresentada inclui funcionalidades centrais de e-commerce, gerenciamento administrativo, controle de drops, pedidos, produtos e clientes.

O cliente aprovou integralmente o fluxo apresentado e destacou positivamente:

- qualidade visual;
- organização do projeto;
- experiência do usuário;
- funcionalidades administrativas.

A arquitetura do projeto já está estruturada em ambiente GitHub privado, com separação entre frontend, backend e documentação, garantindo rastreabilidade e continuidade do desenvolvimento.

Foi definido que o MVP terá foco nas funcionalidades essenciais para operação do negócio, enquanto recursos mais avançados, como clube de assinatura e conteúdos exclusivos, serão tratados em versões futuras.

Na parte técnica, ficou encaminhada a integração com gateway de pagamento externo, provavelmente Hypercash, inicialmente via redirecionamento e posteriormente com integração mais profunda via API.

Também foi aprovada a estratégia de autenticação social com Google Login, visando reduzir fricção no processo de compra.

## Próximos passos

- avanço da implementação;
- alinhamento técnico com fornecedores de pagamento;
- levantamento de custos;
- validação contínua com o cliente e equipe operacional.