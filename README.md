# stellarlearn-frontend

> A Next.js + TypeScript web application for browsing, enrolling in, and completing tech courses on the StellarLearn platform.

---

## About

StellarLearn is an open-source Web3 course platform built on the Stellar blockchain. Learners can browse and enroll in free or paid tech courses, track their progress, and receive verifiable NFT certificates upon completion — minted directly to their Stellar wallet.

This repository contains the frontend web application.

---

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Wallet:** Freighter (Stellar wallet integration)
- **State Management:** Zustand
- **HTTP Client:** Axios

---

## Getting Started

### Prerequisites

- Node.js >= 18
- pnpm >= 8
- A running instance of [stellarlearn-backend](https://github.com/StellarLearn-Labs/stellarlearn-backend)

### Installation

```bash
git clone https://github.com/StellarLearn-Labs/stellarlearn-frontend.git
cd stellarlearn-frontend
pnpm install
cp .env.example .env.local
```

### Environment Variables

```env
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_STELLAR_NETWORK=testnet
```

### Running Locally

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## Project Structure

```
stellarlearn-frontend/
├── app/
│   ├── (auth)/                 # Login, register
│   ├── courses/                # Browse and course detail
│   ├── learn/                  # Lesson player
│   ├── dashboard/              # Creator and learner dashboards
│   └── certificates/           # Public certificate viewer
├── components/
│   ├── ui/                     # Base components
│   ├── course/                 # Course-specific components
│   ├── layout/                 # Header, Footer, Sidebar
│   └── certificate/            # Certificate components
├── hooks/                      # Custom React hooks
├── lib/                        # Utilities and API helpers
├── store/                      # Zustand stores
├── types/                      # TypeScript types
└── public/                     # Static assets
```

---

## Pages

| Route | Description |
|-------|-------------|
| `/` | Landing page |
| `/courses` | Browse all courses |
| `/courses/:id` | Course detail and enrollment |
| `/learn/:courseId` | Lesson player |
| `/dashboard/creator` | Creator course management |
| `/dashboard/learner` | Learner progress and certificates |
| `/certificates/:address` | Public certificate viewer |

---

## Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) before opening a pull request.

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push and open a pull request targeting `main`

---

## Related Repositories

| Repo | Description |
|------|-------------|
| [stellarlearn-backend](https://github.com/StellarLearn-Labs/stellarlearn-backend) | REST API and database |
| [stellarlearn-contracts](https://github.com/StellarLearn-Labs/stellarlearn-contracts) | Soroban smart contracts |

---

## License

MIT © [StellarLearn](https://github.com/StellarLearn-Labs)