# PRIZM RFQ Module

## 1. Introduction

The **RFQ (Requests for Quotation)** module in PRIZM ENERGY ERP manages the full procurement quotation lifecycle, from internal request creation through supplier invitation, quotation collection, evaluation, approval, and final award. It ensures a transparent, auditable, and structured approach to supplier selection and cost control.

RFQs act as the formal bridge between internal demand (projects, budgets, operational needs) and external suppliers.

### Key Capabilities

- Complete RFQ lifecycle management
- Supplier invitation and response tracking
- Quote evaluation and comparison
- Approval workflow integration
- Automated conversion to Purchase Orders
- Comprehensive reporting and analytics
- Document management and audit trails

## 2. Module Overview

The PRIZM RFQ module provides comprehensive tools for:

- Creating and managing RFQs
- Inviting suppliers and tracking responses
- Comparing and evaluating quotations
- Managing approval workflows
- Converting RFQs to Purchase Orders or Contracts
- Generating procurement reports
- Maintaining compliance and audit trails

## 3. Navigation Structure

The PRIZM RFQ module is organized as follows:

```
PRIZM RFQ
├─ RFQ Dashboard
├─ RFQ List / Pipeline
├─ RFQ Creation
├─ RFQ Stages & Statuses
├─ RFQ Details View
├─ Supplier Invitations & Responses
├─ Quote Evaluation & Comparison
├─ RFQ Items (Products / Services)
├─ Documents & Attachments
├─ RFQ Approval Workflow
├─ RFQ Conversion (to Purchase Order / Contract)
├─ RFQ Reports & Analysis
└─ Integration with Other Modules
```

## 4. Navigation to RFQ

### How to Access

Access the RFQ module from the Admin sidebar:

1. Log in to the PRIZM ENERGY Admin Portal
2. Navigate to **Procurement → RFQ**
3. The RFQ workspace opens where users can:
   - View dashboards
   - Manage RFQs
   - Initiate new quotation requests

### User Permissions

Access is controlled based on user roles and permissions configured by administrators.

## 5. RFQ Dashboard

The RFQ Dashboard provides a real-time overview of procurement activity.

### Dashboard Components

#### Status Summary

RFQs grouped by status:
- **Draft** – Being prepared
- **Pending** – Awaiting internal action or approval
- **Active** – Sent to suppliers, awaiting responses
- **Expired** – Response deadline passed
- **Closed** – Supplier awarded
- **Archived** – Stored for reference

#### Visual Indicators

- Summary counters for each status
- Color-coded status badges
- Progress indicators

#### Filters

- Time-based filters (date ranges, due dates)
- Supplier-based filters
- Project-based filters
- Owner/assigned user filters
- Priority filters

### Why It Matters

Procurement managers can immediately:
- Identify bottlenecks
- Monitor overdue RFQs
- Track workload distribution
- Prioritize urgent requests
- Review pipeline health

## 6. RFQ List / Pipeline

The RFQ List displays all RFQs in a searchable, filterable table.

### Key Information

Each RFQ entry shows:
- **RFQ Reference** – Unique identifier
- **Related Project or Request** – Source of the RFQ
- **Assigned Owner** – Responsible procurement officer
- **Supplier Response Status** – Number of responses received
- **Current Lifecycle Status** – Draft, Active, Closed, etc.
- **Creation Date** – When the RFQ was initiated
- **Due Date** – Response deadline
- **Estimated Value** – Total quote value

### Common Actions

- **Open RFQ details** – View full RFQ information
- **Edit draft RFQs** – Modify RFQs before sending
- **Send RFQs to suppliers** – Initiate quotation process
- **Archive or close completed RFQs** – Finalize and store

### Table Features

- Column sorting
- Pagination
- Advanced filtering
- Bulk actions
- Export to Excel/PDF

## 7. RFQ Creation

Creating an RFQ initiates the formal quotation process.

### Creation Flow

#### Step 1: Initiate RFQ

Click **Create RFQ** from the dashboard or list view

#### Step 2: Enter RFQ Details

- **Subject** – Clear description of what is being quoted
- **Related Project** – Link to project or budget
- **Owner** – Assign responsible procurement officer
- **Priority** – Low, Medium, High, Urgent
- **Due Date** – Supplier response deadline
- **Currency** – Quote currency

#### Step 3: Define Email Settings

- **Email Subject** – Subject line for supplier invitation
- **Sender** – Email sender (typically procurement team)
- **Email Template** – Use predefined templates or customize

#### Step 4: Add RFQ Items

For each item, specify:
- Item name/description
- Quantity
- Unit of measure
- Specifications
- Technical requirements
- Reference documents

#### Step 5: Select Suppliers

- Choose from approved supplier list
- Add new suppliers if needed
- Specify per-supplier instructions
- Set individual response deadlines (if different)

#### Step 6: Add Remarks and Notes

- **Public Remarks** – Visible to suppliers
- **Internal Notes** – For internal team only
- **Terms and Conditions** – Commercial terms
- **Special Instructions** – Delivery, warranty, etc.

#### Step 7: Save or Send

- **Save as Draft** – Continue editing later
- **Send** – Immediately send to suppliers

**Note:** Draft RFQs remain fully editable until sent.

## 8. RFQ Stages & Statuses

RFQs move through controlled stages to ensure proper workflow.

### Stage Definitions

#### Draft

- Being prepared
- Fully editable
- Not visible to suppliers
- Can be deleted

#### Pending

- Awaiting internal action or approval
- Limited editing
- Requires approval to proceed

#### Active

- Sent to suppliers
- Awaiting responses
- Core fields locked
- Cannot be deleted

#### Expired

- Response deadline passed
- Can still receive late responses
- May be extended or closed

#### Closed

- Supplier awarded
- RFQ finalized
- Converted to PO or Contract

#### Archived

- Stored for reference
- Read-only
- Cannot be modified

### Status Transitions

Once an RFQ is **Active**, core fields become locked to maintain integrity and ensure fair comparison across suppliers.

### Status Visibility

Users can filter and view RFQs by status to manage their workflow effectively.

## 9. RFQ Details View

The RFQ Details page is the central workspace for managing an individual RFQ.

### Page Components

#### RFQ Summary

- Reference number
- Subject/description
- Related project
- Owner
- Current status
- Priority level
- Creation and due dates

#### Item List

Complete list of items being quoted with:
- Item descriptions
- Quantities
- Units
- Specifications
- Target prices (if applicable)

#### Supplier Invitations

List of invited suppliers with:
- Supplier name and contact
- Invitation status (sent, opened, responded)
- Response received indicator
- Quote submission date

#### Response Indicators

Visual indicators showing:
- Number of suppliers invited
- Number of responses received
- Number pending
- Overdue responses

#### Internal Notes and Remarks

- Team discussions
- Evaluation notes
- Decision rationale
- Change history

#### Attachments and Documents

- Technical specifications
- Drawings
- Sample documents
- Supplier quotations

#### Approval History

- Approval requests
- Approver actions
- Comments and feedback
- Timestamps

### Action Buttons

Depending on status and permissions:
- Edit RFQ
- Send to Suppliers
- Extend Deadline
- Evaluate Quotes
- Request Approval
- Award Supplier
- Convert to PO
- Archive

## 10. Supplier Invitations & Responses

Suppliers are invited directly from the RFQ to ensure proper communication and tracking.

### Invitation Process

#### Sending Invitations

1. Select suppliers from the RFQ
2. System generates personalized email
3. Email includes:
   - RFQ reference
   - Item details
   - Specifications
   - Response deadline
   - Submission instructions
   - Contact information

#### Email Delivery

- Invitations are emailed automatically
- Delivery status is tracked
- Failed deliveries are flagged
- Reminders can be sent

### Response Tracking

#### Supplier Behavior

- **Invitations sent** – Tracked with timestamp
- **Email opened** – Read receipt captured (if supported)
- **Response submitted** – Quote received indicator
- **Attachments uploaded** – Files captured and stored
- **Response status visible** – Per supplier status

#### System Features

- Automatic response logging
- Email threading
- Document attachment capture
- Response validation

### Benefits

This ensures:
- No quotation is lost or overlooked
- Complete audit trail
- Fair and transparent process
- Easy follow-up on pending responses

## 11. Quote Evaluation & Comparison

The module supports structured quote comparison to make informed procurement decisions.

### Evaluation Features

#### Side-by-Side Comparison

Compare suppliers across:
- Price per item
- Total quote value
- Delivery terms
- Payment terms
- Warranty
- Lead time
- Quality certifications

#### Price Analysis

- Lowest price highlighting
- Price variance calculation
- Historical price comparison
- Budget vs. quote analysis

#### Commercial Review

Evaluate non-price factors:
- Supplier reputation
- Past performance
- Compliance with specifications
- Terms and conditions
- Risk assessment

#### Internal Evaluation Notes

- Team comments
- Scoring or ranking
- Recommendation rationale
- Risk considerations

#### Preferred Supplier Selection

- Mark preferred supplier
- Document selection criteria
- Record decision justification

### Approval Process

Approved evaluations move the RFQ to award stage, triggering conversion to Purchase Order or Contract.

## 12. RFQ Items (Products / Services)

RFQ Items define what is being quoted and ensure consistency across suppliers.

### Item Management

#### Item Fields

- Item code or SKU
- Description
- Technical specifications
- Quantity
- Unit of measure
- Target price (optional)
- Notes

#### Editing Rules

- **Draft and Pending** – Fully editable
- **Active** – Locked once sent to suppliers
- **Closed** – Read-only

#### Sharing

- Items are shared across all supplier quotations
- Ensures apples-to-apples comparison
- Maintains fair evaluation process

### Item Specifications

Attach detailed specifications:
- Technical drawings
- Material standards
- Performance requirements
- Quality certifications
- Compliance requirements

### Why Clear Definitions Matter

Clear item definitions ensure:
- Fair comparison across suppliers
- Accurate pricing
- Reduced clarification requests
- Faster evaluation
- Better compliance

## 13. Documents & Attachments

RFQs support comprehensive document management throughout the lifecycle.

### Common Documents

#### Request Phase

- **Technical specifications** – Detailed requirements
- **Scope of work** – Project scope documents
- **Drawings and designs** – Technical drawings
- **Sample documents** – Reference materials

#### Response Phase

- **Supplier quotations** – Quote documents
- **Technical proposals** – Supplier proposals
- **Certifications** – Quality/compliance certificates
- **Brochures** – Product information

#### Evaluation Phase

- **Evaluation notes** – Internal assessments
- **Comparison spreadsheets** – Analysis documents
- **Recommendation reports** – Decision documentation

### Document Management

- Upload and download
- Version control
- Access permissions (internal only or shared with suppliers)
- Document tagging
- Search functionality

### Audit Trail

All documents remain linked to the RFQ for:
- Compliance verification
- Historical reference
- Audit purposes
- Knowledge management

## 14. RFQ Approval Workflow

Approval may be required before sending RFQs or awarding suppliers to ensure proper governance.

### Workflow Stages

#### Pre-Send Approval

- Review RFQ content
- Verify item specifications
- Confirm supplier list
- Validate budget availability

#### Pre-Award Approval

- Review evaluation results
- Verify selected supplier
- Confirm pricing
- Check compliance

### Approval Process

#### Step 1: Submit for Approval

User submits RFQ or evaluation for approval

#### Step 2: Approver Review

Approver reviews:
- RFQ details
- Item list
- Selected suppliers
- Evaluation results (for award approval)
- Budget impact

#### Step 3: Approver Action

- **Approve** – RFQ proceeds to next stage
- **Reject** – RFQ returns with comments
- **Request Changes** – Modifications required

#### Step 4: Follow-up

- Approved RFQs proceed automatically
- Rejected RFQs require updates and resubmission

### Audit Trail

System records:
- Who approved or rejected
- Timestamps
- Comments and feedback
- Version history

### Field Locking

During approval:
- Critical fields are locked
- Prevents unauthorized changes
- Maintains integrity

## 15. RFQ Conversion (to Purchase Order / Contract)

Awarded RFQs convert into downstream procurement documents.

### Conversion Process

#### Step 1: Award Supplier

1. Select winning supplier from evaluation
2. Confirm quoted prices and terms
3. Document selection rationale
4. Mark RFQ as awarded

#### Step 2: Finalization

- **Selected supplier finalized** – Locked in system
- **Prices and quantities carried forward** – Auto-populated
- **Terms captured** – Delivery, payment, warranty

#### Step 3: Document Generation

Generate:
- **Purchase Order** – For goods procurement
- **Contract** – For services or long-term agreements

#### Step 4: Data Transfer

Information transferred includes:
- Supplier details
- Item descriptions
- Quantities
- Agreed prices
- Delivery terms
- Payment terms
- Special instructions

### Benefits

- Eliminates duplicate data entry
- Ensures accuracy
- Maintains consistency
- Speeds up procurement
- Preserves audit trail

### Post-Conversion

- RFQ marked as Closed
- Link to PO/Contract maintained
- Original RFQ archived for reference

## 16. RFQ Reports & Analysis

Reporting provides procurement insight for management and continuous improvement.

### Available Reports

#### RFQs by Status

- Count and value by status
- Status distribution over time
- Aging analysis

#### Supplier Participation

- Response rates by supplier
- Average quote values
- Win/loss ratios
- Performance ratings

#### Award Analysis

- Award distribution by supplier
- Price competitiveness
- Negotiation effectiveness
- Cost savings achieved

#### Cycle Time Analysis

- Average time to quote
- Approval cycle times
- Response times
- Overall RFQ duration

#### Budget Compliance

- RFQ value vs. budget
- Variance analysis
- Spending patterns

### Report Customization

- Filter by date range, project, supplier, owner
- Export to Excel, PDF
- Schedule automated reports
- Create custom dashboards

### Usage

Reports are used for:
- Management reviews
- Performance audits
- Process improvement
- Supplier evaluation
- Budget planning

## 17. Integration with Other Modules

RFQ integrates seamlessly with other PRIZM modules for end-to-end procurement continuity.

### Suppliers Module

- Access approved supplier list
- Create new suppliers during RFQ
- Update supplier contact information
- Track supplier performance

### Projects and Budgets

- Link RFQs to projects
- Check budget availability
- Track project spending
- Allocate costs correctly

### Purchase Orders

- Convert awarded RFQs to POs
- Auto-populate PO fields
- Maintain RFQ reference
- Track PO status

### Contracts

- Generate contracts from RFQs
- Capture service terms
- Manage contract lifecycle
- Link to RFQ history

### Finance and Approvals

- Budget verification
- Approval routing
- Financial reporting
- Audit trail maintenance

### Benefits

Integration ensures:
- Consistent data across modules
- Reduced manual entry
- Improved accuracy
- Better visibility
- Streamlined workflows

## 18. Permissions & Roles

Role-based access controls RFQ actions to ensure proper governance.

### Typical Roles

#### Procurement Officer

- Create RFQs
- Add items
- Invite suppliers
- Track responses
- Conduct initial evaluation

#### Procurement Manager

- Review and approve RFQs
- Final supplier selection
- Award decisions
- Budget oversight

#### Finance Manager

- Budget verification
- Cost approval
- Financial evaluation
- Spend control

#### Administrator

- Configure RFQ settings
- Manage approval workflows
- Set up templates
- User permission management

#### Viewer / Auditor

- Read-only access
- Report generation
- Compliance review
- Audit activities

### Permission Levels

Permissions determine who can:
- Create RFQs
- Edit RFQs
- Send to suppliers
- Evaluate quotes
- Approve RFQs
- Award suppliers
- Convert to PO
- Archive RFQs

## 19. Common Procurement Scenarios

### Scenario 1: Project Material Sourcing

1. Project manager submits material request
2. Procurement creates RFQ with technical specs
3. Invites 3-5 approved suppliers
4. Evaluates quotes on price and delivery
5. Awards to best-value supplier
6. Converts to Purchase Order

### Scenario 2: Service Provider Selection

1. Department requests consulting services
2. RFQ created with scope of work
3. Suppliers submit proposals and pricing
4. Evaluation includes experience and methodology
5. Negotiation with top 2 candidates
6. Award and contract generation

### Scenario 3: Emergency Procurement

1. Urgent requirement identified
2. Quick RFQ with short deadline
3. Limited supplier pool (qualified vendors only)
4. Fast-track approval
5. Immediate award
6. Expedited PO issuance

### Scenario 4: Budget-Controlled Purchasing

1. Budget allocation approved
2. RFQ created within budget limits
3. Quote evaluation against budget
4. Finance approval required if over threshold
5. Award to cost-effective supplier
6. Budget tracking updated

## 20. Best Practices & Tips

- **Define items clearly** – Detailed specifications reduce ambiguity and ensure accurate quotes
- **Invite multiple suppliers** – Typically 3-5 suppliers for competitive pricing
- **Attach full specifications** – Complete documentation up front reduces back-and-forth
- **Monitor response deadlines** – Send reminders to suppliers as deadline approaches
- **Maintain audit completeness** – Document all decisions and communications
- **Use templates** – Standardize RFQ format for consistency
- **Set realistic deadlines** – Allow sufficient time for quality responses
- **Follow up promptly** – Quick responses maintain supplier relationships
- **Document evaluation criteria** – Transparent criteria ensure fair process
- **Keep suppliers informed** – Notify all participants of award decisions
- **Review and improve** – Analyze RFQ metrics to optimize process
- **Train users** – Ensure team understands RFQ procedures

## 21. Known Limitations / Notes

- **RFQs cannot be edited after sending** – Once sent to suppliers, core fields are locked to ensure fairness and consistency
- **Awarded RFQs cannot be deleted** – Maintains audit trail and historical record; use archive instead
- **Expired RFQs require manual closure** – System does not auto-close expired RFQs; procurement officer must review and close
- **Approval behavior depends on configuration** – Workflow varies based on organizational settings; consult administrator
- **Supplier email delivery** – System tracks sending but cannot guarantee receipt; confirm critical RFQs via phone
- **Concurrent editing** – Multiple users editing same RFQ may cause conflicts; coordination recommended
- **Document size limits** – Large file attachments may have size restrictions; contact administrator for limits
- **Browser compatibility** – Optimized for modern browsers; older browsers may have limited functionality
- **Data export limitations** – Some complex reports may require custom configuration
