# Azure deployment plan

Use Azure Static Web Apps Free for the React frontend and serverless API.

Build settings:

- App location: frontend
- Api location: api
- Output location: dist

Required app settings:

- OPENAI_API_KEY
- OPENAI_MODEL
- SUPABASE_URL
- SUPABASE_SERVICE_ROLE_KEY
- BROKER_PROVIDER

Recommended starting provider: sample or csv.

Deployment steps:

1. Create Azure Static Web App.
2. Connect GitHub repo nateprice490/fidelity-money-manager-agent.
3. Use the build settings above.
4. Add app settings in Azure Portal.
5. Push code to main.

Cost-control rule: keep brokerage integration disabled until the sample dashboard and AI endpoint are live.
