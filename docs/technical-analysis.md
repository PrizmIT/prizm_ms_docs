# PRIZM Technical Analysis Module – User Guide

## Overview

The **Technical Analysis** module is a core engineering governance component within the PRIZM ENERGY ERP Admin Portal. It provides a structured framework for performing, documenting, reviewing, and approving technical evaluations related to projects, opportunities, vendors, and engineering decisions.

A Technical Analysis record represents a formal technical assessment used to validate feasibility, compliance, risks, scope alignment, and engineering soundness before critical business or project decisions are finalized. The module ensures transparency, traceability, and accountability across engineering and management teams.

Technical Analysis supports:
- Engineering validation and design compliance  
- Risk identification and mitigation  
- Technical decision justification  
- Cross-department alignment  
- Audit and compliance requirements  

---

## Navigation to Technical Analysis

The Technical Analysis module is accessible from the Admin Portal main navigation menu. Users with appropriate permissions can locate it under the engineering or technical governance section of the sidebar.

Navigation typically follows:
- Admin Portal → Technical Analysis

Access visibility depends on assigned user roles and permissions.

---

## Technical Analysis Dashboard

The dashboard provides a consolidated overview of all Technical Analysis activities.

Users see:
- Summary counters by status (Draft, Under Review, Approved, Rejected, etc.)
- Recently updated Technical Analysis records
- Pending reviews and approvals
- Key engineering workload indicators

Typical users:
- Engineering managers  
- Project managers  
- Technical leads  

The dashboard helps prioritize reviews, monitor engineering throughput, and identify bottlenecks.

---

## Technical Analysis List / Register

![Technical Analysis List](./technical-analysis/img/technical_analysis_list.png)

The Technical Analysis Register displays all records in a searchable and filterable list.

Users can:
- View all Technical Analysis records
- Filter by status, type, related project or opportunity
- Sort by creation date, last update, or priority
- Open records for detailed review

This screen acts as the central control point for managing the full Technical Analysis lifecycle.

---

## Technical Analysis Creation

![Technical Analysis Create Form](./technical-analysis/img/technical_analysis_create_form.png)

**Field Guide:**

1. **Analysis ID** - Auto-generated identifier
2. **Project Type** - Type of project
3. **Project Funded** - Funding source
4. **Staff Member** - Assigned staff member
5. **Related To** - Linked opportunity or project
6. **World's Domain / Opportunity** - Domain and opportunity link
7. **Note** - Additional notes
8. **Description** - Detailed description of the analysis

Creating a Technical Analysis initiates a formal technical evaluation process.

During creation, users typically define:
- Technical Analysis title and reference
- Purpose and scope of the analysis
- Related project, opportunity, or external request
- Requesting department or individual
- Assigned engineers or reviewers

Mandatory information must be completed before submission. Records are saved in **Draft** status until formally submitted for review.

Typical creators:
- Engineers  
- Project managers  
- Technical coordinators  

---

## Technical Analysis Types

The module supports multiple Technical Analysis types to cover diverse engineering use cases, including:
- Project-based Technical Analysis
- Opportunity-based Technical Analysis
- Vendor or supplier technical evaluation
- Design review and compliance assessment
- Method statement or technical proposal review

The selected type determines applicable evaluation criteria, review participants, and approval requirements.

---

## Technical Analysis Stages & Statuses

Each Technical Analysis follows a controlled lifecycle with defined statuses:

- **Draft** – Editable working version
- **Submitted** – Formally sent for review
- **Under Review** – Actively reviewed by assigned engineers
- **Clarification Required** – Additional input or revisions requested
- **Revised** – Updated after clarification
- **Approved** – Technically accepted
- **Rejected** – Not technically acceptable
- **Closed** – Finalized and archived

Status rules:
- Editing is restricted once submitted
- Approved or rejected records are locked
- Revisions require explicit resubmission
- Closed records are read-only

---

## Technical Analysis Details View

![Technical Analysis Detail View](./technical-analysis/img/technical_analysis_detail_view.png)

The detail view is the central workspace for each Technical Analysis record.

Users see:
- General information and metadata
- Related projects, opportunities, or vendors
- Current status and assigned reviewers
- Action buttons based on permissions and status

Actions may include:
- Submit for review
- Request clarification
- Approve or reject
- Upload supporting documents

---

## Technical Scope & Evaluation Criteria

![Technical Analysis Scope Items](./technical-analysis/img/technical_analysis_scope_items.png)

![Technical Analysis Supplier Pricing](./technical-analysis/img/technical_analysis_supplier_pricing.png)

This section captures the core engineering assessment.

Users document:
- Technical scope and assumptions
- Design requirements and constraints
- Compliance with standards and specifications
- Feasibility and constructability considerations
- Identified risks and mitigation measures

Completion of mandatory technical sections is required before submission or approval.

---

## Attachments & Supporting Documents

Users can attach supporting documentation such as:
- Drawings and schematics
- Technical specifications
- Calculations and simulations
- Vendor datasheets
- Method statements

Certain Technical Analysis types require mandatory attachments. Attachments become locked after approval to preserve audit integrity.

---

## Review & Clarifications

Reviewers use this section to:
- Add technical comments
- Request clarifications
- Highlight risks or non-compliance
- Recommend approval or rejection

Clarification requests temporarily return the record to the requestor for updates. All comments are preserved as part of the audit trail.

---

## Approval Workflow

The Technical Analysis approval workflow enforces governance and accountability.

Key characteristics:
- Engineering-level technical approval
- Optional management or senior engineering approval
- Single or multi-level approval based on configuration
- Automatic status updates and timestamps

Only authorized approvers can finalize decisions.

---

## Revision & Version History

The module maintains a complete revision history.

Users can:
- View previous versions
- Track what changed and when
- See who made each change
- Identify approval outcomes per version

Revisions ensure continuous improvement while maintaining traceability.

---

## Technical Analysis Reports & Audit

Reporting and audit features provide:
- Status-based Technical Analysis reports
- Engineering workload summaries
- Approval and rejection statistics
- Complete audit logs of actions and decisions

These reports support compliance audits and management reviews.

---

## Integration with Other Modules

Technical Analysis integrates tightly with:
- Opportunities
- Projects
- RFQs and Tenders
- Vendors and Suppliers
- Document Management
- Tasks and Assignments
- Approval workflows

Integration ensures technical decisions directly inform commercial, project, and procurement processes.

---

## Permissions & Roles

Access is controlled through role-based permissions, including:
- Create and edit Technical Analysis
- Review and comment
- Approve or reject
- View reports and audit logs
- Administer configuration and access

Permissions ensure segregation of duties and governance compliance.

---

## Common Technical Scenarios

Typical use cases include:
- Evaluating design feasibility for a new project
- Assessing vendor technical compliance during tendering
- Reviewing method statements for execution approval
- Validating scope alignment before project kickoff

---

## Best Practices & Tips

- Clearly define technical scope and assumptions
- Attach all relevant supporting documents
- Respond promptly to clarification requests
- Use objective, standards-based evaluation criteria
- Ensure approvals reflect documented conclusions

---

## Actual Navigation Menu

The Technical Analysis module sidebar contains:

| Sub-menu | Description | Access |
|----------|-------------|--------|
| **Dashboard** | Overview with statistics | Admin only |
| **Technical Analysis** | Main list with table view | All with view permission |
| **BOQ Management** | Bill of Quantities management (AG Grid) | TI view or BOQ view permission |
| **Settings** | Stages, statuses, approval configuration | Admin only |

---

## BOQ Management

The **BOQ (Bill of Quantities) Management** sub-module provides a dedicated workspace for creating and managing BOQs linked to opportunities, projects, or technical inquiries.

### BOQ Features

- **Auto-generated BOQ codes** based on relation type (project, opportunity, TI)
- **Version tracking** — Each BOQ has a version number for revision control
- **Line item management** — Add, edit, and delete BOQ items with automatic total calculation
- **Multi-currency support** — Select currency for each BOQ
- **Excel import/export** — Import items from Excel or export for sharing
- **AG Grid table** — Interactive table for BOQ listing
- **Relation linking** — Each BOQ is linked to a project, opportunity, or TI via `rel_type` and `rel_id`

### Creating a BOQ

1. Navigate to **Technical Analysis > BOQ Management**
2. Click **Create BOQ** or access from within an opportunity/project
3. Fill in:
    - **Title** — Descriptive name for the BOQ
    - **Currency** — Select the currency
    - **Related To** — Project, Opportunity, or Technical Inquiry
    - **Notes** — Additional remarks
4. Add line items with quantities and amounts
5. Save — the total value is auto-calculated

### BOQ Versioning

BOQs support version tracking, allowing you to:

- Create revised versions of existing BOQs
- Track changes across versions
- Compare different versions

---

## Technical Inquiry Detail Tabs

When viewing an individual Technical Inquiry, the following tabs are available:

| Tab | Description |
|-----|-------------|
| **Overview** | Summary with circle progress indicators |
| **Details** | Core fields and line items with specifications |
| **RFQ** | Linked Requests for Quotation |
| **Tasks** | Tasks assigned within the TI |
| **Timesheets** | Time tracking entries |
| **Files** | Document and attachment management |
| **Notes** | Internal notes |
| **Discussions** | Threaded discussion board |
| **Edit** | Edit form for the TI |

---

## Smart Wizard

Technical Inquiry creation uses a **multi-step Smart Wizard** interface:

1. **Step 1**: General details (title, description, dates)
2. **Step 2**: Select items from budget catalog (with specifications and units)
3. **Step 3**: Resource allocation wizard
4. **Step 4**: Review and submit

---

## Kanban Board

The Technical Analysis list supports a **Kanban board view** for visual stage-based tracking, similar to the Opportunities module.

---

## Import Capabilities

- **Import Technical Inquiries** — Bulk import from external sources
- **Import Budget Items** — Import items from budget module data

---

## Permissions Reference

The module uses **2 permission groups**:

### Technical Inquiries

| Permission | Description |
|------------|-------------|
| **View (Global)** | View all technical inquiries |
| **View Own** | View only your own TIs |
| **Create** | Create new technical inquiries |
| **Edit** | Modify existing TIs |
| **Delete** | Delete TIs |
| **Upload** | Upload files and attachments |

### BOQ

| Permission | Description |
|------------|-------------|
| **View BOQ** | View bills of quantities |
| **Create BOQ** | Create new BOQs |
| **Edit BOQ** | Modify existing BOQs |
| **Delete BOQ** | Delete BOQs |
| **Upload BOQ** | Upload BOQ-related files |

---

## Integration with Other Modules

| Module | Integration |
|--------|-------------|
| **RFQ** | TI status change can auto-create an RFQ |
| **Budget** | Items, specifications, and units sourced from budget catalog |
| **Materials** | API integration for material data |
| **Tenders** | Import data from tenders into TIs and BOQs |
| **Projects** | "Technical Analysis" tab added to project view |
| **Opportunities** | TIs linked to opportunities via relation system |
| **Tasks** | TI is a relation type — tasks can be linked to TIs |

---

## Global Search

The module provides global search across two entity types:

- **Technical Analysis** — Search by title, inquiry code, or description
- **BOQs** — Search by BOQ code, title, or notes (displays version number)

---

## Project Integration

The module adds a **Technical Analysis** tab to the project view, allowing project managers to view and manage all TIs related to their project directly from the project page.

---

## Known Limitations / Notes

- Approved records cannot be edited without special permissions
- Deletion is restricted after submission
- Historical records are preserved for audit purposes
- Some workflows depend on organizational role configuration
- BOQ version changes create new records; previous versions are retained
- Auto-RFQ creation from TI status changes depends on the RFQ module being active
