# RFQ (Request for Quotation)

The **RFQ** module manages the full procurement quotation lifecycle — from creating requests linked to technical inquiries, through supplier invitation via email, quotation collection, comparison, evaluation, and final award. It integrates deeply with the Microsoft Graph API for email communication and includes AI-powered features for automated quotation processing.

---

## Accessing the Module

Navigate to **RFQ** from the left sidebar. The module contains the following sub-sections:

| Sub-menu | Description |
|----------|-------------|
| **Dashboard** | Statistics, user performance, and supplier analytics |
| **RFQ** | Main RFQ list — create, edit, send, and track RFQs |
| **RFQ Items** | Items linked to RFQs from technical inquiries |
| **Items** | Master item catalog and comparison sheet items |
| **RFQ Emails** | Supplier reply emails fetched via Microsoft Graph API |
| **AI Quotation Backlog** | AI-processed quotation extraction queue |
| **Procurement Mails** | General procurement inbox (non-RFQ emails) |
| **Webmail** | Web-based email viewer for procurement mailbox |
| **KPI Report** | Employee RFQ performance dashboards |
| **Comparison Sheet** | Side-by-side supplier quotation comparison |
| **Reports** | RFQ reports with reply/action tracking |
| **Settings** | Admin-only RFQ configuration |

---

## Dashboard

The RFQ Dashboard provides a real-time overview of procurement activity with multiple analytical views.

### Statistics Overview

- **Pending RFQs** — Count of RFQs awaiting action
- **Accepted RFQs** — Count of accepted/active RFQs
- **Quotations** — Total quotations received
- **Supplier Latency** — Average response time from suppliers
- **Monthly Trends** — Charts showing RFQs created, replies received, quotations, and actions per month

### User Performance

View performance metrics per procurement user:

- RFQs created (total and monthly)
- Supplier replies received
- Quotations processed
- Actions taken
- Replies needing action
- Active RFQ statistics

### Supplier Analytics

View per-supplier performance:

- RFQs sent to supplier
- Accepted/pending RFQ breakdown
- Total replies and quotations
- Purchase orders generated
- Response latency tracking
- Monthly activity trends

### Period Filtering

Filter all dashboard data by:

- Today, This Week, Last Week, This Month, Last Month
- Custom date range

---

## RFQ List

The main RFQ view displays all requests in an interactive AG Grid table.

### Key Columns

- **RFQ Code** — Unique reference number (e.g., RFQ-24000067)
- **Email Subject** — Subject line used for supplier communication
- **Status** — Current lifecycle status (Draft, Pending, Active/Accepted, Closed, Archived)
- **Related Project** — Linked project or budget source
- **Owner** — Assigned procurement officer
- **Supplier Response Status** — Replies received / suppliers invited
- **Creation Date** and **Due Date**

### Actions

- **Create RFQ** — Initiate a new quotation request
- **View/Edit** — Open RFQ details
- **Delete** — Soft-delete with activity logging
- **Send to Suppliers** — Dispatch via email
- **Fetch Emails** — Pull latest supplier replies from Microsoft Graph API

### Filtering

Filter by status, supplier, project, assigned user, and date ranges.

---

## Creating an RFQ

### Step 1: Select Items

Items come from **Technical Inquiries**. Select one or more inquiry items to include in the RFQ.

### Step 2: Select Suppliers

Choose suppliers from the approved supplier list. Each supplier's contacts are loaded automatically.

### Step 3: Configure RFQ Details

- **Subject** — Clear description of what is being quoted
- **Related Project** — Link to a project
- **Owner** — Assign responsible procurement officer
- **Due Date** — Supplier response deadline
- **RFQ Type** — Supplier (materials) or Service

### Step 4: Email Settings

- **Email Subject** — Subject line for the invitation email
- **Sender** — Select sending entity (Prizm Energy or Al Manshour Contracting)
- **Email Template** — Predefined or custom email body

### Step 5: Terms and Notes

- **Public Remarks** — Visible to suppliers in the invitation
- **Internal Notes** — For the procurement team only
- **Terms and Conditions** — Commercial terms

### Step 6: Save or Send

- **Save as Draft** — Continue editing later
- **Send** — Dispatch to all selected suppliers via Microsoft Graph API

!!! info "RFQ Code"
    Each RFQ is assigned a unique code (e.g., RFQ-24000067) which is included in all email subjects. The system uses this code to automatically match supplier replies to the correct RFQ.

---

## RFQ Stages & Statuses

| Status | Description |
|--------|-------------|
| **Draft** | Being prepared; fully editable; not visible to suppliers |
| **Pending** | Awaiting internal approval or additional information |
| **Accepted/Active** | Sent to suppliers; awaiting responses; core fields locked |
| **Expired** | Response deadline passed; can be extended or closed |
| **Closed** | Supplier awarded; converted to PO or contract |
| **Archived** | Stored for reference; read-only |

!!! warning "Field Locking"
    Once an RFQ is sent (Active status), core fields are locked to ensure fair comparison across all suppliers. Only the status and internal notes can be modified.

---

## Supplier Invitations & Email Integration

### Sending Invitations

Invitations are sent via **Microsoft Graph API** using the configured procurement email accounts:

- **Prizm Energy** — procurement@prizm-energy.com
- **Al Manshour Contracting** — procurement@almanshour.com

Each invitation includes the RFQ code in the subject line, item details, specifications, response deadline, and submission instructions.

### Automatic Reply Fetching

The system runs a **cron job** that:

1. Connects to Microsoft Graph API
2. Fetches new emails from the procurement mailbox
3. Matches replies to RFQs by the **RFQ code in the subject line**
4. Filters out internal emails (@prizm-energy.com, @almanshour.com)
5. Excludes bounce-back notifications (Undeliverable, Delivery Failed, etc.)
6. Stores valid supplier replies with attachments

### Reply Tracking

For each supplier, the system tracks:

- Invitation sent timestamp
- Replies received (count and content)
- Attachments uploaded
- Response latency
- Actions taken on replies

---

## RFQ Items

RFQ Items are sourced from **Technical Inquiries** and define what is being quoted.

### Item Fields

- **Item ID** and **Item Name** — Unique identifier and short name
- **Item Long Name** — Full descriptive name
- **Technical Inquiry Reference** — Source inquiry
- **Quantity** and **Unit of Measure**
- **Specifications** and **Requirements**

### Item Status Tracking

Items have their own status workflow, tracking progression through the RFQ process with summary statistics.

---

## Comparison Sheet

The Comparison Sheet provides a structured side-by-side comparison of supplier quotations.

### Features

- View all supplier quotes for the same item in one table
- Compare prices, delivery terms, and conditions
- Highlight lowest price or best value
- Add internal evaluation notes
- Track item-level details across multiple RFQs

### Access

Navigate to **RFQ > Comparison Sheet** or search for specific items via global search.

---

## AI Quotation Backlog

The **AI Quotation Backlog** automates quotation extraction from supplier reply emails.

### How It Works

1. Supplier replies are fetched and stored
2. AI processes the email content and attachments
3. Quotation data (prices, quantities, terms) is extracted
4. Extracted data is queued for human review
5. Approved data updates the comparison matrix

### Backlog Management

- View pending and processed quotations
- Track extraction status and counts
- Separate views for RFQ emails and procurement mails

---

## Procurement Mails

General procurement emails that are **not** tied to a specific RFQ.

### Features

- Fetched from Microsoft Graph API
- Filtered to exclude internal emails and bounce-backs
- Linked to supplier contacts when possible
- Searchable by subject, supplier name, or contact name
- Status tracking (pending/processed)
- Mail count statistics

---

## Webmail

A web-based email viewer embedded within the RFQ module, providing direct access to the procurement mailbox without leaving the system.

---

## KPI Report

Employee performance dashboards for the procurement team.

### Metrics Tracked

- **RFQs Created** — Per user and period
- **Replies Received** — Supplier response tracking
- **Quotations Processed** — Converted quotations
- **Actions Taken** — User activity on replies
- **Response Latency** — Average time to handle replies

### Views

- **Department KPI** — Overview of all procurement users
- **User KPI** — Individual detailed dashboard
- **Procurement KPI** — Procurement-specific metrics
- **Employee KPI** — Per-employee with manager context

---

## Reports

### Reply & Action Reports

- RFQ replies received vs. actions taken
- Per-user and per-period breakdown
- Conflict detection for RFQ emails vs. procurement mails
- Export capabilities

### Period Filtering

Same period options as dashboard (Today, This Week, Last Week, This Month, Last Month, Custom).

---

## RFQ Engine (v2)

The **RFQ Engine** is an AI-driven pipeline that automates the RFQ process with a "System acts, human reviews" approach.

### Pipeline Stages

| Stage | Description |
|-------|-------------|
| **Intake** | System detects flagged items, proposes RFQ grouping |
| **Compose** | AI drafts RFQ content (title, description, terms, notes) |
| **Match** | System recommends suitable suppliers |
| **Approve** | Human final review before sending |
| **Sent** | System dispatches emails via Microsoft Graph API |
| **Tracking** | System monitors for supplier replies |
| **Received** | Replies classified and quotations extracted |
| **Compared** | Comparison matrix auto-generated |
| **Awarded** | Winner selected by human review |
| **Closed** | RFQ lifecycle complete |

### Automated Cron Tasks

The RFQ Engine runs three automated background tasks:

1. **Auto-Intake** — Detects new flagged items and proposes RFQ groupings
2. **Auto-Track** — Fetches supplier replies from Microsoft Graph API
3. **Auto-Remind** — Sends reminders for approaching or past-due deadlines

### Integration

The RFQ Engine adds a tab to the **Project view**, allowing you to see all RFQ Engine requests related to a project.

---

## Integration with Other Modules

| Module | Integration |
|--------|-------------|
| **Technical Inquiries** | Auto-create RFQ when TI status changes; items sourced from TIs |
| **Projects** | RFQ tab in project view; link RFQs to projects |
| **Purchases** | Convert awarded RFQs to Purchase Orders |
| **Suppliers** | Supplier contacts, quotation tracking, latency analytics |
| **Advance Leads** | Supplier and lead data integration |
| **Microsoft Graph** | Email send/receive for invitations and reply fetching |

---

## Permissions

### RFQ Permissions

| Module | Permissions |
|--------|------------|
| **RFQ** | View (Global), View Own, Action, Change Status, Change Activation, Create, Edit, Convert, Delete |
| **RFQ Items** | View (Global), View Own, Edit, Delete |
| **RFQ Emails** | View (Global), View Own, Edit, Delete |
| **RFQ Reports** | View (Global), View Own, Edit, Delete |
| **KPIs** | View (Global), View Own, Edit, Delete |
| **Comparison Sheet** | View (Global) |
| **RFQ Engine (v2)** | View, Create, Edit, Delete |

!!! tip "Admin Access"
    The **Settings** sub-menu is only visible to administrators. This includes RFQ configuration, email templates, and keyword management.

---

## Global Search

The RFQ module is fully integrated with the system-wide global search. You can search across:

- **RFQs** — By RFQ code or email subject
- **RFQ Items** — By item name or long name
- **RFQ Emails** — By subject, contact name, or RFQ code
- **Procurement Mails** — By subject or supplier/contact name
- **Comparison Sheet** — By item name or long name

---

## Best Practices

- **Define items clearly** in Technical Inquiries before creating RFQs — detailed specifications reduce supplier clarification requests
- **Invite 3-5 suppliers** for competitive pricing
- **Monitor the AI Quotation Backlog** regularly to review and approve extracted quotation data
- **Use the Comparison Sheet** before making award decisions — it provides a structured view of all quotes
- **Check KPI Reports** weekly to track team productivity and identify bottlenecks
- **Review Procurement Mails** for supplier communications that may not be tied to a specific RFQ

---

## Known Limitations

- RFQs cannot be edited after sending to suppliers — core fields are locked to ensure fairness
- Awarded RFQs cannot be deleted — use archive instead
- Email reply matching depends on the RFQ code being present in the email subject line
- Microsoft Graph API credentials must be configured and valid for email features to work
- The AI Quotation Backlog requires human review before extracted data is applied
