# Segurança

- **Segredos**: no MVP, `.env` local e `key_ref` armazenando referência; em produção, **AWS Secrets Manager/KMS**.
- **Tokens de projeto**: formato Bearer, hash no banco (BCrypt/Argon2).
- **RBAC**: Admin/User por projeto.
- **Auditoria**: mudanças de credenciais, emissão/revogação de tokens, exportações.
- **Rate limiting** e **circuit breaker** por provedor/projeto.
