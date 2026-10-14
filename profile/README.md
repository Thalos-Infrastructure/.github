<p align="center">
  <img src="./thalos-agreement-flow.gif" width="720" alt="Thalos agreement lifecycle — Companies & Providers"/>
</p>

<p align="center">
  <b>Digital agreements.</b><br/>
  Escrow orchestration on Stellar · powered by Trustless Work
</p>

# Thalos

Thalos is an escrow orchestration layer built on the **Stellar** network. It connects transparently with the **[Trustless Work](https://docs.trustlesswork.com)** protocol to offer programmable agreements and milestone-based payments — simple and secure, designed for end users who need to protect their transactions without dealing with blockchain complexity.

> Funds stay secured until approval. Agreements that hold.

---

## Overview

Digital work still often relies on informal deals, screenshots, or blind upfront transfers. That creates friction, disputes, and risk for both sides.

Thalos replaces that with transparent, verifiable escrow rules:

**create → fund → work → evidence → review → approve → release**  
(optional **dispute** when needed)

Companies (payers) and Providers (payees) share one cycle. Either side can open an agreement; funding and release stay non-custodial via wallet signatures. Settlement is **USDC** on Stellar / Soroban.

---

## Platform Links

| Resource | URL |
| --- | --- |
| Website | https://www.thalosplatform.xyz |
| Platform | https://thalos.app |
| Frontend | https://github.com/Thalos-Infrastructure/ThalosFrontend |
| Backend | https://github.com/Thalos-Infrastructure/ThalosBackend |
| Documentation | https://github.com/Thalos-Infrastructure/thalos-docs |
| Instagram | https://instagram.com/thalos_platform |
| Trustless Work Docs | https://docs.trustlesswork.com |
| Stellar Network | https://stellar.org |
| Contact | thalosinfrastructure@gmail.com |

---

## Tech Stack

| Layer | Technology |
| --- | --- |
| Frontend | Next.js 16, React 19, TypeScript 5 |
| Styling | Tailwind CSS 4, shadcn/ui, Radix UI |
| Wallet Integration | Stellar Wallets Kit, Freighter API |
| Escrow Protocol | Trustless Work API |
| Smart Contracts | Soroban (Stellar) |
| Primary Asset | USDC (Circle) |
| Backend | Node.js, PostgreSQL, Redis *(expanding)* |
| Deployment | Vercel |

---

## 1. System Architecture

Four-layer platform architecture: how Thalos connects users to Stellar.

| Layer | Components | Status |
| --- | --- | --- |
| **Client** | Next.js frontend, Stellar Wallets Kit | Active |
| **Wallets** | Freighter, xBull, LOBSTR, Albedo, Rabet | Active |
| **Backend** | Auth, Agreement, User, Notification, Analytics · PostgreSQL · Redis | Expanding |
| **Escrow** | Trustless Work API | Active |
| **Blockchain** | Stellar Network, Soroban smart contracts, USDC trustline | Active |

- **Client** — UI, wallet connect, agreement UX (perspective, status, next action).
- **Backend** — authentication, agreement metadata, notifications *(roadmap hardening)*.
- **Escrow** — Trustless Work orchestrates contract operations.
- **Stellar** — executes and settles on-chain USDC flows.

---

## 2. Main User Flow

End-to-end journey from first visit to completed agreement. Supports **Personal** and **Enterprise** accounts, with role-specific paths for payers and providers.

| # | Phase | Description |
| --- | --- | --- |
| 1 | Entry | Visit thalos.app / landing |
| 2 | Authentication | Choose Personal or Enterprise · connect wallet |
| 3 | Dashboard | Active agreements, balances, metrics |
| 4 | Create Agreement | Title, amount, milestones, counterparty |
| 5 | Fund Escrow | Payer signs · USDC locked in contract |
| 6 | Execute Milestones | Work → evidence → review → release loop |
| 7 | Dispute Resolution | Optional · evidence, arbitration, decision |
| 8 | Completion | Settled on-chain · history recorded |

### Agreement lifecycle (Companies & Providers)

One shared cycle — either party can start; roles stay fixed after create:

| Step | Who acts | Notes |
| --- | --- | --- |
| Create agreement | Companies or Providers | Roles · milestones · **not funded yet** |
| Fund escrow | Companies | USDC locked by company |
| Wallet signs (fund) | Companies | Non-custodial fund tx |
| Work in progress | Providers | Funded · work can start |
| Submit evidence | Providers | Deliverable / GitHub |
| In review | Companies | Approve · change · dispute |
| Dispute *(optional)* | Both | Trustless Work rules |
| Approve milestone | Companies | Unlocks release |
| Wallet signs (release) | Companies | Non-custodial release |
| Release funds | Providers | USDC to provider |
| Completed | Providers | Settled on-chain |

**On-chain rails:** Trustless Work (audited Soroban escrow) · Stellar (USDC settlement).

---

## Principles

- **Security first** — funds protected by enforceable on-chain logic.
- **Simplicity** — escrow should feel like normal product UX.
- **Neutrality** — protect company and provider equally.
- **Clarity** — status, milestone progress, and next action always visible.

---

## Team

<div align="center">

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Kalchaqui">
        <img src="https://github.com/user-attachments/assets/4079a4f0-8ab5-43bf-8a02-267c5c471691" width="80" alt="Diego"><br>
        <b>Diego Raúl Barrionuevo</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/leandromasotti">
        <img src="https://github.com/user-attachments/assets/426f321b-130d-41ea-a254-994859d655f2" width="80" alt="Leandro"><br>
        <b>Leandro Masotti</b>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/ManuelJG1999">
        <img src="https://github.com/user-attachments/assets/3d535208-1054-4c5e-8253-3740d12e78f0" width="80" alt="Manuel"><br>
        <b>Manuel Jiménez Garro</b>
      </a>
    </td>
  </tr>
</table>

</div>

---

## Roadmap

**Near term**
- Clearer agreements UX (filters, perspective, next action)
- Evidence & demo readiness for ecosystem programs
- Backend hardening (auth, notifications, analytics)

**Next**
- Deeper agreement templates / customization
- Additional payment rails
- Broader digital-agreement use cases

---

Thalos — **Digital agreements.**
