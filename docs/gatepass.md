# PRIZM Gatepass Module

## 1. Introduction

The Gatepass module is the central system for controlling and recording the physical movement of materials, assets, vehicles and personnel across PRIZM ENERGY sites. By formalising requests, approvals and security checks, it ensures that every movement is authorised, tracked, and compliant with operational and safety policies.

### Key Benefits

- **Security control** – Only approved people, vehicles or equipment can enter or leave
- **Asset traceability** – Records which assets or materials move, when they move, and why
- **Operational coordination** – Links movements with projects, purchase orders or opportunities
- **Auditability** – Maintains a permanent history of who requested, approved and verified each movement

A gatepass therefore represents an official permission slip that follows a structured lifecycle from request through approval to gate verification and completion.

## 2. Module Overview

The PRIZM Gatepass module provides comprehensive tools for:

- Creating and managing gatepass requests
- Controlling physical movement of materials and assets
- Managing vehicle and personnel access
- Approval workflow enforcement
- Security verification at gates
- Entry and exit confirmation
- Comprehensive reporting and audit trails
- Integration with projects, procurement and inventory

## 3. Navigation Structure

The PRIZM Gatepass module is organized as follows:

```
PRIZM Gatepass
├─ Gatepass Dashboard
├─ Gatepass List / Register
├─ Gatepass Creation
├─ Gatepass Types
├─ Gatepass Stages & Statuses
├─ Gatepass Details View
├─ Items / Assets in Gatepass
├─ Vehicle & Driver Information
├─ Approval Workflow
├─ Security Verification & Gate Control
├─ Entry / Exit Confirmation
├─ Gatepass Reports & Audit
└─ Integration with Other Modules
```

## 4. Navigation to Gatepass

### How to Access

Authorised users can reach the Gatepass module from the Admin Portal's side menu:

1. Log in to the PRIZM ENERGY Admin Portal
2. Navigate to **Operations**, **Logistics**, or **Security** section
3. Select **Gatepass**

### Available Menu Items

Within the Gatepass menu, users will find links to:
- Dashboard
- Gatepass register
- Vehicle management
- Request manager
- Settings

**Note:** The menu is visible only to those with the necessary permissions.

## 5. Gatepass Dashboard

The dashboard provides a real‑time snapshot of all gatepass activities.

### Key Indicators

#### Status Counters

Counts of gatepasses by status:
- Pending approval
- Issued
- Completed
- Expired
- In progress
- Draft

#### Upcoming Movements

- Scheduled movements for the day/week
- Expiring passes requiring attention
- Pending returns

#### Alerts

- New requests awaiting review
- Gate verification pending
- Expired documents (licenses, insurance)
- Overdue completions

#### Recent Activity Logs

Timeline of recent:
- Submissions
- Approvals
- Gate verifications
- Completions
- Cancellations

### Typical Users

- **Operations managers** – Monitor daily movement
- **Security supervisors** – Spot bottlenecks
- **Warehouse leads** – Ensure no unauthorised access occurs

## 6. Gatepass List / Register

The register lists every gatepass in the system. It functions as the official log book for all authorised movements.

### What You See

#### Gatepass Table

Key details displayed:
- Gatepass reference number
- Requester name
- Gatepass type
- Duration (start/end dates)
- Destination/location
- Current status
- Associated project or purchase order

#### Filters

Narrow records by:
- Date range
- Type (inward, outward, asset transfer, visitor)
- Status (draft, approved, issued, completed)
- Project
- Requester
- Location

#### Actions

- View details
- Edit (when permitted)
- Cancel
- Restore archived records
- Export for reporting or audit

### Who Uses It

- **Operations and warehouse staff** – Track active passes and plan resources
- **Security teams** – Verify passes at gates
- **Auditors** – Review historical records of all movements

## 7. Gatepass Creation

Creating a gatepass begins by entering all required movement details.

### Creation Flow

#### Step 1: Select Gatepass Classification

Choose whether the movement relates to:
- Project
- Opportunity
- Internal transfer
- Vendor delivery
- Visitor access

#### Step 2: Specify Reference Information

- Link the pass to a project or purchase order
- Provide reference numbers
- Add contract details

#### Step 3: Set Duration and Dates

Choose a pass type:
- **Long term** – Multiple months
- **Short term** – Several days/weeks
- **One day** – Single day access

Define:
- Start date
- End date
- Duration

#### Step 4: Enter Work Location and Details

Identify:
- Site
- Station
- Substation
- Description of work or reason for movement

#### Step 5: Add Representative and Requester Information

Specify:
- Who is responsible for supervising the movement
- Who is submitting the request
- Contact information

#### Step 6: Select Personnel and Vehicles

- Choose employees or visitors who will move
- Select any vehicles involved
- Upload identification documents if required

#### Step 7: Attach Supporting Documents

Upload:
- Letters of authorization
- Permits
- Licenses
- Other supporting documents

#### Step 8: Save or Submit

- **Save as draft** – Continue editing later
- **Submit** – Send the request to approvers

### Important Notes

- Only authorised roles (warehouse staff, project coordinators) can create gatepasses
- Accurate data entry is critical
- Once approved, many fields become locked
- Incomplete information may cause rejection

## 8. Gatepass Types

Gatepasses can represent different movement scenarios.

### Common Types

#### Material Outward

- Goods or materials leaving the premises
- Requires item details and quantities
- May require return confirmation

#### Material Inward

- Deliveries or materials arriving on site
- Links to purchase orders
- Delivery note verification

#### Asset Transfer

- Movement of company‑owned tools or equipment
- Between sites or projects
- Asset tracking and reconciliation

#### Visitor / Personnel

- Temporary access for visitors
- Contractors or employees
- Focus on individual identification and reason for visit

#### Temporary Pass

- Short‑term authorisation
- Defined period
- Specific purpose

#### Permanent / Long Term Pass

- Ongoing or recurring access
- Projects spanning multiple months
- Regular vendor access

### Type-Specific Requirements

Pass types may affect:
- Required information fields
- Approval routing
- Document requirements
- Verification procedures

## 9. Gatepass Stages & Statuses

Gatepasses follow a controlled lifecycle. Each stage determines what actions are possible and who is responsible.

### Status Definitions

| Status | Meaning | Actions Allowed |
|--------|---------|-----------------|
| Draft | Information entered but not submitted | Edit, delete, submit |
| Submitted | Request sent for review but no decision made | Cancel, view |
| Under Review | Managers verifying details, personnel, vehicles | Approve, reject, request changes |
| Approved | All required approvals granted; details locked | Issue, cancel |
| Issued | Gatepass document issued and ready for use | Gate verification |
| In Progress | Personnel/assets/vehicles currently moving | Complete, update status |
| Completed | Exit or entry confirmed by security; archived | View only |
| Rejected | Approvers denied the request | Modify and resubmit |
| Cancelled | Requestor or administrator withdrew the pass | Archive |
| Expired | End date passed without completion | Archive |

### Status Transitions

#### Editing Rules

- **Allowed**: Draft or Submitted states
- **Locked**: Once Approved, information becomes read‑only
- **Exceptions**: Require cancellation and new request

#### Automatic Transitions

- **Expiry**: Automatically becomes Expired if end date passes without completion
- **Security denial**: System marks as denied when verification fails

#### Rejected or Cancelled Passes

- Can be reopened by creating a new request
- Original record remains for audit purposes

## 10. Gatepass Details View

The details view displays everything about a single gatepass in one place.

### Sections Included

#### Summary Panel

Shows:
- Classification
- Linked project or purchase order
- Status
- Duration
- Key dates (created, start, end, completed)

#### Work Information

- Location (site, station, substation)
- Description of work
- Reason for movement
- Special instructions

#### Personnel List

Names of all approved:
- Staff members
- Visitors
- Contractors
- Contact information
- Identification document numbers

#### Vehicle List

For each vehicle:
- Registration number
- Vehicle type
- Driver name
- Insurance expiry
- License expiry
- Color and make/model

#### Documentation

Attached supporting:
- Letters
- Permits
- Licences
- Identification documents
- Insurance certificates

#### Approval History

Records showing:
- Who submitted
- Who reviewed
- Who approved
- Who issued
- Timestamps
- Comments

#### Activity Log

Lists all actions:
- Edits
- Approvals
- Cancellations
- Gate verifications
- Status changes

### Who Uses This View

- **Approvers** – During review process
- **Security** – For verification at gate
- **Auditors** – For post‑completion inspection

## 11. Items / Assets in Gatepass

For movements involving materials or equipment, each item should be explicitly listed on the gatepass.

### Item Information

#### Item Descriptions

Record for each item:
- Name or description
- Category
- Purpose

#### Quantities

Specify:
- Number of units
- Weight
- Volume
- Unit of measure

#### Identifiers

Include:
- Serial numbers
- Asset tags
- Batch numbers
- Part numbers

#### Condition

Note:
- Condition when leaving
- Condition when returning (if applicable)
- Any damages or issues

### Item Management Rules

- **Locking**: Once approved, item lists become locked
- **Verification**: Security guards verify items at gate
- **Reconciliation**: Upon return, items are checked against list
- **Inventory**: Updates stock records and prevents losses

### Why Item Lists Matter

- Ensures nothing moves unnoticed
- Facilitates reconciliation upon return
- Prevents theft and loss
- Supports inventory management
- Provides audit trail

## 12. Vehicle & Driver Information

Whenever vehicles are involved, the gatepass must include comprehensive vehicle and driver details.

### Vehicle Identification

#### Basic Information

- **Registration number** – License plate
- **Plate code** – State/country code
- **Vehicle type** – Pickup, van, truck, car

#### Physical Characteristics

- Color
- Make/model
- Distinguishing features
- Vehicle size/capacity

#### Documents

- **License expiry** – Must be current
- **Insurance validity** – Must be active
- **Inspection certificates** – If required

### Driver Details

#### Driver Information

- Driver's name
- Company affiliation
- Contact number
- Identification document numbers
- Driver's license number

#### Verification

- Scanned copies of vehicle licenses
- Insurance certificates
- Driver identification
- Authorization letters

### Vehicle Registration

- Vehicles must be registered in the system before selection
- Vehicle database maintains all vehicle records
- Links to insurance and maintenance records

### Approval Checks

During review, approvers ensure:
- All vehicle details are valid
- Drivers are authorised
- Documents are not expired
- Insurance coverage is adequate

### Gate Verification

At the gate, security:
- Confirms vehicle matches the pass
- Checks registration plate
- Verifies driver identity
- Inspects documents
- Records entry/exit time

## 13. Approval Workflow

Each gatepass follows a formal approval process that ensures accountability and compliance.

### Workflow Steps

#### 1. Request Submission

- Requestor completes gatepass form
- Submits for approval
- Notifications sent to designated approvers
- Based on classification (project manager or opportunity owner)

#### 2. Review

Approvers:
- Examine the details
- Verify personnel lists
- Check vehicles and attachments
- May request corrections
- Can approve, reject or return for modification

#### 3. Approval

Once all required approvers sign off:
- System marks pass as Approved
- Pass data becomes locked
- Formal document is generated
- Reference number assigned

#### 4. Issuance

The approved pass is:
- Issued as printed document or digital record
- Assigned unique reference number
- Notifications sent to security and warehouse teams
- Ready for gate verification

### Approval Rules

#### Authorization

- Only staff with appropriate role can approve passes
- Approvers cannot approve their own requests (unless delegated authority)
- Multi‑level approvals may be configured for certain pass types

#### Multi-Level Approvals

Example: Both must approve:
- Project manager
- Safety officer

All levels must approve before issuance.

#### Rejection Handling

- Rejection ends the current request
- Requestor can modify and resubmit new request
- Original record preserved for audit

#### Administrative Actions

- Administrators can cancel pending passes
- When circumstances change
- Emergency situations

## 14. Security Verification & Gate Control

Security personnel at the gate play a critical role in enforcing gatepass rules.

### Verification Process

#### Check Gatepass

- Scan or check gatepass reference number
- Retrieve details on handheld device or computer
- Verify pass is active and not expired

#### Confirm Identity

- Check people present match names on pass
- Verify identification documents
- Photo ID verification
- Badge or credentials check

#### Check Vehicles

- Inspect vehicle registration plates
- Verify licenses and insurance dates
- Ensure vehicle matches description on pass
- Check vehicle condition

#### Verify Items

- Tally listed materials or equipment
- Ensure nothing extra or missing
- Check quantities and descriptions
- Note any discrepancies

#### Record Gate Events

- Capture date and time of entry or exit
- Record vehicle details
- Note any discrepancies or incidents
- Log security observations

### Handling Discrepancies

If discrepancies arise:
- Unauthorised person – Refuse entry/exit
- Wrong vehicle – Report and deny access
- Expired pass – Block movement
- Missing items – Investigate before allowing exit

Security can:
- Refuse entry/exit
- Report the issue
- Contact approvers for clarification
- Escalate to supervisor

### Validation Requirement

Security validation is required for pass to progress to:
- In Progress status
- Completed status
- Proper closure

## 15. Entry / Exit Confirmation

After verification, security confirms when the movement takes place.

### Confirmation Process

#### Outbound (Materials or Equipment Leaving)

Security actions:
- Note the time of departure
- Record condition of items
- Photograph items if necessary
- Update pass status to In Progress

For returnable items:
- Pass remains open until items return
- Or until end date is reached

#### Inbound (Deliveries or Visitors Arriving)

Security actions:
- Record arrival time
- Collect paperwork or delivery notes
- Issue visitor badges
- Update pass status

#### Completion

Once all items or personnel have:
- Returned (for two-way movements)
- Or after end date (for one-way movements)

Security actions:
- Mark pass as Completed
- Record completion time
- Note any issues or damages
- Archive for audit

### Benefits

Entry and exit confirmations ensure:
- Physical movement aligns with authorised plan
- Nothing remains unaccounted for
- Complete audit trail
- Asset reconciliation

## 16. Gatepass Reports & Audit

Reporting tools provide insights into gatepass activity and support internal and external audits.

### Report Types

#### Activity Reports

Summarise movements by:
- Period (daily, weekly, monthly)
- Project
- Department
- Vendor

**Use cases:**
- Planning
- Performance monitoring
- Resource allocation

#### Status Reports

Highlight passes that are:
- Pending approval
- Issued
- In progress
- Overdue for completion
- Expired

#### Compliance Reports

Identify passes with:
- Expired or missing documents
- License violations
- Insurance gaps
- Violations and exceptions

#### Audit Logs

Record every action:
- Who created
- Who edited
- Who approved
- Who cancelled
- Who restored
- Timestamps for all actions

Provides complete chain of custody for each pass.

### Report Features

- **Export options** – Spreadsheet or PDF formats
- **Filters** – Date range, type, status, location
- **Scheduling** – Automated report generation
- **Custom views** – Create specific report templates

### Usage

Reports are essential for:
- Internal audits
- External compliance reviews
- Investigations
- Performance analysis
- Management reviews
- Security assessments

## 17. Integration with Other Modules

The Gatepass module integrates with several other systems within the ERP.

### Project Management

- Gatepasses linked to specific projects
- Project information populates the pass
- Approvals may come from project managers
- Resource tracking aligned with project needs

### Opportunities & Sales

- Passes associated with opportunities
- Site visits during sales stages
- Convert from request to pass when needed
- Sales coordination

### Procurement & Purchase Orders

- Materials delivered or dispatched
- Gatepasses reference purchase order numbers
- Synchronise with inventory and finance
- Delivery verification

### Vendor & Supplier Records

- Vendor details pulled into gatepasses
- Inbound deliveries
- Correct contact and contract information
- Supplier performance tracking

### Asset & Inventory Management

- Movement of tools, equipment and stock
- Updates inventory records
- Triggers reconciliation upon return
- Asset tracking and location updates

### Human Resources

- Employee and contractor details
- Names, roles, contact numbers
- Staff database integration
- Maintain consistency
- Reduce data entry

### Vehicle Management

- Vehicles registered in vehicle module
- Documents and status checked
- Before assignment to passes
- Maintenance and insurance tracking

### Security Logs

- Gate verification feeds into security reporting
- Entry/exit confirmations
- Comprehensive view of site access
- Security incident tracking

## 18. Permissions & Roles

Access to the Gatepass module is controlled via defined roles and permissions.

### Typical Roles

| Role | Responsibilities | Permissions |
|------|------------------|-------------|
| Requestor | Creates gatepass requests, edits drafts, submits for approval | Create, edit drafts, submit, cancel before approval |
| Approver | Reviews and approves or rejects requests | View, approve, reject, request changes, add comments |
| Gatepass Administrator | Manages system settings, approval routing, document templates | Configure settings, manage users, override restrictions |
| Vehicle Manager | Maintains vehicle records, documents and assignment to passes | Manage vehicles, update documents, assign to passes |
| Security Personnel | Verifies passes at gate, records entry/exit, completes passes | Verify, confirm entry/exit, complete passes, report issues |
| Auditor | Views all passes, logs and reports | Read-only access to all records, generate reports |
| System Administrator | Full privileges across the module | All permissions, delete/restore records, manage roles |

### Permission Levels

Permissions determine which screens and actions each user can access:

- **Requestors** – May only see their own passes
- **Approvers** – Can view all passes they are responsible for
- **Administrators** – Access to all configuration and management features
- **Security** – Focus on verification and gate operations
- **Auditors** – Comprehensive read-only access

## 19. Common Operational Scenarios

Gatepasses support a variety of day‑to‑day operational needs.

### Scenario 1: Sending Equipment for Repair

1. Record tools being dispatched to service center
2. Identify vehicle transporting them
3. Specify expected return date
4. Attach service order or repair request
5. Approve and issue pass
6. Gate verification on exit
7. Return confirmation on entry

### Scenario 2: Receiving Vendor Deliveries

1. Create inbound pass for supplier
2. Include purchase order references
3. Attach delivery notes
4. Approve based on PO
5. Security verifies delivery
6. Materials received into inventory
7. Pass completed

### Scenario 3: Contractor Site Access

1. Issue pass for contractor teams
2. Working on specific project
3. Specific start and end dates
4. Station locations specified
5. Personnel list with IDs
6. Vehicle details included
7. Daily or periodic verification

### Scenario 4: Employee Transferring to Another Site

1. Authorise employees to transport company assets
2. Between projects
3. Asset list attached
4. Transfer documentation
5. Receiving site confirmation
6. Asset reconciliation
7. Pass completion

### Scenario 5: Visitor Entry

1. Grant temporary access for guests
2. Specify host and purpose
3. Location and time window
4. Identification verification
5. Badge issuance
6. Escort requirements
7. Exit confirmation

### Scenario 6: Temporary Removal of Spare Parts

1. Allow engineers to take parts off site
2. For testing or emergency repair
3. Tracking to ensure return
4. Condition documentation
5. Return deadline
6. Verification on return
7. Inventory update

## 20. Best Practices & Tips

To get the most out of the Gatepass module:

- **Plan ahead** – Submit requests early to allow sufficient time for approvals and document preparation
- **Provide complete and accurate information** – Incomplete passes cause delays and may be rejected
- **Attach supporting documents** – Upload permits, letters and licenses to support your request
- **Choose the correct type and duration** – Align the pass with the actual movement to avoid unnecessary rework
- **Verify vehicles and staff** – Ensure vehicles have valid licenses and insurance, and that staff lists are up to date
- **Monitor the dashboard** – Use real‑time indicators to track pending tasks and avoid expired passes
- **Update responsibility settings** – Administrators should keep approval settings and contact numbers current
- **Follow security procedures** – Security should not bypass verification; discrepancies must be reported immediately
- **Document everything** – Take photos of items and vehicles when appropriate
- **Communicate changes** – Inform all parties if plans change
- **Review before submission** – Double-check all details before submitting
- **Track returns** – For returnable items, set reminders for return dates

## 21. Known Limitations / Notes

While comprehensive, the Gatepass module has a few operational constraints:

- **Gatepasses cannot be deleted once approved** – They can only be cancelled or archived for audit purposes
- **Editing is not permitted after issuance** – Any changes require cancellation and creation of a new pass
- **Passes automatically expire at end of duration** – Expired passes cannot be reactivated; a new pass is required
- **Approval workflows are predefined** – Complex multi‑department approval chains may require configuration by an administrator
- **File uploads have size limits** – Must be in supported formats (PDF, image, spreadsheet) to be processed
- **Digital signatures and stamps** – Must be configured in advance for document generation
- **Integration with external systems** – May require additional configuration by the IT team
- **Concurrent editing** – Multiple users editing the same draft may cause conflicts
- **Browser compatibility** – Optimized for modern browsers; older browsers may have limited functionality
- **Mobile access** – Some features may have limited functionality on mobile devices
- **Offline capability** – Module requires internet connection for real-time updates

This guide should assist security personnel, warehouse staff, operations managers and auditors in effectively using the Gatepass module to control physical access and asset movement across PRIZM ENERGY facilities.
