# Infrastructure

Deployment-only files; no application code.

- `postgres/init/`: creates the databases and roles on first start of the Postgres container
- `postgres/backup.sh`: encrypted nightly backup
- `keycloak/realm-sentrail.json`: realm imported by the Keycloak container
- `observability/`: Loki, Alloy and Grafana configuration (compose profile `observability`)

`docker-compose.yml` and `.env` stay at the repository root; services build from `backend/` and `frontend/`.
