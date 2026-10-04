# Audex Environment Variables Matrix

| Variable Name | Development (`dev`) | Testing (`test`) | Staging (`staging`) | Sensitivity / Type |
| :--- | :--- | :--- | :--- | :--- |
| `NODE_ENV` | `development` | `test` | `staging` | Plaintext Config |
| `PORT` | `3000` | `3001` | `3000` | Plaintext Config |
| `AUDEX_ACTIVE_MODE` | `compass` | `compass` | `perfect` | Architecture Rule |
| `DATABASE_URL` | `postgresql://dev_user:pass@localhost:5432/audex_dev` | `postgresql://test_user:pass@localhost:5432/audex_test` | `env:STAGING_DB_URL` | High Secret |
| `REDIS_URL` | `redis://localhost:6379/0` | `redis://localhost:6379/1` | `redis://redis-stg:6379/0` | Internal Secret |
| `LLM_API_BASE_URL` | `http://localhost:11434` | `http://mock-llm:11434` | `https://llm.staging.audex.internal` | Internal Endpoint |
| `LLM_API_KEY` | `dev-dummy-key` | `test-dummy-key` | `env:AUDEX_STG_LLM_KEY` | High Secret |
| `VECTOR_DB_URL` | `http://localhost:6333` | `http://localhost:6333` | `http://qdrant-stg:6333` | Internal Endpoint |
| `JWT_SECRET` | `dev-jwt-secret-123` | `test-jwt-secret-456` | `env:AUDEX_STG_JWT_SECRET` | Critical Secret |
| `MASK_PII_DATA` | `true` | `true` | `true` | Privacy Rule |