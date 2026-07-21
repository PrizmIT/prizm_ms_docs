# PRIZM Supplier Invoice Module

## 1. Introduction

The PRIZM Supplier Invoice module is the accounts payable hub of the PRIZM ENERGY Admin Portal. It enables finance teams, procurement officers, and project managers to record, verify, approve, and pay supplier invoices — closing the loop between purchase orders, goods receipts, and vendor payments.

Every supplier invoice starts as a billing record from a supplier and progresses through verification, approval, and payment until it is fully settled. The module enforces financial controls at each stage, maintains a complete audit trail, and integrates with procurement, projects, cost centres, and the Resource Manager to ensure accurate and timely payments.

This module is integrated with:

- Purchase Orders
- Suppliers
- Projects
- Departments & Cost Centres
- Resource Manager (Items)
- Approval Workflows
- Finance & Payments

## 2. Module Overview

The PRIZM Supplier Invoice module provides comprehensive tools for:

- Recording supplier invoices manually or from approved purchase orders
- Linking invoice line items to Resource Manager items for material tracking
- Tracking invoice status through configurable approval stages
- Monitoring payment status across the invoice lifecycle (Unpaid → Paid)
- Managing supporting documents and file attachments
- Maintaining a complete activity log for audit purposes
- Filtering and searching invoices using AG Grid with column-level filters

## 3. Navigation Structure

The Supplier Invoice module is organised as follows:

```
Prizm Purchase
├─ Grid
├─ Dashboard
├─ Expense Request
├─ Purchase Request
├─ Purchase Items Backlog
├─ Purchase Order
├─ Purchase Order Backlog
├─ Suppliers
├─ Quotations
├─ Quotation Items
├─ Received Vouchers Backlog
├─ Received Vouchers
├─ Payment Request
├─ Supplier Invoices          ← You are here
├─ Delivery Notes
├─ Delivery Notes Backlog
├─ Summary
├─ Approval Logs
└─ Settings
```

## 4. Navigation to Supplier Invoice

### How to Access

1. Log in to the PRIZM ENERGY Admin Portal using your credentials
2. From the left sidebar, expand **Prizm Purchase**
3. Click **Supplier Invoices**
4. The Supplier Invoice List page opens, displaying all invoices you have permission to view

![Supplier Invoice - Sidebar Navigation](supplier_invoice/img/sidebar_navigation.png)

!!! info "Quick Access"
    The Supplier Invoice list page is located at **Prizm Purchase → Supplier Invoices** in the sidebar navigation menu.

---

## 5. Supplier Invoice List (AG Grid)

![Supplier Invoice - AG Grid List View](supplier_invoice/img/ag_grid_list.png)

The Supplier Invoice List is the main landing page for the module. It displays all supplier invoices in a fully interactive AG Grid with server-side data loading, column-level filters, and sortable columns.

### What You See

The grid displays the following columns:

| # | Column | Description |
|---|--------|-------------|
| 1 | **Actions** | Quick-action links for each row: **View**, **Edit**, and **Delete**. |
| 2 | **#** | System-generated invoice code (e.g., SI-26070001). Clickable link that opens the invoice detail page. |
| 3 | **Supplier** | The supplier or vendor who issued the invoice. |
| 4 | **Supplier Invoice** | The supplier's own invoice number as provided on their billing document. |
| 5 | **Invoice Date** | The date the invoice was issued by the supplier. |
| 6 | **Due Date** | The payment due date for the invoice. |
| 7 | **Related PO** | The purchase order linked to this invoice, if applicable. Shows "--" if none. |
| 8 | **Project** | The project associated with this invoice, if applicable. Shows "--" if none. |
| 9 | **Grand Total** | The final invoice amount including VAT. Displayed in the invoice currency. |
| 10 | **Status** | The approval status of the invoice (e.g., Approved). Colour-coded badge. |
| 11 | **Payment Status** | The current payment state (e.g., Paid). Colour-coded badge. |

### Filters

The list page provides two levels of filtering:

**Top-Level Dropdown Filters:**

- **Supplier** — select a supplier to show only their invoices
- **Project** — filter by project association
- **Related PO** — filter by linked purchase order
- **Status** — filter by approval status

**Column-Level Filters (AG Grid):**

Each column header includes a filter icon. Click the filter icon on any column to apply text-based, date-based, or set-based filtering directly within the grid.

### Grid Controls

- **Theme** — switch between visual themes (e.g., Quartz) or toggle dark mode via **Switch to Dark**
- **Page Size** — control the number of rows displayed per page (default: 50)
- **Search** — global text search across all visible columns
- **Reset Columns** — restore default column widths and visibility

### Actions

- **+ New Supplier Invoice** — opens the invoice creation form (blue button, top of page)
- **Row Actions** — each row provides:
    - **View** — open the invoice detail page
    - **Edit** — open the invoice in edit mode
    - **Delete** — remove the invoice (subject to permissions and status)

### Pagination

The grid footer shows:
- Page size selector
- Record count (e.g., "1 to 1 of 1")
- Page navigation (first, previous, next, last)

---

## 6. Supplier Invoice Creation

![Supplier Invoice - Creation Form](supplier_invoice/img/creation_form.png)

Creating a supplier invoice records a vendor's billing document in the system. Invoices can be created manually or by linking to an existing purchase order, which can auto-populate line items.

### How to Create a Supplier Invoice

1. Navigate to **Prizm Purchase → Supplier Invoices**
2. Click **+ New Supplier Invoice**
3. Complete the form fields as described below
4. Add resource items (line items)
5. Click **Save**

### Form Fields

#### Purchase Order & Supplier Details

| # | Field Name | Required | Description |
|---|-----------|----------|-------------|
| 1 | **Purchase Order Reference** | No | Select an existing purchase order to link to this invoice. Dropdown shows available POs. |
| 2 | **Pull items from the selected PO as candidate lines** | No | Checkbox — when ticked, line items from the selected PO are automatically loaded into the invoice as candidates. |
| 3 | **Supplier** | Yes | The supplier who issued the invoice. Select from the dropdown list of registered suppliers. Marked with a red asterisk. |
| 4 | **Supplier Invoice Number** | Yes | The supplier's own invoice number as printed on their billing document. Free-text field. Marked with a red asterisk. |

#### Dates & Classification

| # | Field Name | Required | Description |
|---|-----------|----------|-------------|
| 5 | **Invoice Date** | No | The date the invoice was issued by the supplier. Date picker. |
| 6 | **Due Date** | No | The payment due date. Used for ageing reports and overdue tracking. Date picker. |
| 7 | **Currency** | No | The billing currency for this invoice. Select from configured currencies. |
| 8 | **Project** | No | Link the invoice to a specific project for cost tracking. |
| 9 | **Department** | Yes | The department responsible for this invoice. Required field. |
| 10 | **Cost Center** | No | The cost centre to which this invoice should be allocated. |

#### Financial Summary

| # | Field Name | Required | Description |
|---|-----------|----------|-------------|
| 11 | **Subtotal** | No | The total value of all line items before tax. Numeric field. |
| 12 | **VAT Amount** | No | The total VAT (Value Added Tax) amount. Numeric field. |
| 13 | **Grand Total** | No | The final invoice amount including VAT. Numeric field. |

#### Notes & Documentation

| # | Field Name | Required | Description |
|---|-----------|----------|-------------|
| 14 | **Notes** | No | General notes about the invoice. Visible to relevant staff. Multi-line text area. |
| 15 | **Internal Remarks** | No | Internal-only remarks not shared with the supplier. Multi-line text area with dropdown for formatting or templates. |
| 16 | **Attach a file** | No | Upload supporting documents such as scanned invoices, delivery receipts, or correspondence. Click **Choose File** to browse. |

### Related Resource Items

![Supplier Invoice - Resource Items Section](supplier_invoice/img/resource_items.png)

The Related Resource Items section links the invoice to items from the Resource Manager. This enables material tracking and mapping between supplier catalogue items and internal resource items.

**How to add items:**

1. In the **Search or create a Resource Item** dropdown at the bottom of the form, search for an existing resource item or create a new one
2. The item is added to the table with the following columns:

| # | Column | Description |
|---|--------|-------------|
| 1 | **Supplier Item Code** | The supplier's catalogue code for this item. |
| 2 | **Supplier Description** | The supplier's description of the item. |
| 3 | **Resource Item** | The linked PRIZM Resource Manager item. Clickable link to the item profile. |
| 4 | **Unit** | The unit of measure (e.g., Volt-Ampere, Kilogram, Piece). |
| 5 | **Qty** | The quantity being invoiced. |
| 6 | **Unit Price** | The per-unit cost. |
| 7 | **Total** | Automatically calculated: Qty × Unit Price. |
| 8 | **Mapping Status** | Shows whether the supplier item has been mapped to an internal resource item. Colour-coded badge: **Mapped** (green) or **Unmapped**. |

!!! info "Resource Item Mapping"
    Mapping supplier items to internal resource items ensures consistency across procurement, inventory, and project cost tracking. Items marked as **Mapped** are fully linked to the Resource Manager catalogue.

### Creating from a Purchase Order

When you select a **Purchase Order Reference** and tick **Pull items from the selected PO as candidate lines**:

1. The system loads line items from the selected PO into the Related Resource Items section
2. Supplier details may be pre-populated from the PO
3. You can modify quantities, prices, and descriptions to match the actual supplier invoice
4. Additional items can be added manually

!!! warning "Important"
    Verify that the auto-populated line items match the supplier's actual invoice before saving. Discrepancies should be investigated with the procurement team.

---

## 7. Supplier Invoice Statuses & Workflow

![Supplier Invoice - Status Workflow](supplier_invoice/img/status_workflow.png)

The Supplier Invoice module tracks two distinct status dimensions: the **Approval Status** and the **Payment Status**.

### Approval Status

The approval status tracks whether the invoice has been reviewed and authorised through the configured approval workflow.

| Status | Description |
|--------|-------------|
| **Pending** | The invoice has been created and is awaiting approval. |
| **Approved** | The invoice has been reviewed and approved by all required approvers. |
| **Rejected** | The invoice has been rejected by an approver. A reason may be provided. |

### Payment Status

The payment status tracks the financial settlement of the invoice.

| Status | Colour | Description |
|--------|--------|-------------|
| **Unpaid** | — | No payments have been recorded or approved against this invoice. |
| **Paid** | Green | The invoice has been fully settled. |

### Typical Invoice Lifecycle

```
Invoice Created (Pending Approval)
    ↓
Submitted for Approval
    ↓
Approved by designated approver(s)
    ↓
Payment Processed
    ↓
Paid (fully settled)
```

### Undo Paid

If a payment needs to be reversed, authorised users can click the **Undo Paid** button on the invoice detail page. This resets the payment status and allows corrections to be made.

---

## 8. Supplier Invoice Details View

![Supplier Invoice - Detail View](supplier_invoice/img/detail_view.png)

The detail page provides a comprehensive view of a single supplier invoice, organised into tabs.

### Header Information

At the top of the detail page, you see:

- **Invoice Code** — system-generated identifier (e.g., SI-26070001)
- **Approval Status Badge** — colour-coded (e.g., "Approved" in green)
- **Payment Status Badge** — colour-coded (e.g., "Paid" in blue)
- **Undo Paid** button — allows reversing the payment status (visible when paid)

### Invoice Summary Fields

| Field | Description |
|-------|-------------|
| **Supplier** | The supplier name, clickable link to the supplier profile. |
| **Supplier Invoice Number** | The vendor's own invoice reference. |
| **Invoice Date** | The date the invoice was issued. |
| **Due Date** | The payment due date. |
| **Related PO** | The linked purchase order (or "--" if none). |
| **Project** | The associated project (or "--" if none). |
| **Cost Center** | The allocated cost centre (or "--" if none). |
| **Currency** | The invoice currency (or "--" for default). |

### Financial Summary

- **Subtotal** — sum of all line items before tax
- **VAT** — total VAT amount
- **Grand Total** — final amount including VAT
- **Payment Status** — current payment state with colour-coded badge

### Related Resource Items Table

The detail view displays all line items in a table:

| Column | Description |
|--------|-------------|
| **Supplier Item Code** | Supplier's catalogue reference |
| **Supplier Description** | Supplier's description of the goods or service |
| **Resource Item** | Linked internal resource item (clickable link to Resource Manager) |
| **Unit** | Unit of measure |
| **Qty** | Quantity invoiced |
| **Unit Price** | Per-unit cost |
| **Total** | Line total (Qty × Unit Price) |
| **Mapping Status** | Whether the item is mapped to an internal resource item (green "Mapped" badge) |

### Approver & Stages Info

Below the line items, the **Approver And Stages Info** section shows:

- The approval stage configuration
- Each approver's name, decision (Approved/Rejected), and timestamp
- This provides a complete audit trail of who approved the invoice and when

### Tabs

The detail view has three tabs:

#### Tab 1: Info

The default tab showing the full invoice summary, line items, financial totals, and approval history as described above.

#### Tab 2: Attachment

Upload and manage supporting documents:

- Scanned copies of the supplier's original invoice
- Delivery receipts or goods receipt vouchers
- Purchase order confirmations
- Correspondence and supporting documentation

Files can be uploaded, previewed, and downloaded from this tab.

#### Tab 3: Activity Log

A chronological record of all actions performed on this invoice:

- Creation events
- Status changes
- Edits and updates
- Approval decisions
- Payment events
- File uploads

Each entry is timestamped and attributed to the user who performed the action, providing a complete audit trail.

---

## 9. Line Items Management

### Adding Resource Items

1. On the invoice creation or edit form, locate the **Related Resource Items** section
2. Use the **Search or create a Resource Item** dropdown to find an existing item from the Resource Manager
3. Enter the supplier item code, description, quantity, unit price, and unit
4. The system automatically calculates the line total
5. The mapping status indicates whether the supplier item is linked to an internal resource item

### Auto-Population from Purchase Order

When a purchase order is selected and **Pull items from the selected PO as candidate lines** is ticked:

- PO line items are loaded into the Related Resource Items section
- Item codes, descriptions, quantities, and prices are inherited from the PO
- You can adjust any field to reflect the actual supplier invoice
- Additional items can be added manually

### Mapping Status

Each line item shows a **Mapping Status**:

- **Mapped** (green badge) — the supplier's item has been linked to a corresponding item in the PRIZM Resource Manager. This enables unified tracking across procurement, inventory, and project costing.
- **Unmapped** — the supplier's item has not yet been linked to an internal resource item. Consider mapping it for better traceability.

---

## 10. Three-Way Matching (PO / Delivery / Invoice)

Three-way matching is a core accounts payable control that ensures the amounts billed by a supplier are consistent with what was ordered and what was received.

### The Three Documents

| Document | Source | What It Confirms |
|----------|--------|-----------------|
| **Purchase Order** | Procurement team | What was ordered: items, quantities, agreed prices |
| **Received Voucher** | Warehouse / receiving team | What was actually received: items and quantities delivered |
| **Supplier Invoice** | Supplier | What the supplier is billing: items, quantities, prices |

### How Matching Works in PRIZM

1. **Link the invoice to a Purchase Order** — when creating the invoice, select the PO reference and tick the checkbox to pull PO items
2. **Compare against received vouchers** — verify that the quantities invoiced match the quantities received (available in the **Received Vouchers** section under Prizm Purchase)
3. **Investigate discrepancies** — if the invoice amounts differ from the PO or delivery:
    - Check for partial deliveries
    - Check for price changes or surcharges
    - Contact the supplier or procurement team to resolve differences
4. **Submit for approval** — once verified, the invoice proceeds through the approval workflow

!!! warning "Best Practice"
    Never approve an invoice for payment without confirming that the billed items and amounts match both the purchase order and the received voucher. This prevents overpayment and fraud.

---

## 11. Approval Workflow

![Supplier Invoice - Approval Workflow](supplier_invoice/img/approval_workflow.png)

The Supplier Invoice module supports a configurable approval workflow. This ensures that invoices are reviewed and authorised before payment is processed.

### How Approval Works

1. A user creates a supplier invoice and saves it
2. The invoice enters **Pending** approval status
3. Designated approvers are notified
4. Each approver reviews the invoice details, line items, and supporting documents
5. The approver either **Approves** or **Rejects** the invoice
6. Once all required approvals are obtained, the status changes to **Approved**
7. Approved invoices can proceed to payment processing

### Approval Stages

The system supports multi-stage approval:

- Each stage can have one or more designated approvers
- Stages must be completed in sequence
- The **Approver And Stages Info** section on the invoice detail page shows:
    - Stage number and title
    - Approver name
    - Decision (Approved/Rejected)
    - Date and time of the decision

### Rejection and Re-Submission

When an invoice is rejected:

- The rejection reason is recorded in the approval history
- The invoice creator is notified
- The invoice can be edited and re-submitted for approval
- The original rejection remains in the audit trail

---

## 12. Payment Processing

### Recording Payment

Once an invoice is approved, payment can be processed. The payment status is tracked on the invoice and displayed as a colour-coded badge.

### Payment Status Indicators

| Status | Badge Colour | Meaning |
|--------|-------------|---------|
| **Unpaid** | — | No payment has been recorded |
| **Paid** | Green/Blue | The invoice has been fully settled |

### Undo Paid

If a payment was recorded in error or needs to be reversed:

1. Open the invoice detail page
2. Click the **Undo Paid** button (top right corner)
3. The payment status is reset
4. Corrections can be made before re-processing the payment

!!! info "Payment Integration"
    Payment processing may also be managed through the **Payment Request** module under Prizm Purchase, which provides additional approval workflows for payment disbursement.

---

## 13. Attachments & Documents

### Uploading Attachments

**During creation:**
1. On the creation form, click **Choose File** in the **Attach a file** section
2. Select the file from your device
3. The file is attached when the invoice is saved

**On an existing invoice:**
1. Open the invoice detail page
2. Click the **Attachment** tab
3. Upload files using the upload control

### Recommended Documents to Attach

- Scanned copy of the supplier's original invoice
- Delivery receipt or goods receipt voucher
- Purchase order confirmation
- Correspondence regarding pricing or discrepancies
- Approval or authorisation documentation

---

## 14. Activity Log & Audit Trail

The **Activity Log** tab on the invoice detail page maintains a comprehensive, chronological record of all actions performed on the invoice.

### What Is Tracked

- Invoice creation (who created it and when)
- Field modifications (what was changed, by whom)
- Status transitions (pending → approved, approved → paid)
- Approval decisions (approver name, decision, timestamp)
- Payment events
- File uploads and deletions
- Any other system-generated events

### How to Access

1. Open any supplier invoice detail page
2. Click the **Activity Log** tab
3. Review the chronological list of events

Each entry includes:
- **Timestamp** — exact date and time of the action
- **User** — the staff member who performed the action
- **Action** — description of what was done

---

## 15. Reports & Analytics

### Invoice Data in Reports

Supplier invoice data is available across several reporting dimensions:

- **By Supplier** — view all invoices for a specific supplier from the supplier profile page
- **By Purchase Order** — see invoices linked to a specific PO
- **By Project** — track invoices against a project
- **By Status** — use the Status filter on the list page to see Pending, Approved, or Rejected invoices
- **By Payment** — use the Payment filter to see Paid or Unpaid invoices
- **By Date Range** — use the Due Date column filter to analyse invoices for a specific period

### Export Options

- Use AG Grid's built-in features to sort and filter data for analysis
- Individual invoice details can be printed or saved from the detail view

### Summary View

The **Summary** page under Prizm Purchase provides aggregated procurement data including supplier invoice totals.

### Approval Logs

The **Approval Logs** page under Prizm Purchase tracks all approval decisions across purchase requests, purchase orders, and supplier invoices.

---

## 16. Integration with Other Modules

The Supplier Invoice module connects with several other PRIZM modules to provide end-to-end procurement and financial management.

### Purchase Orders

- Invoices can be created directly from a purchase order by selecting the PO reference
- Line items can be auto-populated from the PO using the checkbox option
- PO references appear on the invoice list and detail pages

### Suppliers

- Every invoice is linked to a registered supplier
- Supplier selection determines available purchase orders
- The supplier name links to the supplier profile for full vendor details

### Resource Manager (Items)

- Invoice line items link to Resource Manager items
- **Mapping Status** tracks whether supplier items are linked to internal catalogue items
- This enables unified material tracking across procurement, inventory, and project costing

### Projects

- Invoices can be linked to projects for cost tracking
- Project managers can filter invoices by project

### Departments & Cost Centres

- Each invoice is assigned to a department (required field)
- Invoices can be allocated to specific cost centres for granular financial tracking

### Received Vouchers

- Received vouchers (goods receipt records) are available under Prizm Purchase
- Use them alongside the invoice and PO for three-way matching

### Payment Requests

- Payment requests under Prizm Purchase provide an additional approval workflow for payment disbursement
- Invoices and payment requests work together to manage the full payment cycle

### Approval Workflows

- Configurable multi-stage approval ensures invoices are reviewed before payment
- Approval logs provide a centralised audit trail across all purchase module documents

---

## 17. Permissions & Roles

Access to the Supplier Invoice module is controlled through the PRIZM role-based permission system.

### Typical Permission Levels

| Permission | Description |
|-----------|-------------|
| **View** | See all supplier invoices in the system |
| **View Own** | See only invoices you created |
| **Create** | Create new supplier invoices |
| **Edit** | Modify existing invoices |
| **Delete** | Remove invoices from the system |

### Typical Role Assignments

| Role | Typical Permissions |
|------|-------------------|
| **Finance / AP Clerk** | View, Create, Edit |
| **Finance Manager** | View, Create, Edit, Delete + Approval authority |
| **Procurement Officer** | View, Create |
| **Project Manager** | View (filtered by project) |
| **System Administrator** | All permissions |

!!! info "Approval Permissions"
    Approval authority is configured separately through the approval workflow settings. A user may have permission to create invoices but not to approve them.

---

## 18. Common Scenarios

### Scenario 1: Recording an Invoice from a Purchase Order

**Situation:** A supplier delivers goods against an approved purchase order and sends their invoice.

1. Navigate to **Prizm Purchase → Supplier Invoices**
2. Click **+ New Supplier Invoice**
3. Select the **Purchase Order Reference** from the dropdown
4. Tick **Pull items from the selected PO as candidate lines**
5. Select the **Supplier** (may auto-populate from the PO)
6. Enter the **Supplier Invoice Number** from the vendor's document
7. Set the **Invoice Date** and **Due Date**
8. Select the **Department** (required)
9. Verify that line items, quantities, and prices match the supplier's invoice
10. Upload a scanned copy of the supplier's invoice using **Attach a file**
11. Click **Save**

### Scenario 2: Creating a Manual Invoice (No PO)

**Situation:** A supplier provides a service not covered by a purchase order (e.g., emergency repair).

1. Click **+ New Supplier Invoice**
2. Leave **Purchase Order Reference** as "-- none --"
3. Select the **Supplier** from the dropdown
4. Enter the **Supplier Invoice Number**
5. Set the **Invoice Date**, **Due Date**, and **Department**
6. Optionally link to a **Project** and **Cost Center**
7. Enter **Subtotal**, **VAT Amount**, and **Grand Total**
8. Add resource items in the **Related Resource Items** section
9. Add any **Notes** or **Internal Remarks**
10. Attach supporting documents
11. Click **Save**

### Scenario 3: Approving an Invoice

**Situation:** An invoice has been submitted and requires your approval.

1. Open the invoice from the list (filter by Status = Pending if needed)
2. Review the invoice details on the **Info** tab:
    - Verify supplier, amounts, and linked PO
    - Check the resource items against the delivery records
    - Review any attached documents on the **Attachment** tab
3. In the **Approver And Stages Info** section, click **Approve** or **Reject**
4. If rejecting, provide a reason for the rejection
5. The invoice status updates accordingly

### Scenario 4: Handling a Discrepancy

**Situation:** A supplier's invoice shows a higher quantity or price than what was ordered.

1. Open the invoice and compare line items against the linked purchase order
2. Check received vouchers to confirm what was actually delivered
3. Add an internal remark documenting the discrepancy via the **Internal Remarks** field
4. Reject the invoice with a clear reason if the discrepancy cannot be resolved
5. Contact the supplier to request a corrected invoice or credit note
6. Once resolved, create a new invoice with the correct details

---

## 19. Best Practices & Tips

### For Finance Teams

- **Always verify before approving** — check that the invoice matches the PO and received voucher before approving
- **Use the Supplier Invoice Number** — enter the supplier's own invoice number for easy cross-referencing during audits
- **Attach source documents** — upload the supplier's original invoice and delivery receipt for a complete audit trail
- **Monitor due dates** — use the Due Date column filter to track approaching payment deadlines
- **Use Internal Remarks** — record internal observations and decisions separately from supplier-facing notes

### For Procurement Officers

- **Link invoices to POs** — always select the purchase order reference when creating an invoice to enable three-way matching
- **Check mapping status** — ensure resource items are mapped to internal catalogue items for accurate material tracking
- **Pull PO items** — use the checkbox to auto-populate line items from the PO to reduce manual data entry

### For Approvers

- **Review all tabs** — check the Info tab for details, the Attachment tab for supporting documents, and the Activity Log for history
- **Provide rejection reasons** — when rejecting an invoice, always include a clear reason so the submitter knows what to correct
- **Verify the approval stage** — check the Approver And Stages Info section to understand where the invoice is in the approval workflow

### For System Administrators

- **Configure approval workflows** — set up appropriate approval stages and designate approvers for your organisation
- **Manage suppliers** — ensure the supplier register is up to date so users can correctly link invoices
- **Review approval logs** — use the Approval Logs page under Prizm Purchase for a centralised audit view

---

## 20. Known Limitations & Notes

- **AG Grid features** — the Supplier Invoice list uses AG Grid with server-side data loading. Column filters, sorting, and pagination are fully supported. Saved filter presets may depend on module configuration.
- **Department is required** — every supplier invoice must be assigned to a department. Ensure departments are configured before creating invoices.
- **Resource item mapping** — items that show as "Unmapped" in the mapping status column have not been linked to the internal Resource Manager catalogue. While invoices can be saved with unmapped items, mapping is recommended for complete traceability.
- **Undo Paid** — the Undo Paid action is available only to authorised users and is logged in the activity trail. Use with caution as it affects financial records.
- **File attachments** — files are uploaded during creation via the Attach a file field, and on existing invoices via the Attachment tab. Ensure file sizes comply with system upload limits.
- **Approval stage visibility** — the Approver And Stages Info section is visible on the detail page only after the invoice has entered the approval workflow.
