# sportshop-deploy

Cross-repo prod orchestration for the Sportshop monorepo (frontend + backend + swagger).

`docker-compose.yml` is the entry point — its header comment block has the full
build / run / teardown / TLS-trust instructions. Per-repo artifacts (the backend
Spring Boot image, the frontend `sportshop-web` image + its `Caddyfile`, `.env*`)
live inside each repo; only DB credentials (`.env.prod.db`) live here.
