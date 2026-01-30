# PRIZM Budget Module

## 1. Introduction

The PRIZM Budget module is the financial backbone of the PRIZM ENERGY Admin Portal. It enables departments and project teams to plan, control, and track budgets for materials, manpower, equipment, services, contingencies, petty cash, and advance cash. Budgets are associated either with projects or departments, and they link seamlessly with resource requests, deployment plans, procurement, finance, and approvals.

This guide explains every major page and workflow, from creating budgets to tracking deployment and cash requests, so internal users can manage funds responsibly and transparently.

This module is integrated with:

- Projects
- Opportunities/Sales
- Purchasing/Procurement
- Inventory
- HR/Payroll
- Finance

## 2. Module Overview

The PRIZM Budget module provides comprehensive tools for:

- Creating and managing project and department budgets
- Tracking budget items and specifications
- Processing resource requests (materials, manpower, equipment, services)
- Managing deployment plans and schedules
- Handling advance cash and petty cash
- Maintaining approval workflows
- Generating financial reports and analytics

## 3. Navigation Structure

The PRIZM Budget module is organized as follows:

```
PRIZM Budget
├─ Budget Dashboard
├─ Budget Categories
├─ Budget Items
├─ Budget Creation & Management
├─ Resource Requests
├─ Deployment Plans
├─ Deployment Reports
├─ Advance Cash Management
└─ Approvals & Workflow Logic
```

## 4. Navigation to PRIZM Budget

### How to Access

1. Log in to the PRIZM ENERGY Admin Portal using your credentials
2. From the main navigation menu, select **PRIZM Budget**
   - Depending on your role, this may appear under Finance, Projects, or Administration
3. The Budget module opens on the Budget Dashboard

## 5. Budget Dashboard

The dashboard is the starting point for budget activities. It summarises all budgets you can access, grouped by status, and provides quick filters and actions.

### Key Features

#### Status Summary

Counters for each budget status:
- Draft
- Submitted
- Approved
- Partial Approved
- Rejected
- Revoked

These help you see how many budgets are in each stage.

#### Filters

- **Date range** – narrow the list to budgets created within a specific period
- **Show additional budgets** – include supplementary budgets linked to parent budgets
- **Show only active projects** – hide budgets linked to closed projects
- **Show non‑project budgets** – display budgets created for departments rather than projects

#### Budget List

Budgets are displayed in a grid with columns for:
- Budget code
- Description
- Project/Department
- Total requested amount
- Total approved amount
- Currency
- Status
- Creation date

Clicking a row opens the budget details.

#### Actions

- **New Budget** – create a fresh budget
- **Export/Print** – export data or print summaries for reporting purposes

### When to Use

Use the dashboard to:
- Get a snapshot of all budgets
- Quickly filter by status or date
- Start a new budget
- Locate budgets awaiting review (for approvers)

## 6. Budget Categories

Budget categories classify costs and help track spending against the right account. Categories are predefined by system administrators (e.g., Materials, Manpower, Equipment, Services, Contingency Fund).

### Managing Categories

- For most users, categories are **read‑only**
- Maintained by finance or system administrators under **Settings → Budget Settings**
- Administrators can add, edit, or deactivate categories
- Categories map to general ledger accounts
- Contact your finance team to request new category creation

### Common Categories

- Materials
- Manpower
- Equipment
- Services
- Contingency Fund
- Petty Cash
- Advance Cash

## 7. Budget Items

A budget is composed of items—the individual goods or services required for a project or department. Each item has a specification, unit of measure, quantity, unit price, and total cost.

### Viewing and Managing Items

#### Items List

Under **Budget Items**, the system lists all service items and manpower items.

Columns include:
- Item category
- Short and long names
- Default specification
- Unit of measure
- Creation date
- Creator

Features:
- Click an item to view its details
- Create new service or manpower items using **New Service Item** or **New Manpower Item** (if permitted)

#### Item Details

Each item shows:
- Default specification and unit
- Submission history
- Approval status
- Rejection history (for rejected items)

Items must be **submitted and approved** before they can be used in a budget or resource request.

### Why Item Management Matters

- Standardised items ensure pricing consistency
- Accurate cost estimates
- Approved items speed up budget creation
- Users can select approved items instead of defining new specifications each time

## 8. Budget Creation & Management

Creating a budget involves defining its scope, adding items, and submitting it through an approval workflow. Budgets can be project‑based (linked to a specific project) or department‑based (for departmental expenses).

### Creating a New Budget

#### Step 1: Start from the Dashboard

Click **New Budget**

#### Step 2: General Details

- **Budget description** – provide a clear title
- **Budget type** – choose Project or Department
- **Project/Department** – select the relevant project or department
- **Manager** – identify who is responsible for the budget
- **Currency** – choose the currency for cost estimation
- **Start and end dates** – indicate the validity period of the budget

#### Step 3: Cost Centres and Codes

Assign cost centre(s) and reference codes, which link the budget to accounting structures.

#### Step 4: Add Items

1. Click **Add Item** to open a row for each item
2. Select the category (material, manpower, equipment, service, contingency fund, petty cash, or advance cash)
3. Choose an existing item and its specification and unit, or create a new item if permitted
4. Specify the quantity and unit price; the system calculates the line total and cumulative totals
5. Repeat for each required item
6. Use **Add Specification** if multiple specifications exist for the same item

#### Step 5: Attach Supporting Documents

Upload supplier quotations, estimates, or designs if required.

#### Step 6: Additional Budgets

If you need to add funds later, create an **additional budget** which links to the parent budget. Additional budgets follow the same creation process but reference the original budget for context.

#### Step 7: Save or Submit

- **Save as Draft** – return later without starting the approval process
- **Submit** – send the budget to the approval workflow

Once submitted, edits are restricted until the budget is approved or rejected.

### Managing Existing Budgets

#### View Details

Click on a budget from the dashboard to open its detail page showing:
- General information
- Item breakdowns
- Attached documents
- Discussion threads
- Status history

#### Edit

- **Draft status** – can be edited freely
- **Submitted for approval** – limited editing (e.g., add notes but not change amounts)
- **Approved** – read‑only except for additional budgets and revocation actions

#### Revoking Budget Amounts

If funds are released back to the budget (e.g., a resource request is cancelled), the system tracks revoked budgets. These appear separately in the budget detail and affect available balances.

### Budget Statuses

| Status | Purpose |
|--------|---------|
| Draft | Budget is being prepared and not yet submitted |
| Submitted | Sent for approval; awaiting decisions |
| Approved | Fully approved; funds can be used |
| Partial Approved | Partially approved; some items or amounts reduced |
| Rejected | Declined; the creator may resubmit with changes |
| Resubmitted | Returned for review after rejection |
| Revoked | Budget funds released back (e.g., unused) |

## 9. Resource Requests

Resource requests are the mechanism for consuming budgeted funds. They convert budget items into actionable requests for procurement or operations.

### Types of Resource Requests

| Request Type | Typical Use |
|--------------|-------------|
| Material | Raw materials, consumables, spare parts |
| Manpower | Labour—contractors, temporary staff, labourers |
| Equipment | Rental or purchase of tools and machines |
| Service | External services such as consulting or design |
| Contingency Fund | Unforeseen expenses; acts as a buffer |
| Petty Cash | Small, routine purchases |
| Advance Cash | Larger cash advances before procurement |

### Creating a Resource Request

#### Step 1: Navigate to Resource Requests

From the Budget detail page or main menu, select **Resource Requests**.

#### Step 2: Select Budget

Choose the budget you wish to draw from. Only budgets in **Approved** or **Partial Approved** status allow requests.

#### Step 3: Request Details

- Choose the request type from the table above
- Provide a description, required date, and any internal notes
- For budget‑based requests, department and project fields are auto‑filled
- For general requests, choose a department and optional project

#### Step 4: Add Items

- Select items from the associated budget
- Specify the quantity requested and any specifications
- The system checks available quantities and prevents over‑requesting
- If you need an alternate item, specify the alternate item to be used instead of the budgeted one

#### Step 5: Submit for Approval

The request goes through its own approval workflow. Once approved, it can generate purchase requisitions or deployment plans.

### Tracking Resource Requests

Resource requests include status badges:
- Submitted
- Approved
- Rejected
- Partial Approved
- Cancelled

You can view:
- Item‑level approvals
- Rejection reasons
- Discussion threads

**Note:** Approved requests reduce the available budget; revoked or cancelled requests restore budget funds.

## 10. Deployment Plans

Deployment plans schedule and allocate resource request items to specific projects, sites, or dates. They ensure that approved materials or manpower are delivered to the right place at the right time.

### Creating a Deployment Plan

#### Step 1: Open Deployments

From the main menu, select **Deployments**.

#### Step 2: Choose Creation Type

- **New Deployment** for a single date
- **Multiple Dates Deployment** to plan across several dates
- **Calendar View** to plan visually on a calendar

#### Step 3: Select Deployment Date

The system checks that the date is not already used; if a deployment exists, you can view or edit it instead of creating a new one.

#### Step 4: Add Rows for Each Deployed Item

- **Resource Request** – choose the resource request that provides items
- **Staff / Supplier** – assign employees or suppliers responsible for the deployment
- **Project & Site** – specify where the deployment takes place
- **Job Position** – record the job position of manpower
- **Item** – select the approved item from the resource request
- **Quantity** – specify quantity deployed (cannot exceed approved quantity)
- **Type** – indicate whether the item is Normal or Alternate
- **Notes** – include system notes and custom notes for context

#### Step 5: Save

The plan can be edited until it is finalised. Each deployment entry validates that staff are not deployed elsewhere or on leave and prevents duplicate allocations.

### Managing Deployment Plans

#### Table View

Lists all deployments with columns for:
- Deployment date
- Added by
- Creation date
- Updated date
- Actions (view, edit, delete)

#### Calendar View

- Provides a calendar where each deployment appears as an event
- Clicking an event shows details
- Double‑clicking an empty date creates a plan for that date

#### Relocation

You can relocate deployed staff to another project using the **Relocate Staff** option:
1. Select staff
2. Choose the new project and site
3. Provide remarks
4. The system moves the deployment entries accordingly

#### Deployed Items Report

Generates a detailed report of all deployed items for a selected project showing:
- Requested quantity
- Approved quantity
- Deployed quantity
- Remaining quantity
- Deployment history by date, staff, and site
- Normal and alternate items are clearly labelled

### Why Deployment Plans Are Important

- Bridge the gap between approval and execution
- Ensure resource request items are utilised efficiently
- Provide traceability for audit and project tracking

## 11. Deployment Reports

Deployment reports offer insights into how and when budgeted resources are consumed on the ground.

### Deployed Items Report

For a selected project, this report lists each item with:
- Quantities and status
- Remaining balances
- Every deployment entry (date, staff, job position, site, and notes)

### Use This Report To

- Verify that deployment matches the approved resource requests
- Track remaining quantities for ongoing projects
- Identify alternate items used in place of original budgeted items
- Prepare evidence for project audits or financial reporting

## 12. Advance Cash Management

Advance cash is a controlled way of providing funds before expenses are incurred. The module supports requesting and tracking advance cash and integrates with petty cash and budgets.

### Requesting Advance Cash

#### Step 1: Open Advance Cash

In the Budget module, select **Advance Cash**.

#### Step 2: Click Request Advance Cash

A form appears with fields:

- **Advance cash code** – auto‑generated and unique
- **Title** – a descriptive name for the request
- **Request type** – Budget‑based (linked to a budget) or General (not linked)
- **Requested amount** – the total amount needed
- **Department/Project/Budget** – depending on the request type
- **Note** – justification for the advance

#### Step 3: Add Expense Items

Each item line includes:
- Category
- Item name
- Description
- Specification
- Quantity
- Unit price
- Tax

#### Step 4: Apply Discounts

You can apply a discount (percentage or fixed amount).

#### Step 5: Submit for Approval

The advance cash request enters the approval workflow. Only after approval can the funds be released.

### Tracking Advance Cash

Once funds are granted, you must track usage:

#### Step 1: Open Track Advance Cash

Select the request to track.

#### Step 2: Fill Usage Details

- Enter suppliers, receipt numbers, purchase dates, and notes
- Add each expense item, specifying category, item name, description, specification, quantity, unit price, and tax
- The system calculates subtotals, discounts, and totals automatically

#### Step 3: Review Remaining Petty Cash

The form displays:
- Total petty cash
- Used amount
- Remaining balance

#### Step 4: Submit

Once submitted, usage details are reviewed and recorded against the advance cash request.

### Advance Cash Reports

The **Advance Cash Custody Report** summarises:
- Outstanding advances
- Usage details
- Helps finance teams ensure that all advances are justified and closed

## 13. Approvals & Workflow Logic

The Budget module relies heavily on approvals to ensure spending is authorised. Each approval flow is configurable and consists of stages and statuses.

### Approval Stages and Roles

#### Stages

An approval flow can include multiple stages (e.g., Department Head, Finance, Director):
- Each stage has a stage level (order)
- Associated with staff roles
- May belong to a project or department
- Can be marked optional or final

#### Approvers

- One or more approvers can be assigned within a stage
- Approvers review and either approve or reject requests
- Optional stages can be skipped if not applicable
- Final stages require no further approval after approval

#### Notifications

When a request reaches a stage:
- Assigned approvers receive a notification
- Comments and discussion threads allow clarifications before decision

### Approval Statuses

| Status | Description |
|--------|-------------|
| Submitted | Awaiting approval |
| Approved | All approvers have granted approval; object moves forward |
| Partial Approved | Approvers approve but adjust quantities or prices |
| Rejected | Approver declines; creator receives rejection reason |
| Resubmitted | Previously rejected object updated and sent back |
| Cancelled/Revoked | Request cancelled or revoked; funds returned |

### Partial Approval & Resubmission

When partial approval is granted:
- System records maximum quantity and maximum unit price allowed
- Creator may accept these terms or resubmit with adjusted quantities
- Resubmissions require a note explaining the changes

### Approval Settings

Administrators configure stages and statuses in **Budget Settings**:
- Create new stages
- Assign approvers
- Mark stages optional or final
- Define colours for status badges
- Ensure approvals align with organisational policies

## 14. Integration with Other Modules

The Budget module interacts with several other modules in the PRIZM ERP suite:

### Projects

- Budgets can be tied to projects
- Approved budgets feed into project financial reports
- Track actual versus budgeted costs

### Opportunities/Sales

- Resource requests may originate from sales opportunities
- Ensure materials and manpower are budgeted before proposals are finalised

### Purchasing/Procurement

- Approved resource requests generate purchase requisitions and purchase orders
- Deployment plans ensure ordered items are delivered to the right site

### Inventory

- Materials requested and deployed are recorded in inventory
- Remaining quantities and alternates are tracked

### HR/Payroll

- Manpower budgets and deployment plans integrate with job positions and staff records
- Deployment checks staff leave schedules

### Finance

- Advance cash and petty cash management integrate with finance
- Cash disbursement, reconciliation, and posting to general ledger accounts
- Budgets can be exported to QuickBooks or other accounting systems

This integration ensures accurate data flow across the organisation and prevents duplication of data entry.

## 15. Permissions & Roles

Access to the Budget module is controlled via roles and permissions:

### Budget Creators

- Typically project managers, department heads, or authorised staff
- Can create and edit budgets
- Add items and submit budgets for approval

### Approvers

- Individuals assigned to approval stages (e.g., Finance Manager, Director)
- Can view requests awaiting their approval
- Approve or reject and add comments

### View‑Only Users

- Staff who need to see budgets and reports but cannot create or approve
- Examples: auditors or project team members

### Finance Administrators

- Maintain budget settings (categories, units, stages, statuses)
- Manage petty cash and advance cash
- Generate financial reports

### System Administrators

- Configure module settings
- Assign permissions
- Manage integration with other modules

Permissions are granular; administrators can specify which users or roles can:
- Create budgets
- Manage items
- Request resources
- Approve requests
- View sensitive financial data
- Run reports

## 16. Common User Scenarios

### Creating a New Project Budget

A project manager:
1. Opens the Budget module
2. Clicks New Budget
3. Enters general details
4. Adds items for materials and manpower
5. Attaches supplier quotes
6. Submits the budget

The budget goes through approval stages and, once approved, the project can request resources.

### Raising a Material Resource Request

After a budget is approved, a project engineer:
1. Selects Resource Requests
2. Chooses Material
3. Picks items from the approved budget (e.g., steel beams)
4. Sets quantities and submits

Approvers review and approve the request, which then creates a purchase requisition in the procurement system.

### Planning Deployment

A site supervisor:
1. Uses Deployments to schedule labourers for next week
2. Selects relevant resource requests
3. Assigns staff and job positions to each site
4. Checks that staff are not on leave
5. Saves the deployment plan
6. Runs the Deployed Items Report to see deployment hours

### Requesting Advance Cash

A department head:
1. Opens Advance Cash
2. Fills out the request with items and total amount
3. Selects the relevant budget
4. Submits it

After approval, the finance team releases the cash. The head later tracks expenses and attaches receipts to close the advance.

### Approving a Budget

A finance manager:
1. Logs into the Budget module
2. Filters budgets with Submitted status
3. Reviews each budget's details and attached documents
4. Either approves or rejects them
5. Uses Partial Approval to reduce quantities or prices if needed

The budget creator then resubmits or accepts the partial terms.

## 17. Best Practices & Tips

- **Plan budgets early** – Create budgets before starting major project activities to ensure funds are available and avoid delays
- **Use accurate item specifications** – Selecting the correct item and specification prevents mismatches during procurement and deployment
- **Attach supporting documents** – Upload supplier quotes, estimates, or designs to justify costs; approvers are more likely to approve well‑documented budgets
- **Monitor status regularly** – Use the dashboard's summary counters and filters to track which budgets or requests require attention
- **Communicate via comments** – Use discussion threads within budgets and resource requests to clarify questions with approvers
- **Avoid over‑requesting** – The system prevents exceeding approved quantities, but estimate realistic needs to minimise resubmissions
- **Leverage calendar view** – For deployment, use the calendar view to avoid scheduling conflicts and visualise workload across dates
- **Maintain approval settings** – Administrators should periodically review stages, statuses, and approvers to ensure the workflow reflects organisational changes
- **Keep item catalog updated** – Regularly review and approve new items to expand the catalog
- **Document changes** – Use notes and remarks to document why changes were made
- **Track advance cash promptly** – Close advance cash requests quickly by tracking expenses and attaching receipts

## 18. Known Limitations / Notes

- **Single project association** – Each budget is linked to one project or department. If a budget needs to cover multiple projects, create separate budgets or additional budgets for each project
- **Editing after approval** – Once a budget or resource request is fully approved, it becomes read‑only. To adjust amounts, create an additional budget or raise a partial request
- **Quantity and price limits** – Partial approvals enforce maximum quantities and unit prices. Exceeding these limits requires resubmission
- **Unique codes** – The system generates unique codes for budgets, petty cash, and advance cash requests. These codes cannot be manually changed
- **Deployment date uniqueness** – Each deployment date must be unique; you cannot create multiple deployment plans for the same date without using the Multiple Dates option
- **Staff availability** – Deployment checks staff leave and previous deployment assignments. Ensure leave records are up to date to avoid scheduling conflicts
- **Browser support** – The module is optimised for modern browsers. Outdated browsers may not display interactive grids or modals correctly
