# Stockroom React App

React client for the Stockroom product API.

## Local development

1. Start the API and make sure its CORS configuration allows the frontend origin.
2. Copy `.env.example` to `.env` and set `VITE_API_BASE_URL` to the API origin. The example uses `http://127.0.0.1:3000` for local development.
3. Run `npm ci` and `npm run dev` from this repository root.

The client stores short-lived access and refresh tokens in `sessionStorage`; it never connects to MySQL directly.

## Render Static Site

- Root directory: leave blank
- Build command: `npm ci && npm run build`
- Publish directory: `dist`
- Environment variable: `VITE_API_BASE_URL` set to the deployed API origin

On the API service, set `API_ALLOW_ORIGIN` to the exact Static Site origin. Do not add `.env` files or API credentials to this repository.