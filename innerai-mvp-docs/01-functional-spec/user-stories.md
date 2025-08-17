# User Stories (Backlog)

## Autenticação & Projetos
- Como Admin, quero criar um projeto para separar chaves e uso por equipe.
- Como Admin, quero emitir e revogar tokens do projeto.
- Como User, quero autenticar com token para chamar a API do hub.

## Provedores
- Como Admin, quero cadastrar credenciais OpenAI para `dev` e `prod`.
- Como Admin, quero testar a conectividade do provedor.
- Como Admin, quero definir modelos aprovados por projeto.

## Roteamento
- Como User, quero chamar `/v1/completions` escolhendo explicitamente `provider+model`.
- Como Admin, quero configurar uma lista de fallback.
- Como User, quero receber erro amigável quando todos provedores falharem, com `requestId`.

## Playground & Prompts
- Como User, quero testar um prompt e ver respostas lado a lado entre provedores.
- Como User, quero salvar um template e reutilizar com variáveis.
- Como User, quero exportar o histórico (CSV).

## Observabilidade
- Como Admin, quero ver métricas de latência p95 por provedor.
- Como Admin, quero buscar logs por `requestId` para debug.
- Como FinOps, quero extrair consumo (tokens) por período.

## Segurança
- Como Admin, quero revisar auditoria das alterações de credenciais.
- Como Admin, quero aplicar limites por projeto (RPM/TPM).
