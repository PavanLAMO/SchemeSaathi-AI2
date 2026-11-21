# SchemeSaathi AI (योजना साथी)

Voice-first, multilingual discovery and eligibility exploration for Indian government welfare schemes.

## Project structure

```text
SchemeSaathi-AI/
├── index.html                 # Main standalone web application
├── api/
│   └── index.js               # Vercel serverless API entrypoint
├── backend/
│   ├── server.js              # Native Node.js HTTP API server
│   ├── services/
│   │   └── dataGovService.js  # data.gov.in integration and dataset registry
│   ├── test-api.js            # Backend API/eligibility tests
│   └── test-datagov.js        # data.gov.in service tests
├── public/
│   └── js/                    # Frontend feature modules
├── .env.example               # Safe environment-variable template
├── .gitignore
├── package.json
└── vercel.json
```

## Features

- Citizen profile and scheme discovery flow.
- Multilingual voice interaction and spoken scheme explanations.
- Scheme eligibility matching and scheme information views.
- Ongoing/expired scheme filtering and reopening notification subscriptions.
- data.gov.in dataset integration through the backend service.

## Requirements

- Node.js 18 or later
- A modern browser
- A data.gov.in API key for live dataset requests (where required)

## Run locally

1. Install dependencies:

   ```bash
   npm install
   ```

2. Create your local environment file:

   ```bash
   cp .env.example .env
   ```

   Add your own `DATA_GOV_IN_API_KEY` to `.env`. Never commit or share this file.

3. Start the backend:

   ```bash
   npm start
   ```

   The API listens on `http://localhost:5000` by default.

4. Open `index.html` in a browser for the frontend. If browser restrictions affect local file access, serve the project directory with:

   ```bash
   npx http-server .
   ```

## Development

```bash
npm run dev
```

## Tests

```bash
npm test
```

## Deployment

The repository includes `api/index.js` and `vercel.json` for Vercel API routing. Configure `DATA_GOV_IN_API_KEY` and any required environment variables in the deployment platform's environment settings.

## Security notes

- `.env` is intentionally excluded from this cleaned project.
- `.env.example` contains placeholders only. Supply your own API key locally.
- Do not publish API keys, access tokens, or other credentials.

## License

MIT (as stated in the original project metadata).
