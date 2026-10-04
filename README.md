# Awesome-AI-Finance-Assistant

# Awesome AI Finance Assistant

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Conversational Accounting, AI-Native ERP, Financial Close Automation & Receipt Intelligence*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **AI Finance Assistants**. These tools help finance teams and individuals interact with their books using natural language—generating invoices, reconciling accounts, closing periods, and analyzing financials without manual data entry.

**Examples** include Microsoft Copilot for Finance, Vic.ai, Numeric, Rillet, Booke AI, Datarails, Osfin AI, Truewind, Digits, and Bluecopa (the category leaders).

**Open-source emphasis**: The open-source ecosystem for AI finance assistants is **emerging and genuinely production-capable** at the individual and small-business scale. **ERPClaw** (GPL v3) is the standout—an AI-native ERP where you "chat with your books" using plain English, with full double-entry accounting, US GAAP compliance, and self-hosted deployment . **TaxHacker** (self-hosted) provides an LLM-powered analyzer for receipts, invoices, and transactions with custom prompts and categories . **cfo-stack** (MIT) delivers 27 AI skills for personal and business finance using plain-text Beancount ledgers . **dsh-finance** ports Anthropic's finance skills to DeepSeek Harness with deterministic validation tools . **ezBookkeeping** brings AI receipt recognition and MCP integration to a lightweight Go-based personal finance app . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Microsoft Copilot for Finance](https://www.microsoft.com/en-us/copilot/finance)**
  **AI assistant for finance teams embedded in Microsoft 365.** Combines Copilot with role-based agents for financial analysis, reconciliation support, and reporting. **Key integrations**: Excel, Outlook, Teams, and Dynamics 365. **Requirement**: Microsoft 365 Copilot license per user.

- **[Vic.ai](https://www.vic.ai/)**
  **AI-powered invoice processing and accounts payable automation.** Uses proprietary AI to code invoices, route approvals, and detect anomalies. **Real-time analytics** provide spend visibility and vendor intelligence.

- **[Numeric](https://www.numeric.io/)**
  **AI-first close automation that sits on top of existing ERP.** Automates accruals, reconciliations, and flux analysis with transaction-level ERP visibility. Designed for scaling SaaS companies.

- **[Rillet](https://www.rillet.com/)**
  **AI-native ERP that replaces the accounting workflow itself.** The GL is continuously updated from connected systems, subledgers post near-real-time, and reconciliations run continuously. Aura AI autonomously books journal entries with source documentation.

- **[Booke AI](https://booke.ai/)**
  **AI Bookkeeper that works inside QuickBooks Online or Xero as an invited user.** Performs categorization, matching, and reconciliation preparation through the native accounting interface. Claims 95% autonomy.

- **[Datarails](https://www.datarails.com/)**
  **FP&A platform that keeps Excel at the center.** AI-powered insights, automated data consolidation, and financial storytelling for mid-market finance teams.

- **[Osfin AI](https://osfin.ai/)**
  **AI-powered reconciliation and financial close platform.** Automates transaction matching, exception handling, and close checklists for enterprises.

- **[Truewind](https://www.truewind.ai/)**
  **AI-powered accounting automation focused on review-ready preparation.** Emphasizes source-linked workpapers and exception-first review, showing source, calculation, accounting treatment, and reviewer sign-off in one place.

- **[Digits](https://digits.com/)**
  **Financial intelligence platform combining automated bookkeeping with AI-driven analysis.** Connects to 12,000+ U.S. financial institutions via Plaid. AI-native ledger positioning with "Ask Digits" conversational interface.

- **[Bluecopa](https://bluecopa.com/)**
  **Finance operations automation platform.** Provides AI-powered reconciliation, close management, and financial analytics for enterprises.

## Open-Source GitHub Projects

### AI-Native ERP & Accounting Platforms

- **[ERPClaw](https://github.com/avansaber/erpclaw)**
  **The AI-native ERP: "chat with your books" — free forever, self-hosted (GPL v3).** **Built AI-native from the first commit** with the assistant as primary interface and accounting rules as auditable code . **Key features**: **Double-entry general ledger** with US GAAP chart of accounts, immutable journal entries, multi-company, multi-currency; **Sales & buying** (customers, suppliers, orders, invoices, credit notes); **Inventory** (items, warehouses, stock moves, serial/batch tracking, valuation); **Payments & billing** (payment entries, bank reconciliation, usage-based billing, subscriptions); **Tax & payroll** (tax templates, FICA, W-2s); **Advanced accounting** (ASC 606 revenue recognition, ASC 842 leases, intercompany transactions, consolidation); **Reporting** (trial balance, P&L, balance sheet, cash flow, AR/AP aging) . **Industry coverage**: Retail, healthcare, education, property, construction, agriculture, legal, nonprofit, plus regional tax packs for Canada, UK, India, and EU . **Deployment**: SQLite by default, PostgreSQL fully supported; self-hosted at `~/.openclaw/erpclaw/data.sqlite`; **$0 forever, no freemium tier, no per-seat pricing** . **Quick start**: `clawhub install erpclaw`, then tell your assistant "I'm opening a retail store called Sunrise Goods in Portland, Oregon. Set me up." .

### Receipt & Transaction Intelligence

- **[TaxHacker](https://github.com/vas3k/TaxHacker)**
  **Self-hosted AI accounting app with LLM analyzer for receipts, invoices, and transactions.** **Key features**: **Custom categories, projects, and fields** (unlimited customization); **Full-text search** through recognized documents; **AI-powered extraction** with custom prompts; **Bulk operations** for multiple documents . **LLM support**: OpenAI, Anthropic, and **local LLM** (Ollama, LM Studio, vLLM, LocalAI) via OpenAI-compatible API . **Deployment**: Docker Compose with PostgreSQL 17+; automatic migrations; `no-new-privileges` security option . **Data ownership**: Your financial documents never leave your control; export everything and migrate whenever .

### Personal & Small Business Finance Automation

- **[cfo-stack](https://github.com/MikeChongCan/cfo-stack)**
  **Open-source AI CFO and Tax Accountant for individuals and businesses (MIT).** **27 skills** organized across Capture → Log → Extract → Automate . **Key skills**: `/cfo-capture` (inventory and route files); `/cfo-statement-export` (guided Chrome DevTools MCP export for bank/card/brokerage statements); `/cfo-bank-import` (smart CSV import with format auto-detection); `/cfo-receipt-scan` (OCR receipt photos); `/cfo-log` (transform raw data into Beancount double-entry); `/cfo-classify` (AI categorization with learning and tax treatment); `/cfo-validate` (bean-check + custom rules); `/cfo-report` (income statement, balance sheet, cash flow); `/cfo-tax-plan` (deductions, income splitting, quarterly estimates); `/cfo-consult` (cross-model consultant) . **Architecture**: Plain-text Beancount ledger with Git version control; Fava UI for web reports; Python scripts for importers/classifiers . **Privacy-first option**: `/cfo-statement-export-private` produces a manual checklist only—no browser tools .

- **[dsh-finance](https://github.com/zhang787jun/dsh-finance)**
  **Finance and accounting plugin for DeepSeek Harness—adapted from Anthropic's official finance plugin.** **Eight skills** with upstream parity: journal entries, journal-entry-prep, reconciliation, financial statements, variance analysis, close management, audit support, and SOX testing . **Deterministic DSH validation tools**: `finance_journal_entry_check` (validates debit-credit balance, line structure, documentation gaps, preparer/approver separation—never authorizes posting); `finance_reconciliation_snapshot` (calculated adjusted balances, item aging, stale-item flags, sign-off readiness); `finance_variance_bridge` (proves signed drivers bridge base to actual, exposes residuals, evaluates materiality) . **Human approval boundary**: Prepares and validates analyst work product—does not post journal entries . **Install**: `dsh plugin --profile web add github:zhang787jun/dsh-finance` .

- **[ezBookkeeping](https://github.com/mayswind/ezbookkeeping)**
  **Lightweight, self-hosted personal finance app with AI receipt recognition and MCP support.** **Key features**: Two-level accounts and categories; attach images to transactions; location tracking with maps; recurring transactions; advanced filtering, search, visualization, and analysis . **AI-powered**: Receipt image recognition; **MCP (Model Context Protocol)** for AI integration . **Data import/export**: CSV, OFX, QFX, QIF, IIF, Camt.053, MT940, GnuCash, Firefly III, Beancount, and more . **Deployment**: Single Docker command (`docker run -p8080:8080 mayswind/ezbookkeeping`); SQLite, MySQL, PostgreSQL; runs on Raspberry Pi or scales to clusters . **Security**: Two-factor authentication, login rate limiting, application lock (PIN/WebAuthn) .

### Additional Strong Open-Source Options

- **AI-Native ERP**: **ERPClaw** (GPL v3, chat-with-books, full double-entry) .
- **Receipt Intelligence**: **TaxHacker** (self-hosted, custom prompts, local LLM) .
- **Personal Finance AI**: **cfo-stack** (MIT, 27 skills, Beancount), **dsh-finance** (DeepSeek Harness, deterministic validation), **ezBookkeeping** (Go, MCP, AI receipt recognition) .
- **Cryptographic Accounting**: **Taraz** (MIT, SHA-256 immutability, IFRS reports) .

**Frameworks for building custom systems**: Combine **ERPClaw** for a complete AI-native ERP with conversational accounting, **TaxHacker** for receipt and transaction intelligence with custom prompts, **cfo-stack** for personal/small business finance automation with Beancount ledgers, **dsh-finance** for deterministic journal entry and reconciliation validation, and **ezBookkeeping** for lightweight personal finance with MCP integration. Add **PostgreSQL** for persistence and **Docker** for deployment.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- AI finance assistants handle sensitive financial data; ensure compliance with accounting standards, tax regulations, and data protection laws.
- **Open-source reality**: The open-source ecosystem for AI finance assistants is **emerging and production-capable at the individual and small-business scale**. **ERPClaw** is the standout—a GPL v3 AI-native ERP with full double-entry accounting, US GAAP compliance, and conversational interface, free forever and self-hosted . **TaxHacker** provides LLM-powered receipt intelligence with custom prompts and local LLM support . **cfo-stack** delivers 27 AI skills for personal and business finance with Beancount ledgers . **dsh-finance** brings deterministic validation to journal entries and reconciliations . **ezBookkeeping** adds AI receipt recognition and MCP integration to lightweight personal finance . However, **commercial platforms** (Microsoft Copilot for Finance, Vic.ai, Numeric, Rillet) provide **enterprise ERP integrations, managed infrastructure, and dedicated support** that open-source alternatives require additional configuration to match. The open-source path is **genuinely viable** for individuals, small businesses, and finance teams with strong technical capacity seeking full data sovereignty and zero per-seat fees.
