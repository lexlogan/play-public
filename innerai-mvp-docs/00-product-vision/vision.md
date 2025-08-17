# Visão de Produto

Construir uma **plataforma agregadora de IA (LLM Hub)** que centraliza chaves, versões e políticas de uso de provedores
(OpenAI, Anthropic, Google, Azure OpenAI etc.), oferecendo um **ponto único** de administração, roteamento e auditoria.
Foco inicial: **desenvolvedores** e **equipes de plataforma** que precisam padronizar acesso a LLMs com **controle de custos,
observabilidade e segurança**.

## Objetivos principais
- **Unificar acesso** a múltiplos LLMs via API própria.
- **Gerenciar segredos** e credenciais por ambiente/projeto.
- **Roteamento explícito** (modelo fixo) e **fallback** simples no MVP.
- **Playground web** para testar prompts e comparar respostas entre provedores.
- **Observabilidade e custos**: métricas básicas de uso por projeto/chave.
- **Segurança**: RBAC simples (Admin e User), escopos por projeto.

## Indicadores de sucesso (MVP)
- Integração com pelo menos **3 provedores**.
- Latência p95 e taxa de erro por provedor visíveis no dashboard.
- Criação e rotação de chaves do produto e chaves de provedores por projeto.
- 80%+ das requisições passando pelo proxy/roteador interno.
