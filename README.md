# 360-ERP (FileMaker) — ERP, CRM & Accounting for B2B Sales (Industrial Automation Sales)

**360-ERP** is a FileMaker application I built over several years to help industrial automation sales teams in the United States run the full commercial workflow efficiently — from inbound lead generation to quoting, ordering, purchasing, fulfillment, invoicing, and accounting.

It’s a practical ERP designed to reduce manual work through automation and real-world integrations (Microsoft Graph, Stripe, TaxJar, Mailchimp, UPS/FedEx, WooCommerce, DigiKey, Amazon, and FX rates).

---

## What it includes

### CRM

- Lead capture + automation from **WordPress / website forms / live chat** (auto-creates leads from new customer requests)
- Continuous **NPS measurement** via automated surveys at key stages (offer, order, invoice)
- Customer interest tracking + synchronization with marketing campaigns

### Projects

- Sales professionals create projects and track progress through offers and orders
- Management visibility into **conversion rates** and project-related cost tracking

### Sales Offers (Quoting)

- Fast creation of sales offers
- Automatic emailing of offers to internal users and external distributor reps via **Microsoft Graph**
- Multi-currency handling via **FX rate integration (XRates)**

### Sales Orders

- Manual sales order creation with payment-term-aware processing/confirmation
- Demand & supply logic:
  - automatic reservations
  - items added to a **buy report** when replenishment is required
- Automated sales tax calculation + reporting via **TaxJar**
- Automated freight cost estimation using **UPS & FedEx** (based on item gross volume)
- Multi-currency via **XRates**

### Invoicing

- Automated sales tax valuation + reporting via **TaxJar**
- Online & offline payments:
  - Credit Card + ACH through **Stripe integration**

### Purchasing

- Detects sales-order-driven demand and recommends replenishment based on:
  - sales performance
  - replenishment lead times
- Multi-currency via **XRates**

### Fulfillment / Warehouse

- Creates electronic pick & ship orders (warehouse picks or drop shipments)
- Mobile picking workflow:
  - guides employee to correct SKU location
  - reduces false picks and improves speed
- Automated shipping (UPS/FedEx, etc.)
- Automated inquiry + order placement support for **LCL/FCL shipments**

### Accounting

- Multi-currency document handling for AR/AP
- Integrated dunning (including email) via **Microsoft Graph**
- Automated payment retrieval & updates for Stripe payments
- Bank/payment reconciliation workflows
- Import bank transactions via CSV/Excel
- Fully customizable chart of accounts (supports **GAAP** + **SKR04**)
- Credit notes, AR/AP with attachments
- Financial statements:
  - P&L
  - Balance Sheet
  - Trial Balance
  - other key reports

### Inventory + Product Management

- File handling for product assets (3D files, PDFs, etc.)
- Full **WooCommerce** integration:
  - initial sync
  - continuous stock updates
- Product title/text generation using AI
- Automated SEO optimization using AI
- Marketplace integrations:
  - **DigiKey**
  - **Amazon**
- Automated product cost calculation (procurement + overhead + profit settings)
- Multi-currency via **XRates**

---

## Integrations (high level)

- **Microsoft Graph** — email automation (offers, dunning, etc.)
- **Stripe** — credit card + ACH payments (online/offline supported)
- **TaxJar** — sales tax calculation + reporting
- **Mailchimp** — NPS surveys + re-engagement campaigns
- **UPS / FedEx** — shipping automation + freight valuation
- **WooCommerce, DigiKey, Amazon** — product/order sync
- **XRates** — multi-currency conversions

---

## User Roles (test accounts)

- `SuperUser`
- `RegularUser`
- `LogisticUser`
- `FinanceUser`
- `OperationUser`
- `SalesUser`

> ⚠️ **Security note:** Do **not** publish real passwords or production authentication details in a public repository. For public demos, use a separate demo file/database with scrubbed data and disabled API keys.

---

## Authentication (Production)

Production environments can authenticate via:

- Google
- Microsoft Entra ID
- Apple
- Amazon  
  (Integration required)

---

## Installation

### Requirements

- **FileMaker Pro** (client)
- Recommended: **FileMaker Server** for multi-user / production deployments

### Setup

1. Open `360-ERP-App` in FileMaker Pro
2. Run the setup assistant:
   - company details
   - branding (logos, letterheads)
   - terms & conditions
   - other configuration items

---

## Pricing / Cost Model

Base subscription:

- **$19.99 / month** (no user restrictions)
- **$0.45 per record created**

Additional usage costs:

- **$0.05** per imported order (WooCommerce / DigiKey / Amazon)
- **$0.0035** per AI token (product/content/SEO features)
- **$0.003** per foreign currency request

If you want a better estimate for your scenario, open an issue with:

- monthly order volume
- number of products/SKUs
- expected record creation rate
- which integrations you plan to enable

---

## Repository Structure (suggested)

- `/data/` — Databases which stores the actual data
- `/docs/` — Screenshots, diagrams, setup guides
- `360-ERP-App.fmp12` - Main App
- `360-Accounting-App` - Accounting App
- `README.md`
- `LICENSE`

---

## Disclaimer

This is a personal project built and improved over years in real-world usage. Before deploying in production, review security settings, API key handling, and compliance requirements relevant to your region and use case.
