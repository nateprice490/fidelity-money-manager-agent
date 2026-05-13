# Engineering phases

## Phase 1: Cheapest MVP

Architecture:
- Azure Static Web Apps Free for React hosting
- Azure Functions API through Static Web Apps
- Supabase Free for Postgres and optional auth
- CSV import first, real brokerage provider later

Goal:
Build a working read-only portfolio dashboard with AI chat and sample/CSV data.

## Phase 2: Brokerage integration

Add a connector interface for:
- SnapTrade
- Akoya
- Plaid Investments

Start read-only only: balances, holdings, transactions.

## Phase 3: AI money manager agent

Add tool-style functions:
- getPortfolio
- analyzeRisk
- detectOverlap
- forecastRetirement
- explainNextInvestment

The agent should never execute trades in the MVP.

## Phase 4: Financial intelligence

Add:
- ETF overlap detection
- allocation drift
- retirement projections
- dividend forecasting
- Roth vs Traditional guidance
- tax-aware notes

## Phase 5: Alerts

Add notifications for:
- cash sitting idle
- portfolio drift
- large market drops
- contribution reminders
- dividend payments

## Phase 6: Production security

Add:
- OAuth login
- encrypted provider tokens
- audit logs
- read-only permission enforcement
- no Fidelity passwords stored

## Phase 7: Production deployment

Move to paid hosting only when needed:
- Azure App Service or Container Apps
- Supabase Pro or Azure PostgreSQL
- Key Vault
- monitoring and backups
