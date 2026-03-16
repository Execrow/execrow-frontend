# Execrow Frontend

> The operator dashboard for managing autonomous AI agents, monitoring budgets, reviewing task activity, and controlling agent permissions — built with Next.js.

This repository contains the web application that human operators use to interact with the Execrow protocol. It gives operators full visibility and control over their agents — provisioning new agents, setting budgets and permission scopes, monitoring active tasks, reviewing completed work, managing disputes, and exercising emergency override when needed.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Repository Structure](#repository-structure)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The Execrow operator dashboard is designed for humans who deploy AI agents that make financial decisions on their behalf. It provides:

- **Agent Management** — create, configure, pause, and terminate agents
- **Budget Control** — set and adjust budget ceilings and permission scopes in real time
- **Task Monitor** — live view of all active and completed tasks across all agents
- **Escrow Tracker** — see all open escrow positions, amounts locked, and conditions
- **Reputation Dashboard** — view agent and counterparty reputation scores and history
- **Dispute Center** — manage open disputes, review evidence, and track rulings
- **Activity Feed** — real-time feed of all financial events across the operator's agents
- **Analytics** — aggregate metrics on agent performance, spend, success rates

---

## Features

- 🔐 **Wallet connect** — connect your Stellar wallet via Freighter or any WalletConnect-compatible wallet
- 📊 **Real-time updates** — live task and payment updates via WebSocket
- 🚨 **Emergency pause** — one-click pause for any or all agents
- 📱 **Responsive design** — works on desktop and mobile
- 🌙 **Dark mode** — because operators work at all hours
- 🔔 **Notifications** — browser and email notifications for critical events

---

## Repository Structure
```

execrow-frontend/
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── dashboard/
│   │   │   └── page.tsx
│   │   ├── agents/
│   │   │   ├── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   ├── tasks/
│   │   │   └── page.tsx
│   │   ├── escrow/
│   │   │   └── page.tsx
│   │   ├── disputes/
│   │   │   └── page.tsx
│   │   └── analytics/
│   │       └── page.tsx
│   ├── components/
│   │   ├── agents/
│   │   ├── tasks/
│   │   ├── escrow/
│   │   ├── disputes/
│   │   ├── analytics/
│   │   └── shared/
│   ├── hooks/
│   │   ├── useAgent.ts
│   │   ├── useTask.ts
│   │   ├── useEscrow.ts
│   │   └── useWebSocket.ts
│   ├── lib/
│   │   ├── api.ts
│   │   ├── stellar.ts
│   │   └── utils.ts
│   ├── store/
│   │   └── index.ts
│   └── types/
│       └── index.ts
├── public/
├── tests/
├── .env.example
├── next.config.js
├── tailwind.config.js
├── package.json
├── tsconfig.json
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

---

## Prerequisites

- Node.js `>=20.0.0`
- [Freighter Wallet](https://freighter.app) browser extension for Stellar

---

## Getting Started
```bash
git clone https://github.com/Execrow/execrow-frontend.git
cd execrow-frontend
cp .env.example .env.local
npm install
npm run dev
```

Open `http://localhost:3000`

---

## Environment Variables
```env
NEXT_PUBLIC_API_URL=http://localhost:3001
NEXT_PUBLIC_STELLAR_NETWORK=testnet
NEXT_PUBLIC_WS_URL=ws://localhost:3001
```

---

## Contributing

We especially welcome contributors with experience in Next.js, TailwindCSS, data visualization, and Web3 wallet integrations. Browse [`good first issue`](https://github.com/Execrow/execrow-frontend/issues?q=label%3A%22good+first+issue%22) to get started.

---

## License

[Apache 2.0](LICENSE) — Execrow Organization, 2025

---

<div align="center">

Part of the [Execrow](https://github.com/Execrow) open-source organization.

**The payment infrastructure layer for autonomous AI agents.**

</div>
