# Nexus Intelligence

A full-stack starter application for data analytics, business reporting, market trend visualization and defensive cybersecurity intelligence.

## Features
- Responsive landing/login/register experience.
- JWT authentication, bcrypt password hashing and SQLite persistence.
- Overview dashboard and interactive Recharts visualizations.
- CSV import, preview, numeric-field detection, basic data-quality checks and CSV export.
- Sales analytics with clearly labelled illustrative sample data.
- Market Watch with illustrative sample prices (not live market data).
- Defensive log keyword review and incident-response checklist.
- Passive domain intelligence: public DNS records and RDAP registration metadata.
- Save reports to SQLite, browser print-to-PDF and in-app assistant demo.

## Requirements
- Node.js 18.18+ (Node 20 LTS recommended)
- npm

## Run locally
```bash
cp .env.example .env
# Change JWT_SECRET in .env before using beyond local development
npm install
npm run dev
```
Frontend: http://localhost:5173  
Backend: http://localhost:5000/api/health

Register a new account from the app. SQLite database is created automatically at `server/nexus.db`.

## Build frontend
```bash
npm run build
```

## Important configuration
Set a strong random `JWT_SECRET` and appropriate `CLIENT_ORIGIN` in `.env`. For production, serve the frontend and API over HTTPS, configure a production database and backups, add email verification/password reset, audit logging, monitoring, CSRF strategy appropriate to the auth design, and a proper secrets manager. Do not use the development fallback JWT secret in production.

## Data and security limitations
- Sales and market charts use sample data until you import/connect real sources.
- Market Watch is not a live exchange feed and does not provide investment advice.
- Threat Center uses transparent keyword rules against text supplied by the user. It is not an endpoint detection product, malware sandbox, SIEM, vulnerability scanner or forensic investigation.
- Domain Intel makes passive DNS and RDAP lookups only. WHOIS-style data availability varies by registry. It does not scan ports, exploit systems or certify a domain as safe.
- The chat assistant is a local demonstration response engine, not a connected LLM. Add an authenticated AI provider server-side if needed; never expose API keys in frontend code.
- Reports are saved in the local SQLite database. Browser Print can save the report page as PDF.

## Suggested next integrations
Connect a market-data provider, an AI provider through a server-side endpoint, a real SIEM/EDR source, and a business database after reviewing licensing, privacy and security requirements.
"# Market--intelligence" 
