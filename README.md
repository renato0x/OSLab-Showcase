<div align="center">
  <br/>
  <h1>ALTOLAB OS</h1>
  <p><strong>Complete platform for managing service orders, customers, scheduling, and financial control</strong></p>
  <p>Built for small repair shops and technical assistance businesses</p>
  <br/>
  <a href="https://altolab-painel.vercel.app" target="_blank"><strong>Management Panel</strong></a>
  ·
  <a href="https://altolabtech.vercel.app" target="_blank"><strong>Customer Portal</strong></a>
  <br/><br/>
  <a href="#">
    <img src="https://img.shields.io/badge/Next.js%2015-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js 15"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Tailwind%20CSS%204-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel"/>
  </a>
  <br/>
  <a href="#">
    <img src="https://img.shields.io/badge/Shadcn/ui-000000?style=flat-square&logo=shadcnui&logoColor=white" alt="Shadcn/ui"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Lucide-FF6B6B?style=flat-square&logo=lucide&logoColor=white" alt="Lucide"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Playwright-45BA4B?style=flat-square&logo=playwright&logoColor=white" alt="Playwright"/>
  </a>
  <br/><br/>
</div>

---

## OVERVIEW

ALtoLab OS is a full-stack management system designed for electronics repair shops and technical assistance businesses. It streamlines the entire workflow from customer intake to service delivery and payment collection.

### Key Capabilities

- **Service Order Lifecycle** — Full Kanban workflow from new intake through diagnosis, budgeting, parts ordering, repair, testing, delivery, and closure
- **Customer Relationship Management** — Complete registry with service history, contact management, and export capabilities
- **Financial Control** — Dashboard with revenue overview, payment tracking with proof of payment, method configuration, and CSV export
- **Operational Schedule** — Calendar for pickup, delivery, and technical visit appointments
- **Client Communication** — Automated WhatsApp messages for status changes, budget approvals, and payment requests

---

## SCREENSHOTS

<div align="center">

| Panel | Orders |
|:---:|:---:|
| ![Dashboard](screenshots/dashboard.png) | ![Orders Kanban](screenshots/orders-kanban.png) |

| Customers | Finance |
|:---:|:---:|
| ![Customers](screenshots/customers.png) | ![Financial Dashboard](screenshots/financeiro.png) |

| Schedule | Reports |
|:---:|:---:|
| ![Schedule](screenshots/schedule.png) | ![Reports](screenshots/reports.png) |

</div>

---

## TECH STACK

| Layer | Technology |
|---|---|
| **Frontend** | Next.js 15 (App Router), TypeScript, Tailwind CSS 4, Shadcn/ui, Lucide React |
| **Backend** | Next.js API Routes, Supabase (PostgreSQL, Auth, Storage) |
| **Infrastructure** | Vercel (hosting), GitHub (version control) |

### Why this stack

- **Next.js 15 App Router** — Server components, streaming, and nested layouts for optimal performance
- **Supabase** — Open-source Firebase alternative with PostgreSQL, built-in auth, and Row-Level Security
- **Tailwind CSS 4 + Shadcn/ui** — Utility-first CSS with accessible, unstyled components
- **TypeScript** — End-to-end type safety across frontend and backend

---

## FEATURES

### Service Order Management
- Kanban board with 13 statuses in the workflow pipeline
- Detail view showing device info, budget items, payment history, and event log
- Smart status transitions with conditional steps (parts selection for awaiting parts, diagnosis review for approval)
- Budget creation with parts items (JSONB) and labor amounts
- Event history recording every status change and action

### Customer Management
- Searchable customer registry with CPF/CNPJ, phone, address, and neighborhood
- Per-customer service history linked to all their orders
- CSV export with UTF-8 BOM for Excel compatibility

### Financial Dashboard
- Overview cards: total received, pending, overdue, monthly revenue
- Payment listing with filters by date range, payment method, and status
- Payment detail view with proof of payment upload (images, PDF)
- Payment methods CRUD (PIX, cash, credit/debit card, bank transfer, boleto)
- PIX key and name configuration from the interface
- CSV export for payment records

### Operational Schedule
- Calendar view with event creation and management
- Events types: pickup, delivery, technical visit, general appointment
- Linked to customers and service orders

### Reports and Analytics
- Daily and monthly revenue charts
- Service order status distribution
- Exportable data

### WhatsApp Integration
- Automatic notifications for status changes, budget creation, and payment requests
- Diagnosis details and PIX information included in messages
- Direct links to WhatsApp chat with customers

### Security
- Rate limiting: 30 requests/min general, 5 requests/min login
- Security headers: HSTS, X-Frame-Options, Content-Security-Policy
- Row-Level Security (RLS) on all Supabase tables
- Generic error messages on login (no information leakage)
- Admin authentication via Supabase Auth with secure credential policies

---

## LIVE DEMOS

| Application | URL | Description |
|---|---|---|
| **Management Panel** | [altolab-painel.vercel.app](https://altolab-painel.vercel.app) | Full admin interface for daily operations |
| **Customer Portal** | [altolabtech.vercel.app](https://altolabtech.vercel.app) | Public-facing website with WhatsApp chat support |

---

## PROJECT STRUCTURE

```
OSLab/
  altolab-painel/       # Next.js 15 management panel
    ├── src/app/        # App Router pages and API routes
    ├── src/components/  # Reusable UI components
    ├── src/lib/         # Utilities, helpers, integrations
    └── supabase/       # Database migrations
  altolab-site/         # Static customer-facing website
```

---

<div align="center">
  <br/>
  <sub>Built with care for small businesses in Montes Claros, MG</sub>
  <br/><br/>
</div>
