# Fidelity Money Manager Agent

A read-only AI money manager starter app for Fidelity-style brokerage data.

## What it does

- React portfolio dashboard
- Spring Boot backend
- PostgreSQL-ready config
- Brokerage connector abstraction
- Fidelity CSV fallback connector
- AI money manager chat endpoint
- Portfolio allocation and risk analysis
- Docker Compose for local development

## Important safety rule

This project does **not** store Fidelity passwords and does **not** place trades. Start read-only. Use OAuth or aggregator tokens only.

## Fidelity integration strategy

Fidelity generally requires a permissioned aggregator such as Akoya, Plaid, SnapTrade, Finicity, or MX. This project keeps the broker layer behind `BrokerageConnector` so you can plug in the real provider later without rewriting the agent.

## Quick start

```bash
cp .env.example .env
docker compose up --build
```

Frontend: http://localhost:5173
Backend: http://localhost:8080

## Backend env

```bash
OPENAI_API_KEY=your_key
OPENAI_MODEL=gpt-4.1-mini
BROKER_PROVIDER=csv
DATABASE_URL=jdbc:postgresql://postgres:5432/money_manager
DATABASE_USERNAME=postgres
DATABASE_PASSWORD=postgres
```

## Roadmap

1. Add real provider connector: SnapTrade, Akoya, or Plaid.
2. Add secure auth and encrypted token storage.
3. Add ETF overlap analysis.
4. Add retirement projections.
5. Add dividend and contribution forecasting.
6. Add alerting for allocation drift and large market moves.
