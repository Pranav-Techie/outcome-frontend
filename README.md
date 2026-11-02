# OUTCOME V2 — Conditional Payments

**Don't pay for promises. Pay for verified outcomes.**

OUTCOME is a prototype for conditional payments that connects an agreed outcome, submitted evidence, verification, and a potential payment settlement workflow.

## Frontend stack

- Next.js and React
- TypeScript
- Tailwind CSS
- AG Grid
- PayPal JavaScript and React SDK packages

## Current features

- Overview dashboard and outcome metrics
- Create Outcome workspace
- Contracts list with search and status filtering
- Verification workflow interface
- Responsive navigation
- AG Grid table for outcome records
- PayPal authorization component preparation

## Current prototype limitations

- Sample outcome records are stored in local React state and reset on refresh.
- Authentication and persistent user accounts require backend integration.
- PayPal authorization, capture, and void operations must be connected to the backend and tested in PayPal Sandbox.
- Evidence verification and settlement decisions are not yet confirmed as production-ready.
- Demo records are not real contracts or completed payments.

## Run locally

Requirements: Node.js and npm.

```bash
npm install
npm run dev
```

Open http://localhost:3000.

To validate the frontend:

```bash
npx tsc --noEmit
npm run build
```

## Environment configuration

Create a local `.env.local` file using the actual values supplied by the team.

```dotenv
NEXT_PUBLIC_PAYPAL_ENVIRONMENT=sandbox
NEXT_PUBLIC_PAYPAL_CLIENT_ID=
NEXT_PUBLIC_API_BASE_URL=
```

The API URL must match the backend service configured by the team. Do not commit `.env.local` or any server-side secrets.

## Backend integration

The backend team should coordinate the API contracts for:

- User registration, sign-in, and sign-out
- Outcome creation, listing, and retrieval
- PayPal order creation and authorization
- Evidence submission and verification
- Authorized payment capture or void
- Outcome status updates

Frontend and backend request formats, response formats, CORS settings, and authentication behavior must be agreed upon before integration is considered complete.

## Team

- **Frontend:** Pranav
- **Backend and integration:** Anika

This repository represents the frontend prototype. Payment and authentication claims should be updated only after the corresponding functionality has been integrated and tested.