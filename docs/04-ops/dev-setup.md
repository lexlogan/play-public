# Ambiente de Desenvolvimento (Docker)

1. Crie `.env` a partir de `.env.example`.
2. Suba os serviços:
   ```bash
   docker compose up -d
   ```
3. Acesse:
   - Postgres: `localhost:5432` (innerai/innerai)
   - Redis: `localhost:6379`
   - MinIO: `http://localhost:9001` (console; admin/adminadmin)
4. Crie o bucket `${MINIO_BUCKET}` caso não seja criado automaticamente.
