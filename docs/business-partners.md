# Business Partners

The **Business Partners** module provides a centralized registry for managing all companies your organization interacts with — whether they are customers, suppliers, or both. It eliminates duplicate entries, organizes companies into groups, and includes AI-powered enrichment to automatically populate partner details.

---

## Accessing the Module

Navigate to **Business Partners** from the left sidebar menu. The module contains four sub-sections:

| Sub-menu | Description |
|----------|-------------|
| **Business Partners** | Main list of all partners |
| **Name Group** | Parent company grouping and merge tool |
| **AI Enrichment Tracking** | Monitor AI data enrichment status |
| **AI Operation Logs** | Audit trail of all AI operations |

---

## Business Partners List

The main view displays all business partners in an interactive AG Grid table with the following columns:

| Column | Description |
|--------|-------------|
| **#** | Unique ID |
| **Company** | Company name |
| **Email** | Contact email address |
| **Customer** | Whether this partner is marked as a customer |
| **Supplier** | Whether this partner is marked as a supplier |

### Toolbar Actions

- **Add Business Partners** — Create a new partner record
- **Bin Records** — View soft-deleted partners that can be restored

### Filtering

Use the **Advanced Filter** system to build custom queries:

- Filter by **Company**, **Email**, **Customer/Supplier** status, **Created/Updated dates**
- Save filters for reuse
- Share filters with other team members
- Set a default filter that loads automatically

---

## Adding a Business Partner

1. Click **Add Business Partners** from the toolbar
2. Fill in the form:
    - **Company** — The company name (must be unique)
    - **Email** — Contact email address
    - **Customer** toggle — Mark as a customer (this automatically creates a record in the Clients table)
    - **Supplier** toggle — Mark as a supplier (this automatically creates a record in the Suppliers table)
3. Click **Submit**

!!! info "Automatic Sync"
    When you toggle **Customer** or **Supplier** on, the system automatically creates the corresponding record in the internal Clients or Suppliers tables. This ensures the partner is available across all related modules (Purchases, Tenders, etc.).

---

## Editing a Business Partner

1. Click on a partner record in the list
2. Modify any fields (company name, email, customer/supplier status)
3. Click **Submit** to save changes

---

## Deleting and Restoring

### Soft Delete
- Click the delete action on a partner record
- The partner is moved to the **Bin** (soft-deleted with a timestamp)
- It will no longer appear in the main list

### Restore
1. Click **Bin Records** from the toolbar
2. Find the deleted partner in the bin list
3. Click **Restore** to bring it back to the active list

---

## Name Groups

The **Name Group** feature allows you to organize companies under a parent name and merge duplicate entries.

### Why Use Name Groups?

Over time, the same company might be entered with slight variations (e.g., "ACME Corp", "Acme Corporation", "ACME"). Name Groups let you consolidate these into a single parent entity.

### Creating a Name Group

1. Navigate to **Business Partners > Name Group**
2. Click **New Item**
3. Enter the **Primary Name** for the group
4. Click **Submit**

### Merging Companies

1. Select multiple company names from the list
2. Choose the target **Primary Name** to merge under
3. Click **Merge**

!!! warning "Merge Effects"
    Merging updates the company name across all related tables:

    - **Business Partners** table
    - **Tenders** table (tenderer_name)
    - **Clients** table (company)
    - **Suppliers** table (company)

    Child records are created to track original names for audit purposes.

### Bin Records (Name Groups)

Deleted name groups can be viewed and restored from the Name Group bin, accessible via the **Bin Records** button.

---

## AI Enrichment

The module includes an AI-powered system that automatically enriches business partner data.

### How It Works

1. **Email Fetching** — The system connects to Microsoft Graph API and fetches emails from configured mailboxes
2. **AI Email Analysis** — Emails are analyzed by AI to extract:
    - Company name
    - Contact role
    - Contact information
    - Phone numbers
3. **Website Enrichment** — Partner websites are scraped and AI extracts:
    - Business address
    - Industry sector
    - Additional business details
4. **Auto-Sync** — New or updated partner records are created automatically

### AI Enrichment Tracking

Navigate to **Business Partners > AI Enrichment Tracking** to monitor:

| Column | Description |
|--------|-------------|
| **Partner** | The business partner being enriched |
| **Type** | Client or Supplier |
| **Status** | New, In Progress, Completed, or Failed |
| **Created At** | When the enrichment task was queued |

### AI Operation Logs

Navigate to **Business Partners > AI Operation Logs** to view the full audit trail:

| Column | Description |
|--------|-------------|
| **Operation Type** | Type of AI operation performed |
| **Partner Type** | Client or Supplier |
| **Input Data** | Data sent to AI |
| **Output Data** | AI response/results |
| **Staff** | Staff member who triggered the operation |
| **Created At** | Timestamp |

### Manual Enrichment

Administrators can manually trigger enrichment for a specific partner if needed, rather than waiting for the automated cron cycle.

---

## Activity Log

All actions on business partners are logged for audit purposes:

| Field | Description |
|-------|-------------|
| **Company** | The affected partner |
| **Action** | added, updated, deleted, or restored |
| **User** | Staff member who performed the action |
| **Date** | Timestamp of the action |

Administrators can **clear the activity log** when needed.

---

## Permissions

Access to the Business Partners module is controlled by the following permissions:

| Permission | Description |
|------------|-------------|
| **View** (Global) | View all business partners |
| **Create** | Add new business partners |
| **Edit** | Modify existing partners |
| **Delete** | Soft-delete partners |
| **Action** | Perform general actions |
| **Change Status** | Change customer/supplier status |
| **Convert** | Convert partner types |

!!! tip "Admin Access"
    Administrators have full access to all features including Bin Records for Name Groups, clearing activity logs, and AI configuration.

---

## Global Search

Business partners are included in the system-wide global search. Type a company name in the top search bar to quickly find and navigate to a business partner record.
