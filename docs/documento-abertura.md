# Documento de Abertura do Projeto

**Projeto:** Plataforma Shio (E-commerce + Comunidade)
**Data:** 23/03/2026
**Link da primeira reunião:** Reunião de Kick-off - Shio - 2026/03/23 20:47 GMT-03:00

---

## 1. Objetivo do Projeto

Desenvolver uma plataforma digital para a marca Shio que integre:

* E-commerce próprio (substituindo a Nuvemshop)
* Estrutura de comunidade (Club)
* Base de dados de clientes (CRM)

O objetivo é permitir escala do negócio, aumento de vendas e construção de uma comunidade engajada no nicho gospel.

---

## 2. Problema Identificado

* Plataforma atual com taxas altas
* Nenhuma venda relevante no e-commerce
* Falta de:
  * Controle de estoque
  * Gestão de clientes
  * Dados de comportamento
* Operação muito manual
* Dificuldade em escalar com tráfego pago

---

## 3. Stakeholders

* **Cliente:** Douglas (Shio)
* **Equipe do projeto:** Alunos TPPE
* **Design:** Guilherme
* **Parceiros externos:**
  * Empresa de logística
  * Produtora (private label)

---

## 4. Visão do Produto

A Shio deixará de ser apenas uma loja e passará a ser um ecossistema digital com e-commerce + comunidade + conteúdo, incluindo:

* Venda de roupas (drops exclusivos)
* Lançamento de livros e devocionais
* Clube de membros com benefícios
* Parcerias com influenciadores e embaixadores

---

## 5. Escopo do MVP (0–3 meses)

### E-commerce

* Cadastro e gestão de produtos (drops)
* Compra online
* Pagamentos:
  * Cartão (parcelado)
  * PIX
* Cálculo de frete (ou integração futura)

### Gestão interna

* Controle de estoque (preço de custo e venda)
* Painel administrativo (preferencialmente mobile)

### CRM e dados

* Cadastro de usuários
* Histórico de compra
* Análise de comportamento (frequência, retenção)
* Integração com pixel (tracking)

---

## 6. Funcionalidades Futuras (fora do MVP)

* Clube de assinatura (membership)
* Conteúdos exclusivos
* Sistema de afiliados/embaixadores (com comissão)
* Produtos exclusivos para membros
* Eventos e integração com comunidade
* Gamificação / fidelização

---

## 7. Integrações

* API da empresa de logística (a validar)
* Gateways de pagamento
* Pixel de marketing (Meta/Google)
* Possível integração com Correios

---

## 8. Restrições

* Prazo inicial: até 3 meses (MVP)
* Dependência de: API logística, definição de frete, Design (Guilherme)
* Orçamento a ser definido
* Necessidade de escalar posteriormente

---

## 9. Público-alvo

* Jovens de 16 a 28 anos
* Nicho cristão/gospel
* Consumidores de streetwear com propósito

---

## 10. Critérios de Sucesso

* Primeiras vendas via plataforma própria
* Base de clientes estruturada (CRM)
* Capacidade de rodar tráfego pago
* Controle interno operacional
* Engajamento inicial da comunidade

---

## 11. Próximos Passos

* Levantamento detalhado de requisitos
* Definição do escopo final do MVP
* Levantamento de custos
* Definição de arquitetura
* Alinhamento com design
* Validação com cliente

---

## 12. Observações Importantes

* O projeto deve priorizar validação rápida (micro → macro)
* Foco em dados e comunidade, não só vendas
* Estratégia baseada em: Exclusividade (drops), Escassez, Engajamento

---

## Protótipo (estrutura de telas)

(A definir)

---

## Primeira proposta de cronograma (3 meses)

### Mês 1 — Base do sistema

| Semana | Atividade |
|--------|-----------|
| 1 | Levantamento final de requisitos / Definição de arquitetura |
| 2 | Modelagem de banco / Setup backend + frontend |
| 3 | Cadastro/login / Estrutura de produtos |
| 4 | Listagem de produtos / Página de produto |

### Mês 2 — Core de vendas

| Semana | Atividade |
|--------|-----------|
| 5 | Carrinho |
| 6 | Checkout |
| 7 | Integração PIX e cartão |
| 8 | Criação de pedidos / Controle de estoque |

### Mês 3 — Gestão + ajustes

| Semana | Atividade |
|--------|-----------|
| 9 | Painel admin (produtos) |
| 10 | Painel admin (pedidos/clientes) |
| 11 | Frete / Pixel tracking |
| 12 | Testes / Correções / Deploy |

---

## Entregáveis Finais

* Sistema funcionando (MVP)
* Documentação (SRS + modelo + casos de uso)
* Base de dados estruturada
* Pronto para escalar

---

## Checklist para Iniciar o Desenvolvimento

### 1. Alinhamento de negócio
- [x] Problema validado com cliente
- [x] Escopo do MVP definido
- [x] Backlog priorizado
- [x] Requisitos funcionais documentados
- [x] Regras de negócio claras
- [x] Stakeholders alinhados

### 2. Validação
- [ ] Protótipo aprovado pelo cliente
- [ ] Fluxos principais validados (compra, cadastro, admin)
- [ ] Expectativa de entrega alinhada

### 3. Viabilidade
- [ ] Análise de custo aprovada
- [ ] Cronograma aprovado
- [ ] Recursos disponíveis (time, tempo)

### 4. Arquitetura
- [ ] Arquitetura definida (monolito, microserviços, etc.)
- [ ] Stack definida (linguagem, framework, banco)
- [ ] Modelagem de dados pronta
- [ ] Definição de APIs
- [ ] Estratégia de autenticação definida
- [ ] Estratégia de integração (pagamento, frete, etc.)

### 5. Infraestrutura
- [ ] Ambiente de desenvolvimento configurado
- [ ] Repositório criado (Git)
- [ ] Padrão de branches definido
- [ ] Ambiente de homologação definido
- [ ] Ambiente de produção definido
- [ ] Banco de dados provisionado
- [ ] Serviço de hospedagem escolhido (cloud)

### 6. Segurança e acesso
- [ ] Controle de acesso definido (admin vs usuário)
- [ ] Uso de HTTPS definido
- [ ] Gestão de variáveis sensíveis (env)
- [ ] Backup inicial planejado

### 7. Deploy
- [ ] Estratégia de deploy definida (manual / CI/CD)
- [ ] Pipeline de deploy configurado
- [ ] Versionamento definido
- [ ] Plano de rollback definido

### 8. Qualidade
- [ ] Estratégia de testes definida
- [ ] Critérios de aceitação definidos
- [ ] Ambiente de testes preparado

### 9. Monitoramento
- [ ] Logs configurados
- [ ] Monitoramento básico definido
- [ ] Métricas de sucesso definidas
