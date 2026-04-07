# IMPERION - Nigeria's Premier Online Earning Platform

## Overview

IMPERION is a full-featured earning platform built with React + Vite, Firebase Firestore, and Firebase Storage. It is a pnpm workspace monorepo.

## IMPERION Features

### User Features
- Landing page with reviews, features, how-to guide
- Sign Up / Login (6-digit password, unique username, IP tracking)
- Dashboard: Task, Referral, Deposit, Daily Claim balances
- Tasks: Admin-posted tasks, image proof upload, approval/decline
- Deposit: Bank transfer to Opay, receipt upload to Firebase Storage
- Withdraw: Task (₦2,000 min), Referral (₦1,000 min), Daily (₦1,000 min)
- Referrals: Unique referral link, 10% commission on referral's first deposit
- Daily Bonus: ₦100 claim every 24 hours with real countdown
- Investment Machines: Lite/Basic/Standard/Premium (daily profit, withdrawal)
- Account Activation: ₦1,000 one-time fee from deposit balance
- Airtime/Data: One-time ₦200 purchase (deducted from task balance)
- History: All deposit/withdrawal records with status
- Place Ads: WhatsApp redirect

### Admin Panel
- Access: Press "A" button, enter passcode "2011"
- Manage: Withdrawals, Deposits, Task Proofs (approve/decline)
- View: Total users, all balances
- Tasks: Add tasks with category, link, price, description
- Portals: Open/close withdrawal portals per type

### Firebase Collections
- users, deposits, withdrawals, taskSubmissions, tasks, reviews, airtimeOrders, portalStatus

## Tech Stack

- **Frontend**: React + Vite + Wouter + TailwindCSS
- **Backend**: Firebase Firestore + Firebase Storage
- **Auth**: Custom (email + 6-digit PIN, stored in Firestore)
- **Monorepo**: pnpm workspaces

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
