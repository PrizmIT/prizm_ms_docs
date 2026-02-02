# PRIZM Resource Manager Module

## 1. Introduction

The Resource Manager module is a core part of the PRIZM ENERGY ERP system. It provides a unified platform for registering, classifying, allocating and tracking all resources used across the organisation's projects and operations. These resources can be physical items (e.g., construction materials, tools, equipment) or non‑physical assets (e.g., service hours or licences). By centralising resource information, the module supports accurate planning, cost control and seamless collaboration between departments.

### Key Capabilities

- **Resource Directory** – Every resource has a unique code, descriptive name, category and lifecycle information. Each entry captures ownership, vendor/partner references, pricing and user‑defined metadata
- **Flexible classification structures** – Resources can be organised into hierarchical categories and sub‑categories
- **Comprehensive Units & Measurements framework** – Incorporating base units (metre, kilogram, second, ampere, Kelvin, etc.) and user‑defined unit categories
- **Stock and availability tracking** – Ensures resources are on hand when needed
- **Allocation and return workflows** – Links resources to projects, kits or work orders while maintaining audit trails
- **Detailed history and reporting features** – Supports operational decisions and management oversight

## 2. Module Overview

The PRIZM Resource Manager module provides comprehensive tools for:

- Managing resource directory and master data
- Organizing resources with hierarchical categories
- Defining and managing units of measurement
- Tracking stock levels and availability
- Allocating resources to projects and tasks
- Processing resource returns and adjustments
- Managing resource kits and batch issues
- Generating resource usage reports
- Maintaining approval workflows

## 3. Navigation Structure

The PRIZM Resource Manager module is organized as follows:

```
PRIZM Resource Manager
├─ Dashboard
├─ Resource Directory (Master)
├─ Resource Categories & Types
├─ Units & Measurements
├─ Resource Stock & Availability
├─ Resource Allocation & Issue
├─ Resource Return & Adjustments
├─ Project Resource Assignment
├─ Resource Usage History
├─ Resource Reports
└─ Approvals & Workflow Logic
```

## 4. Navigation to Resource Manager

### How to Access

1. Log in to the PRIZM ENERGY Admin Portal
2. From the navigation bar, choose **Operations → Resource Manager**
3. The module opens in its own workspace, showing a dashboard and list of options on the left

### Available Menu Items

Depending on your permissions, you will see:
- Resource Directory
- Categories
- Units
- Stock
- Kits
- Allocations
- Reports
- Settings

**Note:** Unsaved changes are highlighted before navigating away to prevent accidental data loss.

## 5. Resource Manager Dashboard

The Dashboard provides an at‑a‑glance overview of your resources. It summarises key metrics and allows quick filtering by status.

### Dashboard Elements

#### Status Counters

Tiles showing:
- Total number of resources
- Resources added manually
- Resources requiring review
- Archived items
- Classification statuses (Pending Classification, Needs Manual Classification, etc.)

These counters correspond to the resource lifecycle states that administrators use to manage data quality.

#### Recent Activity

A feed of recent:
- Additions
- Updates
- Allocations
- Returns

Each entry shows the resource name, action, user and timestamp.

#### Alerts and Tasks

Indicators for:
- Pending approvals
- Low stock thresholds
- Classification reviews requiring attention

#### Quick Actions

Buttons to:
- Add a new resource
- Review duplicates
- Manage brands
- Launch merge tools

### Dashboard Customization

The dashboard can be customised per user role:
- **Managers** – See KPI charts (e.g., resource utilisation over time)
- **Operational staff** – Focus on quick links to frequent tasks

## 6. Resource Directory (Resources Master)

The Resource Directory is the master list of all resources. Each entry represents a distinct item or asset.

### Resource Information Fields

#### Basic Information

- **Resource Code** – Unique identifier (material number, SKU or asset tag)
- **Resource Name** – Descriptive name for the resource
- **Category** – Links to a category or sub‑category from classification hierarchy
- **Ownership / Staff** – Staff member who registered the resource

#### Partner & Vendor Details

- Partner references (vendor names)
- Partner item codes
- Partner item names

Use these to map internal resources to supplier catalogues.

#### Financial Information

- **Purchase Price** – Cost for acquisition
- **Selling Price** – Price for internal transfers or sales

Prices are stored with four decimal places for accuracy.

#### Additional Information

- **Remarks** – Free‑text notes for additional description or usage notes
- **Date Created** – Automatically recorded timestamp when the resource is added
- **Metadata** – User‑defined attributes stored in a companion metadata table

### Metadata Management

Each metadata record links to a resource, storing:
- Meta field name
- Value
- Optional unit

**Examples:** dimensions, power rating, colour, voltage, weight

Metadata can be added via the Specifications area and appears on resource detail pages.

### Managing Resources

#### Create a Resource

1. Click **Add New Resource** on the directory page
2. Enter the resource name, code, and category
3. Provide partner references if necessary
4. Fill in purchase/sell price and remarks
5. Add metadata fields with appropriate units
6. Save

**Note:** Provide sufficient descriptive details (at least 20 characters) to enable AI classification and duplicate checking. The resource appears with default status (Pending Classification).

#### Edit a Resource

1. Select a resource from the list to open its details
2. Update names, codes, categories, prices, remarks or metadata
3. Changes are recorded in the history

#### Archive a Resource

- Use the archive toggle to deactivate a resource
- Archived items remain in the system for historical reference
- Hidden from active lists

#### Delete a Resource

- Resources can be deleted if they have no allocations or history
- System blocks deletion when there is usage history to preserve data integrity

#### Merge Resources

Duplicate resources can be merged:
1. Use the merge tool to display potential duplicates
2. Based on AI suggestions or user filters
3. Choose the master record
4. Merge metadata, prices and codes accordingly

### Filtering & Searching

#### Filter Bar Options

- **Status Filters** – Total, Added Manually, Need Review, Archived, etc.
- **Classification Status** – Pending Classification, Classified, Needs Manual Classification, Pending Approval
- **Keyword Search** – Search across all fields
- **Custom Filters** – Define filters on metadata fields or partner attributes

#### Table Features

- Column sorting
- Pagination
- Export to Excel or CSV

## 7. Resource Categories & Types

Categories organise resources into a logical hierarchy.

### Category Structure Examples

- Electrical → Cables → High‑Voltage Cables
- Mechanical → Pumps → Centrifugal Pumps

Categories are stored with parent/child relationships. Mark a category as a **main category** to indicate top‑level groupings.

### Managing Categories

#### Create a Category

1. Navigate to **Resource Manager → Categories**
2. Click **Add Category** button
3. Provide a name
4. Optionally select a parent category to build the hierarchy
5. Assign a staff owner if desired
6. Creation date is recorded automatically

#### Edit a Category

1. Click category name in the list
2. Update the name
3. Change the parent
4. Toggle the main flag

#### Delete a Category

Deleting a category is only allowed if no resources or sub‑categories depend on it.

### Category Features

- **Unlimited depth** – Categories support unlimited hierarchical levels
- **Tree control** – UI presents a tree showing parent/child relationships for quick selection
- **Staff ownership** – Each category can be assigned to a staff member

## 8. Units & Measurements

Consistent units are critical for accurate planning and reporting. The Resource Manager includes a dedicated units framework.

### Framework Components

#### Base Units

Standard International (SI) base units:
- Metre (m) – Length
- Kilogram (kg) – Mass
- Second (s) – Time
- Ampere (A) – Electric Current
- Kelvin (K) – Temperature

These provide the foundation for derived units and conversions.

#### Unit Categories

Categories group related units:
- Length
- Mass
- Time
- Electric Current
- Temperature

Each category references a base unit (e.g., Length category has metre as its base unit).

#### Units

Derived or custom units (e.g., centimetre, inch, kilogram‑force).

Units include attributes such as:
- Type (integer, float)
- Conversion factor relative to base unit
- Formula for complex conversions
- Rounding rules
- Allowed quantity type (integer vs. fractional)
- Base unit flag

These fields help ensure correct conversions during allocations and reporting.

### Managing Units

#### Add a Unit

1. Open **Resource Manager → Units**
2. Click **Add Unit**
3. Select the category
4. Define the symbol (e.g., "cm")
5. Specify whether it is a base unit
6. Provide conversion factor to base unit (e.g., 0.01 for centimetre to metre)
7. Optionally enter rounding rules and quantity restrictions

#### View Units

The units list shows:
- Symbol
- Category
- Type
- Conversion details

#### Edit or Archive Units

- Units can be edited or archived
- Deleting a unit is only allowed if no resources, specifications or allocations reference it

#### Manage Unit Categories

1. Open **Units → Categories**
2. Provide category name
3. Link it to one of the SI base units

### System Enforcement

The system enforces consistency by:
- Preventing multiple base units within the same category
- Blocking conversion factors that would lead to rounding errors or negative results

## 9. Resource Stock & Availability

Stock management ensures resources are available when required without excessive overstock.

### Stock Tracking Fields

#### Current Quantity

- On‑hand quantity of each resource
- When created, quantity is zero until stock entries are added
- Inventory adjustments occur through allocations, returns and manual stock adjustments

#### Committed Quantity

- Quantity reserved for pending allocations or kits
- Deducted from available stock to prevent double booking

#### Available Quantity

- Calculated as: **Current Quantity – Committed Quantity**
- Resources become unavailable when available quantity reaches zero

#### Reorder Point

- Threshold that triggers procurement planning
- When stock falls below this level, system generates alerts or purchase requisitions

### Managing Stock

#### View Stock

Navigate to **Resource Manager → Stock**

The stock table shows:
- Resource name
- Unit of measurement
- Current quantity
- Committed quantity
- Available quantity

#### Add Stock

1. Click **Add Stock** button
2. Select a resource
3. Specify the quantity, unit and date
4. Add optional reference (e.g., purchase order)
5. System prevents negative quantities
6. Records each stock addition in resource history

#### Adjust Stock

To decrease stock outside of an allocation (e.g., write‑off due to damage):
1. Use **Adjust Stock** button
2. Provide quantity decrease
3. Add a reason
4. Negative balances are not allowed

#### Stock Ledger

Displays all stock movements with:
- Dates
- Quantities
- Units
- References
- Staff members

This ledger supports audit and costing.

## 10. Resource Allocation & Issue

Allocations tie resources to projects, tasks or kits. When you allocate a resource, the system reduces its available quantity and records who, when and where the resource is used.

### Allocation Workflow

#### Step 1: Navigate to Allocations

Go to **Resource Manager → Allocations**

#### Step 2: Start Allocation

Click **Allocate Resource**

#### Step 3: Select Target

Select the project or work order

#### Step 4: Choose Resources

- Choose the resource(s)
- Specify quantities and units
- Can allocate multiple resources at once
- System checks availability and conversion factors

#### Step 5: Confirm Allocation

- Resource's committed and available quantities update immediately
- Allocation record created with status of **Issued**

### Batch Issues & Kits

**Resource kits** are predefined sets of resources used together.

Examples:
- "Plumbing Kit" containing pipes, fittings and sealant
- "Electrical Installation Kit" with cables, switches and boxes

#### Kit Features

- Kits have their own IDs
- Maintain lists of constituent resources with quantity and units
- Issuing a kit allocates all its items at once
- Saves time and ensures completeness

#### Using Kits

If the resource is part of a Resource Kit, selecting the kit automatically populates the individual kit items and quantities.

## 11. Resource Return & Adjustments

Once resources are no longer needed on a project, they must be returned to stock or written off. Proper return management prevents resource loss and updates availability.

### Return Workflow

#### Step 1: Navigate to Returns

Go to **Resource Manager → Returns**

#### Step 2: Locate Allocation

Find the allocation record to be returned

**Note:** You can return part or all of the issued quantity.

#### Step 3: Specify Return Details

- Quantity being returned
- Unit
- Return date
- Remarks (e.g., condition on return)

#### Step 4: Process Return

- System increases current quantity
- Decreases committed quantity

### Adjustments for Consumed Resources

If resources were damaged or consumed:
1. Use **Adjustment** option
2. Write off the used portion
3. Do not add back into stock

### Approval & History

- All returns and adjustments appear in resource history
- May require approval depending on workflow settings

## 12. Project Resource Assignment

The Resource Manager integrates tightly with the Projects module. Resource assignments ensure that resources are scheduled and costed correctly against projects.

### Assignment Features

#### Assign to Project Tasks

When creating or updating a project task:
1. Add required resources
2. Specify resource, quantity, unit and planned usage date
3. Reserves the quantity
4. Provides visibility in planning views

#### Automatic Allocation

- On task start, system can automatically allocate required resources
- Based on the assignment
- Ensures stock is deducted
- Usage is recorded

#### Cost Tracking

- Assigned resources contribute to project budgets
- Purchase price or internal transfer cost is captured
- Included in project costing reports

#### Schedule Integration

- Resource assignments appear in project schedules
- Allows planners to avoid over‑commitment
- Identifies resource bottlenecks

## 13. Resource Usage History

Every action on a resource is logged. The Usage History provides a detailed audit trail.

### Logged Events

#### Creation and Updates

- When resource is created or edited
- Records date, user and changes
- Includes updates to codes, names, categories, pricing, metadata and status

#### Stock Movements

- Additions
- Issues
- Returns
- Adjustments

Shows quantities, units, references and notes.

#### Allocations and Returns

- Allocation records show project/work order
- Quantities and status (issued, returned)
- Returns and write‑offs linked back to original allocation

#### Merges and Classification

- When resources are merged
- Classification status changes (e.g., pending to approved)
- Events are recorded

#### Custom Events

Administrators can add custom log entries for special circumstances (e.g., quality inspection results).

### Using History

Use the history to:
- Trace back discrepancies
- Answer audit queries
- Train new staff on proper resource handling

## 14. Resource Reports

Reports provide insights into resource usage, stock levels and efficiency. The module offers several pre‑built reports and allows ad‑hoc analysis.

### Pre-Built Reports

#### 1. Stock Summary

- Shows current, committed and available quantities
- By resource, category or unit
- Filter by location, project or time period

#### 2. Usage Report

- Lists allocations and returns over a period
- Useful for analysing consumption trends
- Forecasting needs

#### 3. Project Resource Cost

- Summarises resource costs per project
- Compares budgeted versus actual usage

#### 4. Category Analysis

- Aggregates usage and cost by category
- Identifies high‑value areas
- Potential savings opportunities

#### 5. Custom Reports

Users with reporting permissions can build custom views by selecting:
- Resource code
- Name
- Category
- Unit
- Quantity
- Price

Apply filters as needed.

### Report Export

Reports can be exported to:
- Excel
- PDF

For further analysis or sharing with stakeholders.

## 15. Approvals & Workflow Logic

Proper governance requires approvals for certain actions. The Resource Manager implements workflow logic based on the type of action and user role.

### Workflow Types

#### Classification Review

- New resources may require classification approval
- System's AI suggests a category
- Classification Review queue allows authorised users to approve or override
- Items can be marked as:
  - Pending Approval
  - Classified
  - Needs Manual Classification
  - Rejected
- Approved changes update the resource record
- Rejected suggestions remain pending

#### Merge Approval

- Merging resources or specifications can have far‑reaching effects
- May require approval from supervisor or administrator
- Workflow records:
  - Who initiated the merge
  - Who approved it
  - Final merged state

#### Allocation Approval

- For high‑value resources or large quantities
- Allocations can be configured to require approval
- Managers receive notifications
- Can approve, reject or modify allocation requests

#### Return and Adjustment Approval

- To prevent misuse
- Returns and stock adjustments may need sign‑off
- Approvers verify quantities and reasons
- System updates stock after approval

### Workflow Configuration

Workflows are configurable in **Resource Manager Settings**:
- Define approval thresholds
- Assign approvers
- Set escalation rules

Workflow status is displayed in relevant queues and history records.

## 16. Integration with Other Modules

The Resource Manager integrates with several other PRIZM modules for seamless data flow.

### Project & Task Management

- Resources can be assigned to tasks and projects
- Links planning, execution and resource availability

### Budgeting & Costing

- Resource costs feed into budgets and cost reports
- Price fields integrate with budgeting module
- Accurate financial tracking

### Procurement

- Low stock triggers generate purchase requests
- Supplier information and partner item codes streamline ordering

### Accounting

- Resource transactions can be posted to accounts
- Interface with chart of accounts
- Mapping items to income or expense accounts
- Transactions include:
  - Purchases
  - Allocations to projects
  - Write‑offs

### Reporting

- Data available to reporting engine
- Allows cross‑module reports
- Example: resource utilisation vs. project progress

Integration ensures consistent data and avoids duplicate entry across the ERP system.

## 17. Permissions & Roles

Access to the Resource Manager is governed by role‑based permissions.

### Common Roles

| Role | Typical Permissions |
|------|---------------------|
| Administrator | Full access to all functions, including settings, approvals, merges and deletions |
| Resource Manager | Create, edit and archive resources; manage categories, units and kits; allocate and return resources; view reports |
| Project Manager | View resources; request allocations; assign resources to tasks; view usage and costs |
| Reviewer/Approver | Approve classifications, merges, allocations and returns |
| Viewer | Read‑only access to resources, stock and reports |

### Permission Features

- Permissions can be fine‑tuned for your organisation
- Users only see menu items and actions corresponding to their role
- Attempting a restricted action prompts "Access Denied" message

## 18. Common User Scenarios

### Registering a New Resource

1. Go to **Resource Directory** and click **Add New Resource**
2. Enter a descriptive name, unique code
3. Select a category
4. Provide partner details if necessary
5. Fill in purchase/sell price and remarks
6. Add metadata fields (dimensions, weight, voltage)
7. Assign appropriate units
8. Save
9. Resource appears with status **Pending Classification** until approved

### Classifying and Approving a Resource

1. Navigate to **Resource Manager → Classification Review**
2. Select a resource in the **Pending Classification** list
3. Review the AI‑suggested category and metadata
4. Approve the suggested classification, modify it or mark as needing manual classification
5. Once approved, resource status updates to **Classified**
6. Becomes available for allocations

### Allocating Resources to a Project

1. Go to **Allocations** and click **Allocate Resource**
2. Choose the target project or work order
3. Select one or more resources
4. Specify quantities and units
5. If resource is part of a kit, selecting the kit populates kit's items automatically
6. Submit the allocation
7. Depending on configuration, request might require approval
8. Upon approval, system reserves quantities and records allocation

### Returning and Adjusting

1. Open the **Returns** menu
2. Select the allocation to return
3. Enter the quantity being returned and remarks
4. Partial returns are allowed
5. Confirm
6. Returned quantity is added back to stock
7. Any remainder left unused can be adjusted or written off

### Merging Duplicate Resources

1. Navigate to **Resource Manager → Merge Resources**
2. System displays potential duplicates based on name, code and metadata similarity
3. Review the candidates
4. Select the primary resource and one or more duplicates
5. Merge wizard shows differences in fields and metadata
6. Decide which values to keep
7. Approve and merge
8. Duplicates are archived
9. Reference links (allocations, history) are redirected to primary resource

## 19. Best Practices & Tips

- **Use meaningful codes and names** – Short yet descriptive resource codes and names help users locate items quickly
- **Maintain a clean category structure** – Plan your category hierarchy in advance; avoid creating similar categories with subtle differences
- **Define units carefully** – Ensure conversion factors and base units are accurate; changing these can affect historical data
- **Capture rich metadata** – Use specifications and metadata fields to store important attributes; makes searching and classification more effective
- **Regularly review duplicates and classifications** – Periodic reviews help maintain data quality; use merge and classification review tools
- **Set reorder points** – For consumable resources, define reorder thresholds to avoid stockouts; leverage alerts for timely procurement
- **Train users on allocation/return procedures** – Ensures staff know how to allocate and return resources; reduces errors and improves auditability
- **Document resource specifications** – Complete metadata helps with accurate planning and procurement
- **Monitor stock levels regularly** – Review stock reports to identify overstock or shortage situations
- **Use kits for common resource sets** – Saves time and ensures completeness when issuing frequently used resource combinations

## 20. Known Limitations / Notes

- The module supports both stock‑based and non‑stock resources; for intangible resources (e.g., licences), availability tracking is limited to quantity and expiry dates
- Deleting resources is restricted; records with allocations or history cannot be deleted; they must be archived instead
- Changing unit conversion factors affects all reports and calculations; such changes should be tested in a staging environment first
- Complex workflows (e.g., multi‑level approvals) require careful configuration in the settings area; consult your system administrator for advanced setup
- AI classification and duplicate detection depend on the quality of input descriptions; provide detailed descriptions to improve accuracy
- Integration with other modules may depend on your organisation's configuration; some features (such as automatic purchase requests or accounting postings) might not be enabled in every deployment
- Browser support is optimised for modern browsers; outdated browsers may not display interactive grids or modals correctly
- Mass imports of resources require proper data formatting and validation; use the provided import templates
