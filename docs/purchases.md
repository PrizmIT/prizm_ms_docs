# Purchases

## 1. Introduction

The Prizm Purchase module is the core procurement system within the Prizm Management System. It manages the complete purchasing lifecycle, starting from internal demand initiation (Purchase Requests / Expense Requests) through supplier engagement, ordering, delivery, invoicing, and payment tracking.

This module is integrated with:

- Projects
- Departments
- Cost Centers
- Suppliers
- Budget & Expense systems
- Approval workflows
- Payment tracking

## 2. Module Overview

The Prizm Purchase module provides comprehensive tools for:

- Creating and managing purchase requests
- Processing expense requests
- Generating and tracking purchase orders
- Managing supplier relationships
- Recording deliveries and receipts
- Processing payment requests
- Maintaining approval logs and audit trails

## 3. Navigation Structure

The Prizm Purchase module is organized as follows:

```
Prizm Purchase
├─ Grid
├─ Dashboard
├─ Purchase Request
├─ Expense Request
├─ Purchase Items Backlog
├─ Purchase Order
├─ Purchase Order Backlog
├─ Suppliers
├─ Quotations
├─ Quotation Items
├─ Received Vouchers
├─ Received Vouchers Backlog
├─ Payment Request
├─ Delivery Notes
├─ Delivery Notes Backlog
├─ Summary
├─ Approval Logs
└─ Settings
```

## 4. Dashboard

### Purpose

Provides a real-time overview of procurement activity.

![Purchases Dashboard](purchases/img/dashboard_purchases.png)

### Key Elements

- Total Purchase Requests by status
- Purchase Orders (Draft / Submitted / Approved)
- Pending Payments
- Undelivered Orders

### Available Filters

- Department
- Project
- Supplier

### Benefits

- Immediate operational visibility
- Useful for management oversight
- Quick access to key metrics

## 5. Purchase Requests (PR)

### 5.1 Overview

Purchase Requests are used to formally request goods or services internally before engaging with suppliers. This is the starting point of the procurement process.

![Purchase Request Summary](purchases/img/purchase_request_summary.PNG)

The Purchase Request screen provides a comprehensive overview with:

- **Summary Statistics**: Quick view of requests by status (Draft, Approved, Rejected, Submitted, Expired)
- **Filter Options**: Department, Project, Cost Center, Next Action By, and Date filters
- **Request List**: Detailed table showing PR#, Title, Requester, Next Action, Department, Cost Center, Total Cost, Request Date, and Status
- **Action Buttons**: Create new purchase requests and manage bin records
- **Active/General Toggle**: Switch between active and general requests

### 5.2 Creating a Purchase Request

![Create Purchase Request](purchases/img/create_prs.png)

**Field Guide:**

1. **Title** - Name/subject of the purchase request (required)
2. **Department** - Requesting department (required)
3. **Request Type** - Material or Service (required)
4. **Currency** - Transaction currency (required)
5. **Cost Centers** - Budget allocation category (required)
6. **Quotation** - Link to existing quotation
7. **Related To** - Link to project or entity
8. **Items Table** - Line items with specifications and pricing

**Required Information:**

- Purchase Request Code (auto-generated or manual)
- Request Name
- Department
- Project (optional but recommended)
- Cost Center (mandatory if enabled)
- Currency
- Request Type (Material / Service)
- Notes

![Attachments](purchases/img/attachments_prs.png)

**Item Details:**

- Item Name
- Specification
- Quantity
- Unit Price
- Tax
- Subtotal (auto-calculated)

**Comparison Sheet:**

![Comparison Sheet](purchases/img/comparison_sheet_prs.png)

### 5.3 Approval Workflow

```
Draft
 → Submitted
   → Approved
     → Converted to Purchase Order
   → Rejected → Can be Resubmitted
```

![View Purchase Request (Submitted)](purchases/img/view_prs.png)

### 5.4 Status Types

- **Draft** - Initial creation, not yet submitted
- **Submitted** - Awaiting approval
- **Approved** - Ready to convert to Purchase Order
- **Rejected** - Requires revision

### 5.5 Bin Records (Deleted PRs)

The **Bin Records** area stores purchase requests that have been deleted from the main list.

![Deleted Purchase Requests](purchases/img/deleted_prs.png)

**Actions:**

- **View**: Open the deleted request to check details.
- **Delete Permanently**: Remove the request from the system entirely. This cannot be undone.

### 5.6 Activity Log

![Activity Log](purchases/img/activitylog_prs.png)

### 5.7 Best Practices

- Provide detailed item specifications
- Link to appropriate projects and cost centers
- Ensure budget availability before submission
- Use clear and descriptive request names

## 6. Expense Requests (ER)

### Purpose

Expense Requests are used for:

![Expense Request Overview](purchases/img/expense_request_overview.png)

- Operational expenses
- Employee reimbursements
- Advance cash reconciliation

### Key Features

- Item-level expense tracking
- Multi-level approval workflow
- Status tracking
- Budget validation
- Link to advance cash records

### Creating an Expense Request

![Create Expense Request](purchases/img/create_expense_request.png)

**Field Guide:**

1. **Title** - Expense description (required)
2. **Department** - Requesting department (required)
3. **Currency** - Transaction currency (required)
4. **Discount Type** - Discount calculation method
5. **Cost Centers** - Budget allocation category (required)
6. **Related To** - Link to project or entity
7. **Items Table** - Expense line items with pricing

### Budget Validation

The system prevents submission if expenses exceed available funds, ensuring financial control and compliance with budget limits.

### Approval Process

Expense requests follow a strict approval workflow to ensure proper authorization before payment processing.

![View Expense Request](purchases/img/view_expense_request.png)
![View Expense Request Details](purchases/img/view_expense_request_2.png)

### Bin Records (Deleted ERs)

![Expense Request Bin](purchases/img/expense_request_bin.png)

## 7. Purchase Items Backlog

### Purpose

The Purchase Items Backlog acts as a staging area between approved Purchase Requests and Purchase Orders.

![Backlog PRs for PO](purchases/img/backlog_prs_for_PO.png)

### How It Works

- Displays approved Purchase Request items not yet ordered
- Allows grouping multiple items into a single Purchase Order
- Prevents duplicate ordering
- Provides a control point for procurement

### Benefits

- Better control over procurement
- Prevents items from falling through the cracks
- Enables bulk ordering for efficiency

## 8. Purchase Orders (PO)

![Purchase Orders Overview](purchases/img/PO_overview_list.png)

### 8.1 Creating Purchase Orders

![Create Purchase Order](purchases/img/create_po.png)

**Field Guide:**

1. **Title** - PO description (required)
2. **Currency** - Transaction currency (required)
3. **Supplier** - Vendor selection (required)
4. **Delivery Date** - Expected delivery date
5. **Department** - Requesting department (required)
6. **Delivery Location** - Goods delivery address
7. **Request Type** - Material or Service (required)
8. **Related To** - Link to project or entity
9. **Items Table** - Line items from purchase request

Purchase Orders are created from items in the backlog.

**Required Information:**

- PO Number
- Supplier
- Department
- Project
- Currency
- Discount (if applicable)
- Delivery Location

### Viewing and Editing Purchase Orders

![Edit PO](purchases/img/edit_po_1.png)
![Edit PO Details](purchases/img/edit_po_2.png)

### Reviewing Draft PO

![Draft PO View](purchases/img/view_po_draft_1.png)
![Draft PO Details](purchases/img/view_po_draft_2.png)

### 8.2 Status Flow

```
Draft → Submitted → Approved → Partially Delivered → Completed → Paid
```

### 8.3 Key Features

- Direct linkage to original Purchase Requests
- Supplier-specific information
- Accurate financial calculations
- Delivery tracking
- Payment status monitoring

### 8.4 Best Practices

- Verify supplier information before submission
- Double-check pricing and quantities
- Include clear delivery instructions
- Maintain communication with suppliers

### Bin Records (Deleted POs)

![Deleted Purchase Orders](purchases/img/deleted_pos.png)

## 9. Suppliers

### 9.1 Supplier Overview

![Suppliers List](purchases/img/suppliers_list.png)

### Purpose

Maintain a comprehensive database of vendors and suppliers.

### 9.2 Adding Suppliers

**Individual Entry:**
![Add Supplier Step 1](purchases/img/add_supplier_1.png)

**Field Guide (Step 1):**

1. **Company** - Supplier company name (required)
2. **Vat Number** - Tax registration number
3. **Phone** - Contact phone number
4. **Supply Domain** - Business domain (required)
5. **Supplier Speciality** - Area of expertise
6. **Supplier Category** - Supplier classification
7. **Currency** - Default transaction currency

![Add Supplier Step 2](purchases/img/add_supplier_2.png)

**Field Guide (Step 2):**

1. **Address** - Street address
2. **City** - City name
3. **State** - State or province
4. **Zip Code** - Postal code
5. **Country** - Country selection
![Adding Supplier Notes](purchases/img/add_supplier_notes.png)
![Add Note Modal](purchases/img/supplier_note_add.png)

**Batch Import:**
![Batch Add Suppliers](purchases/img/supplier_batch_add.png)

### 9.3 Supplier Groups

Manage parent companies and diverse supplier groups efficiently.

![Parent Supplier Group](purchases/img/parent_supplier_for_group.png)
![Supplier Group Duplication Check](purchases/img/supplier_group_duplication.png)

### 9.4 Contact Management

Manage specific contacts for each supplier.

![Supplier Contacts List](purchases/img/supplier_contacts_list.png)
![Specific Supplier Contacts](purchases/img/supplier_contacts_specific_supplier.png)

**Adding Contacts:**
![Add Contact Modal 1](purchases/img/add_supplier_contact_modal_1.png)

**Field Guide:**

1. **Firstname** - Contact first name (required)
2. **Lastname** - Contact last name (required)
3. **Position** - Job title or role
4. **Email** - Contact email address (required)
5. **Phone Number** - Contact phone
6. **Primary Contact** - Mark as primary contact for supplier

![Add Contact Modal 2](purchases/img/add_supplier_contact_modal_2.png)
![Create Contact 1](purchases/img/supplier_contact_create_1.png)
![Create Contact 2](purchases/img/supplier_contact_create_2.png)

### Key Information

- Supplier master data
- Contact details
- Active / Inactive status
- Contact management
- Payment terms

### Usage

- Select suppliers for Purchase Orders
- Track supplier performance
- Manage supplier relationships
- Maintain updated contact information

![Supplier Statistics](purchases/img/supplier_statistics.png)

## 10. Quotations & RFQs

### 10.1 Overview

Quotations are formal price offers from suppliers in response to Requests for Quotation (RFQs).

![RFQ List](purchases/img/supplier_rfq_list.png)
![Quotations List](purchases/img/quotation_list.png)
![Quotations Express View](purchases/img/quotation_list_express_view.png)
![Quotation Main View](purchases/img/quotation_main_view.png)

### 10.2 Creating Quotations

![Create Quotation 1](purchases/img/create_quotation_1.png)

**Field Guide (Part 1):**

1. **Supplier** - Vendor selection
2. **Currency** - Transaction currency (required)
3. **Reference #** - External reference number
4. **Discount Type** - Discount calculation method
5. **Quotation Number** - Auto-generated quotation code (required)
6. **Supplier Reference** - Vendor's reference number
7. **Date** - Quotation date (required)
8. **Expiry Date** - Quotation validity period
9. **Related To** - Link to project or entity

![Create Quotation 2](purchases/img/create_quotation_2.png)

**Field Guide (Part 2):**

1. **Items Table** - Line items with description, specs, quantity, rate, tax
2. **Discount** - Discount amount or percentage
3. **Adjustment** - Price adjustment value
4. **Quotation Note** - Additional notes for supplier
5. **Terms & Conditions** - Legal terms and conditions

### 10.3 Managing Items

Items can be entered manually or converted from RFQs.

![Converted Items](purchases/img/quotation_items_converted_from_rfq_tab.png)
![Manual Items](purchases/img/quotation_items_entered_manually.png)

### 10.4 Editing & Attachments

![Edit Quotation 1](purchases/img/quotation_edit_1.png)
![Edit Quotation 2](purchases/img/quotation_edit_2.png)
![Attachments](purchases/img/quotation_attachments_view.png)

### Process

1. Send RFQs to multiple suppliers
2. Receive and record quotations
3. Compare supplier offers
4. Select best quotation
5. Use selected pricing for Purchase Orders

### Benefits

- Competitive pricing
- Multiple supplier options
- Documented decision-making
- Better negotiation position

## 11. Received Vouchers

### Purpose

Received Vouchers (Goods Receipt Notes) record goods and services received against Purchase Orders.

![Add Received Voucher](purchases/img/receive_voutcher_add.png)

**Field Guide:**

1. **Voucher Date** - Date of the voucher
2. **Received Date** - Actual goods receipt date
3. **Project** - Related project
4. **Purchase Order** - Linked purchase order
5. **Supplier** - Vendor name
6. **Department** - Receiving department
7. **Cost Centers** - Budget allocation category
8. **Items Table** - Received items with quantities

### Key Features

- Partial receipts allowed
- Updates remaining Purchase Order quantities
- Links to Delivery Notes
- Prepares items for payment processing

### When to Use

- Upon physical receipt of goods
- When services are completed
- For partial deliveries
- To trigger payment authorization

![View Received Voucher](purchases/img/view_received_voucher (1).png)
![Received Voucher Details](purchases/img/view_received_voucher (2).png)

## 12. Delivery Notes

### Purpose

Delivery Notes provide formal acknowledgment of goods received.

![Delivery Note List](purchases/img/delivery_note_list.png)

### Key Information

- Delivery date and time
- Items received
- Quantities verified
- Condition of goods
- Linked Purchase Orders

### Editing Delivery Notes

![Edit Delivery Note 1](purchases/img/delivery_note_edit (1).png)
![Edit Delivery Note 2](purchases/img/delivery_note_edit (2).png)

### Importance

- Audit trail documentation
- Proof of receipt
- Dispute resolution
- Inventory management

### Bin Records (Deleted Delivery Notes)

![Deleted Delivery Notes](purchases/img/delivery_note_deleted.png)

## 13. Payment Requests

### 13.1 Overview

![Payment Request List](purchases/img/payment_request_list.png)
![PO Backlog for Payment Request](purchases/img/po_backlog_to_create_payment_request.png)

### Purpose

Payment Requests initiate payments to suppliers for goods and services received.

### 13.2 Creating Payment Requests

![Create Payment Request 1](purchases/img/create_payment_requst (1).png)

**Field Guide (Part 1):**

1. **Payment Method** - Payment type selection (required)
2. **Supplier** - Vendor name (required)
3. **Currency** - Transaction currency (required)
4. **Purchase Order** - Linked purchase order
5. **Department** - Requesting department (required)
6. **Project** - Related project
7. **Cost Centers** - Budget allocation category

![Create Payment Request 2](purchases/img/create_payment_requst (2).png)

**Field Guide (Part 2):**

1. **Items Table** - Payment line items from PO
2. **Adjustment** - Price adjustment value
3. **Paid Amount** - Amount to be paid

### Features

- Partial or full payment options
- Payment status tracking
- Integration with accounting
- Approval workflow

### 13.3 Editing Payment Requests

![Edit Payment Request 1](purchases/img/edit_payment_request (1).png)
![Edit Payment Request 2](purchases/img/edit_payment_request (2).png)

### Payment Status

- Pending
- Approved
- Processing
- Paid
- Rejected

### 13.4 Approving Payment Requests

![Payment Request Before Approval 1](purchases/img/view_payment_request_before_approval (1).png)
![Payment Request Before Approval 2](purchases/img/view_payment_request_before_approval (2).png)

### Best Practices

- Verify receipt of goods before payment
- Check invoice accuracy
- Follow approval procedures
- Maintain proper documentation

### Bin Records (Deleted Payment Requests)

![Deleted Payment Requests](purchases/img/deleted_payment_requet.png)

## 14. Summary & Reporting

### Summary Page

The Summary page provides aggregated views of procurement data:

- Purchase Request statistics
- Purchase Order summaries
- Payment status overview
- Filterable by department, project, or supplier

### Approval Logs

![Purchases Approval Log](purchases/img/purchases_approval_log.png)

Comprehensive audit trail showing:

- Who approved or rejected requests
- Timestamp of each action
- Comments and reasons
- Complete transaction history

### Benefits

- Full transparency
- Compliance documentation
- Performance tracking
- Decision accountability

## 15. Permissions & Roles

### User Roles

- **Staff** - Create and view own requests
- **Department Manager** - Approve department requests
- **Project Manager** - Approve project-related purchases
- **Senior Project Manager** - Higher approval limits
- **Finance** - Payment processing and oversight
- **Custom Approvers** - Specialized approval roles

### Permission Types

- View all records
- View own records only
- Create new requests
- Edit existing records
- Delete records
- Approve requests

### Security

The system provides granular permission control to ensure proper authorization and data security.

## 16. Key Features

### Strengths

- End-to-end procurement coverage
- Strong approval and audit controls
- Clear separation of duties
- Scalable for large organizations
- Budget enforcement
- Multi-currency support
- Project and department tracking

### Integration Points

- Projects management
- Budget systems
- Department structures
- Cost center allocation
- Financial accounting
- Approval workflows

## 17. Workflow Best Practices

### For Requesters

1. Provide detailed specifications
2. Link to correct projects and cost centers
3. Check budget availability
4. Submit for approval promptly
5. Respond quickly to rejection feedback

### For Approvers

1. Review requests thoroughly
2. Verify budget availability
3. Check business justification
4. Provide clear rejection reasons
5. Approve or reject promptly

### For Procurement Team

1. Group similar items for efficiency
2. Negotiate best prices
3. Maintain supplier relationships
4. Track delivery timelines
5. Process receipts accurately

### For Finance Team

1. Verify invoice accuracy
2. Match to Purchase Orders
3. Confirm goods receipt
4. Process payments on time
5. Maintain payment records

## 18. Tips for Efficient Use

### General Tips

- Use dashboard for daily overview
- Set up email notifications
- Maintain up-to-date supplier information
- Use filters to find specific records
- Export reports for analysis

### Time-Saving Features

- Bulk actions where available
- Template requests for common items
- Quick filters and search
- Status-based views
- Automated calculations

### Compliance

- Follow approval hierarchies
- Document all decisions
- Maintain proper supporting documents
- Use approval comments effectively
- Regular review of pending items

## 19. Settings & Configuration

The Prizm Purchase module allows administrators to customize workflows to match organizational processes. This is accessed via the **Settings** menu.

### Workflow & Approval Cycle

The system provides granular control over the approval cycle for every purchase document type (PR, PO, ER, Payment, Voucher, Delivery Note). The workflow is defined by a hierarchy of **Stages** and **Statuses**, where each step defines who is responsible for moving the process forward.

### Configuration Logic

The approval cycle is built on the following rules:

1.  **Stages define Responsibility:** Each Stage is assigned a **Responsible** role/person who oversees that phase of the lifecycle.
2.  **Statuses define Approvers:** Each Status within a stage is assigned specific **Approvers**.
3.  **Department-Specific Logic:** Status approvers are tied to **Departments**. This means every department can have its own unique approval settings and authorized personnel for the same status (e.g., "Department Approval" will route to different managers depending on the requester's department).

### Module Workflow Settings

Administrators can configure specific workflows for each module:

- **Purchase Requests (PR):** Manage `PR Stages` and `PR Statuses`.
- **Purchase Orders (PO):** Manage `PO Stages` and `PO Statuses`.
- **Received Vouchers:** Configure `Voucher Stages` and `Voucher Statuses`. Use the **Final** flag for payment eligibility and **Optional** flags for inspection steps.
- **Payment Requests:** Configure `Payment Stages` for authorization levels and `Payment Statuses` for departmental checkpoints (Project, Accounts, Admin), using colors for visibility.
- **Delivery Notes:** Configure `Delivery Note Stages` to track physical receipt phases. Use `Delivery Note Statuses` to manage the verification workflow (e.g., "DN Approval") ensuring goods are inspected and approved before formal acceptance.
- **Expense Requests:** Configure `Expense Request Stages` to define approval phases for expense reimbursements and operational expenses. Use `Expense Request Statuses` to set up departmental approval checkpoints (e.g., Admin approval, Budget validation) with assigned approvers and visual color coding for tracking progress.

### Managing Stages and Statuses

For each document type, you can configure:

- **Stages:** Define the broad phases of the document's lifecycle (e.g., Initiation, Review, Approval, Execution).
    - **Stage Name:** The descriptive name of the workflow phase.
    - **Level:** Assign a numeric hierarchy level (e.g., 1, 2, 3) to order the stages sequentially.
    - **Responsible:** Assign the specific user or role responsible for overseeing this stage.

#### Stages Configuration

The following screens show how to configure stages for different document types:

![Purchase Request Stages](purchases/img/purchase_request_stages.png)
![Purchase Order Stages](purchases/img/purchase_order_stages.png)
![Payment Request Stages](purchases/img/payment_request_stages.png)
![Received Voucher Stages](purchases/img/received_voucher_stages.png)
![Expense Request Stages](purchases/img/expense_request_stages.png)
- **Statuses:** Define granular states within stages. When configuring statuses, you can define:
    - **Stage Association:** Link the status to a specific parent stage.
    - **Approver:** Assign specific approvers. Note that these are linked to departments, allowing for different approvers per department for the same status.
    - **Status Name:** The display name for the status.
    - **Color:** Assign distinct colors (Hex codes) for visual differentiation in lists and dashboards.
    - **Order:** Defines the sequence of the status within its stage.
    - **Optional:** Toggle ("Yes" / "No") to specify if this status is mandatory or skippable in the workflow.
    - **Final:** Toggle ("Yes" / "No") to mark if this status represents a terminal state (completion) for that stage.
    - **Active Status:** Enable or disable the status availability without deleting it.

#### Statuses Configuration

Configure statuses for each document type to define approval checkpoints:

![Purchase Request Statuses](purchases/img/purchase_request_statuses.png)
![Purchase Order Statuses](purchases/img/purchase_order_statuses.png)
![Payment Request Statuses](purchases/img/payment_request_statuses.png)
![Expense Request Statuses](purchases/img/expense_request_statuses.png)

### Options

- **Add New Stage/Status:** Create custom workflow steps.
- **Edit:** Modify names or sequence levels of existing stages.
- **Delete:** Remove unused workflow steps (if not in use).

### Issued PO Manager

![Allow Unverified Supplier Setting](purchases/img/allow_unverified_supplier_setting.png)

The **Issued PO Manager** setting controls supplier validation for purchase orders:

- **Allow Unverified Suppliers:** This setting determines whether unverified suppliers can be used in purchase orders.
    - **Disabled** (Default): Only verified/active suppliers can be selected for POs.
    - **Enabled:** Allows users to create POs with unverified suppliers, providing flexibility for new or temporary vendors.

This setting is particularly useful for organizations that need to work with new suppliers while their verification process is underway.

## 20. Grid View

The **Grid** provides a unified overview of all procurement documents in a single screen. It displays key metrics and quick-access links to Purchase Requests, Purchase Orders, Expense Requests, Received Vouchers, Payment Requests, and Delivery Notes — giving procurement managers instant visibility across the entire purchase lifecycle.

## 21. AI Quotation OCR

The Quotation module includes AI-powered OCR (Optical Character Recognition) capabilities to automatically extract data from scanned or uploaded supplier quotations.

### Supported OCR Engines

| Engine | Default | Description |
|--------|---------|-------------|
| **OpenAI** | Auto | Cloud-based AI extraction |
| **Google Gemini** | Auto | Cloud-based AI extraction |
| **Tesseract** | Auto | Open-source local OCR |
| **Ollama** | Disabled | Local AI model (gemma3:12b) |

### AI Configuration Options

| Setting | Default | Description |
|---------|---------|-------------|
| **AI Injection Enabled** | On | Enable/disable AI extraction on quotations |
| **Single Call Mode** | Off | Use one AI call vs. multiple for extraction |
| **Confidence Threshold** | 0.7 | Minimum confidence to accept extracted data |
| **Auto-Create Supplier** | Off | Automatically create supplier records from quotation data |
| **OCR Page Segmentation** | Mode 4 | Tesseract page analysis mode |

!!! info "AI Extraction"
    When enabled, the AI processes uploaded quotation documents (PDF, images) and automatically extracts supplier details, item names, quantities, prices, and terms. Extracted data is queued for human review before being applied.

## 22. Supplier Portal

The **Supplier Portal** provides external access for suppliers to interact with the procurement system.

### Features

- Suppliers can log in via authenticated access
- View RFQs and quotation requests sent to them
- Submit quotations and upload documents
- Track order status and delivery schedules
- Update contact information

### Access

Supplier authentication is managed separately from staff authentication, ensuring secure isolated access for external vendors.

## 23. Backlog System

The module uses a **Backlog** pattern to provide staging areas between procurement stages:

| Backlog | Purpose |
|---------|---------|
| **Purchase Items Backlog** | Approved PR items waiting to be grouped into Purchase Orders |
| **Purchase Order Backlog** | Approved POs ready for downstream processing (vouchers, payments) |
| **Received Vouchers Backlog** | PO items ready for goods receipt recording |
| **Delivery Notes Backlog** | Items ready for delivery note creation |

!!! tip "Backlog Workflow"
    Backlogs prevent items from falling through the cracks. Procurement staff should regularly review backlogs to ensure timely processing of approved requests.

## 24. Permissions Reference

The module uses **11 separate permission groups** for granular access control:

| Permission Group | Controls Access To |
|-----------------|-------------------|
| **przpurchase** | Purchase Requests |
| **prz_expense_request** | Expense Requests |
| **przorder** | Purchase Orders |
| **przquotation** | Quotations |
| **przsuppliers** | Suppliers |
| **prz_received_vouchers** | Received Vouchers |
| **payment_request** | Payment Requests |
| **delivery_notes** | Delivery Notes |
| **przsummary** | Summary Reports |
| **prz_approvals_logs** | Approval Logs |
| **przsettings** | Module Settings |

Each group supports: **View Own**, **View (Global)**, **Create**, **Edit**, **Delete**.

## 25. Global Search

The Purchases module is fully integrated with the system-wide global search. You can search across all procurement document types:

| Document Type | Search By | Prefix |
|--------------|-----------|--------|
| **Purchase Request** | Sequence number, title | PR- |
| **Purchase Order** | Sequence number, title | PO- |
| **Expense Request** | Sequence number, title | ER- |
| **Suppliers** | Company name | — |
| **Quotations** | Quotation code, prefix | — |
| **Received Vouchers** | Voucher number | MR- |
| **Payment Request** | Sequence number | MT- |
| **Delivery Notes** | Sequence number | DN- |

## 26. Project Integration

The Purchases module adds tabs to the **Project view**:

- **Purchase Request** tab — View all PRs linked to the project
- **Purchase Order** tab — View all POs linked to the project
- **Suppliers** tab — View suppliers associated with the project

This provides project managers with direct visibility into procurement activity for their projects.

## 27. Summary

The Prizm Purchase module provides a comprehensive, controlled, and auditable procurement system. It supports organizations in managing their entire procurement lifecycle from initial request through to payment, ensuring compliance, transparency, and efficiency throughout the process.

### Getting Started

1. Familiarize yourself with the dashboard
2. Understand your role and permissions
3. Learn the approval workflow
4. Practice creating sample requests
5. Contact your administrator for training

### Support

For assistance with the Prizm Purchase module, contact your system administrator or internal support team.
