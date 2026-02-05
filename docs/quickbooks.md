# PRIZM QuickBooks Integration – User Guide

## 1. Overview

![Overview](quickbooks/img/overview.png)

The **QuickBooks Integration** module connects PRIZM ENERGY ERP with QuickBooks to ensure accurate, consistent, and auditable financial records across both systems. It enables controlled synchronization of accounting data while clearly defining system ownership, approval boundaries, and compliance traceability.

This integration is designed to support finance operations, audits, and management reporting without exposing technical or implementation‑specific details.

**Key objectives include:**

- Eliminating duplicate data entry
- Ensuring accounting accuracy and reconciliation
- Maintaining a clear system of record
- Supporting audit and compliance requirements
- Providing visibility into synchronization health and errors

## 2. Navigation to QuickBooks Integration

![Navigation to QuickBooks Integration](quickbooks/img/navigation.png)

The QuickBooks Integration module is accessible from the PRIZM ENERGY Admin Portal main navigation.

**Typical access path:**
`Admin Portal → Finance / Accounting → QuickBooks Integration`

Access visibility depends on assigned roles and permissions.

## 3. QuickBooks Integration Dashboard

![QuickBooks Integration Dashboard](quickbooks/img/dashboard.png)

The dashboard provides a high‑level overview of integration health and financial synchronization status.

### What Users See
- Overall connection status
- Summary of synced vs pending records
- Recent sync activity
- Error and warning indicators
- Last successful synchronization timestamp

### Available Actions
- Navigate to detailed sync views
- Initiate manual synchronization
- Review recent errors
- Access reconciliation and audit reports

### Why It Matters
The dashboard acts as a financial control center, allowing finance teams to quickly assess whether accounting data is aligned and ready for reporting or closing activities.

## 4. Connection & Authorization

![Connection & Authorization](quickbooks/img/connection.png)

This screen manages the secure authorization between PRIZM ENERGY ERP and QuickBooks.

### What Users See
- Current connection status
- Authorization state
- Connection validity indicators

### Available Actions
- Initiate or renew authorization
- Disconnect integration (with safeguards)
- Validate connection health

### Governance Considerations
- Authorization changes are logged for audit purposes
- Disconnecting does not delete historical accounting records
- Only authorized roles can manage connections

## 5. Sync Configuration & Settings

![Sync Configuration & Settings](quickbooks/img/settings.png)

This section defines how and when data synchronization occurs.

### Configuration Options
- One‑way or two‑way synchronization (where applicable)
- Manual vs scheduled synchronization
- Entity‑level sync enablement
- Default accounting behaviors

### Validation Rules
- Required accounting data must be present before sync
- Currency and tax configurations must be consistent
- Locked financial periods are respected

### Financial Impact
Proper configuration ensures accurate postings, prevents premature data transfer, and protects closed accounting periods.

## 6. Account & Data Mapping

![Account & Data Mapping](quickbooks/img/mapping.png)

Account and data mapping ensures that PRIZM financial structures align correctly with QuickBooks.

### What Is Mapped
- Customers and vendors
- Income and expense classifications
- Tax treatments
- Payment methods

### Key Rules
- Mandatory mappings must be completed before sync
- One‑to‑one mapping is enforced to prevent ambiguity
- Changes to mappings are logged and versioned

### Why It Matters
Correct mapping is critical to ensure financial statements remain accurate and compliant in both systems.

## 7. Customer & Vendor Synchronization

![Customer & Vendor Synchronization](quickbooks/img/customer_vendor_sync.png)

This view manages the synchronization of business partners.

### Supported Entities
- Customers
- Vendors / Suppliers

### Sync Behavior
- New records are validated before sync
- Existing records are matched to prevent duplicates
- Updates follow ownership rules

### Controls
- Manual sync per record
- Status indicators
- Error feedback for incomplete data

## 8. Invoice, Bill & Expense Synchronization

![Invoice, Bill & Expense Synchronization](quickbooks/img/invoice_sync.png)

This screen handles transactional financial documents.

### Supported Transactions
- Sales invoices
- Vendor bills
- Operational expenses

### Eligibility Rules
- Approved status required
- Complete accounting data
- Valid dates and amounts

### Locking Rules
- Synced documents are locked against financial edits
- Corrections require controlled adjustment workflows

### Accounting Impact
Ensures that operational transactions are accurately reflected in financial statements.

## 9. Payment & Credit Handling

![Payment & Credit Handling](quickbooks/img/payment_sync.png)

This section manages the synchronization of financial settlements.

### Supported Items
- Customer payments
- Vendor payments
- Credits and adjustments (where applicable)

### Key Behaviors
- Payments are linked to original documents
- Partial payments are supported
- Credits follow strict validation rules

### Compliance Notes
All payment‑related syncs maintain full traceability for audit review.

## 10. Sync Statuses & Lifecycle

![Sync Statuses & Lifecycle](quickbooks/img/lifecycle.png)

Every synchronized record follows a defined lifecycle.

### Common Statuses

| Status | Description |
| :--- | :--- |
| **Not Synced** | Eligible but not yet processed |
| **Queued for Sync** | Awaiting processing |
| **Successfully Synced** | Completed without issues |
| **Partially Synced** | Some components failed |
| **Sync Failed** | Requires review |
| **Manually Overridden** | Adjusted by authorized user |

### Lifecycle Rules
- Status changes are timestamped
- User‑initiated actions are distinguished from system actions
- Locked statuses protect accounting integrity

## 11. Manual Sync & Retry Operations

![Manual Sync & Retry Operations](quickbooks/img/manual_sync.png)

Manual controls allow intervention when automation is insufficient.

### Available Actions
- Trigger sync for selected records
- Retry failed syncs
- Revalidate data before retry

### Usage Scenarios
- Correcting validation issues
- Handling exceptional transactions
- Supporting period‑end reconciliation

## 12. Error Handling & Troubleshooting

![Error Handling & Troubleshooting](quickbooks/img/errors.png)

This screen provides visibility into integration issues.

### What Users See
- Error messages in business language
- Affected records
- Suggested corrective actions

### Error Handling Principles
- No silent failures
- Errors do not delete data
- Historical errors are retained for review

## 13. Reconciliation & Audit Reports

![Reconciliation & Audit Reports](quickbooks/img/reports.png)

Designed for finance teams and auditors.

### Available Reports
- Sync history by entity
- Mismatch and exception reports
- User vs system‑initiated activity
- Period‑based reconciliation summaries

### Audit Value
Supports internal controls, external audits, and regulatory compliance.

## 14. Integration with Other PRIZM Modules

![Integration with Other PRIZM Modules](quickbooks/img/integration.png)

QuickBooks Integration works in coordination with other PRIZM modules, including:

- Projects
- Expenses
- Procurement
- Sales and billing
- Budget and cost control

Data flows respect ownership boundaries and approval workflows across modules.

## 15. Permissions & Roles

![Permissions & Roles](quickbooks/img/roles.png)

Access is role‑based.

### Typical Roles
- Finance Manager
- Accountant
- ERP Administrator
- Auditor (read‑only)

### Permission Controls
- Connection management
- Sync execution
- Override and retry actions
- Audit access

## 16. Common Accounting Scenarios

![Common Accounting Scenarios](quickbooks/img/scenarios.png)

### Period‑End Close
- Ensure all eligible records are synced
- Review error logs
- Run reconciliation reports

### Data Correction
- Adjust in owning system
- Retry sync
- Document override if required

### Audit Review
- Export sync history
- Validate timestamps and user actions

## 17. Best Practices & Tips

![Best Practices & Tips](quickbooks/img/best_practices.png)

- Complete mappings before enabling sync
- Avoid edits after synchronization
- Regularly review dashboard health indicators
- Use manual sync sparingly and with documentation
- Align sync schedules with accounting periods

## 18. Known Limitations / Notes

![Known Limitations / Notes](quickbooks/img/notes.png)

- Historical records remain immutable after sync
- Closed accounting periods cannot be altered
- Some configuration changes require revalidation
- Integration behavior follows accounting governance rules, not operational convenience

---
