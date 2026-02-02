# PRIZM Opportunities Module

## 1. Introduction

The Opportunities module in PRIZM ENERGY's ERP system is designed to help sales and operations teams manage prospective business deals from initial contact through to project initiation. Each opportunity represents a potential revenue‑generating initiative, such as a client request for proposal (RFP), tender, or an internal business development idea.

The module provides a structured way to capture opportunity details, track progress across defined stages, obtain approvals, estimate costs, and ultimately convert successful opportunities into projects or budgets. By consolidating the sales pipeline in one place, the module improves visibility, supports forecasting, and ensures that opportunities follow consistent business rules.

## 2. Module Overview

The PRIZM Opportunities module provides comprehensive tools for:

- Managing prospective business deals and opportunities
- Tracking progress through defined sales stages
- Capturing customer and partner information
- Developing cost estimates and pricing
- Managing approval workflows
- Converting opportunities to projects or budgets
- Forecasting revenue and pipeline health
- Documenting activities and communications

## 3. Navigation Structure

The PRIZM Opportunities module is organized as follows:

```
PRIZM Opportunities
├─ Opportunities Dashboard
├─ Opportunities Pipeline / List
├─ Opportunity Creation
├─ Opportunity Stages & Statuses
├─ Opportunity Details View
├─ Opportunity Activities & Follow-ups
├─ Opportunity Estimates & Costing
├─ Opportunity Products / Services
├─ Documents & Attachments
├─ Opportunity Approval Workflow
├─ Opportunity Conversion (to Project / Budget)
└─ Opportunity Reports & Forecasting
```

## 4. Navigation to Opportunities

### How to Access

You can access the Opportunities module through the Admin Portal's main navigation:

1. From the main menu, select **Sales** or **Projects** (depending on your configuration)
2. Choose **Opportunities**
3. A list or pipeline view of existing opportunities appears

### Permissions

Users with appropriate permissions can:
- Create opportunities
- Edit opportunities
- View opportunity records
- Approve opportunities (for designated approvers)

Administrators can configure permissions to restrict who may create, approve, or convert opportunities.

## 5. Opportunities Dashboard

The dashboard provides a high‑level snapshot of your pipeline.

### Dashboard Components

#### Summary Cards

Showing counts of:
- Open opportunities
- Pending approval
- Won opportunities
- Lost opportunities

#### Pipeline Funnel or Chart

Illustrating the distribution of opportunities across stages

#### Key Performance Indicators (KPIs)

- Total estimated value
- Projected revenue
- Expected closing dates
- Win/loss ratios
- Average cycle time

#### Filters

Segment the view by:
- Salesperson
- Business sector
- Partner
- Country
- Priority level
- Date ranges

### Using the Dashboard

Use the dashboard to:
- Monitor overall performance
- Identify bottlenecks
- Focus on high‑priority deals
- Track team performance
- Review pipeline health

## 6. Opportunities Pipeline / List

The pipeline or list view provides a sortable and filterable overview of all opportunities.

### Key Features

#### Pipeline Columns by Stage

- Opportunities are grouped into columns representing stages
- Typical stages: Initiation, Site Visit, Resources Inquiry, Estimation, Review, Submission
- Drag opportunities between stages when progression is permitted

#### List View

Displays opportunities in a tabular format with columns:
- Opportunity Name
- Customer/Partner
- Start/End Dates
- Current Stage
- Status
- Priority
- Assigned Owner
- Estimated Value

#### Search & Filters

Quickly find opportunities by:
- Name
- Partner
- Responsible staff
- Stage
- Status
- Business sector
- Country
- Cost centre

#### Bulk Actions

Depending on permissions, select multiple opportunities to:
- Change responsible owner
- Update statuses
- Export data
- Assign team members

### View Options

- **Pipeline view** – Visual management with stage columns
- **List view** – Detailed filtering and reporting

## 7. Opportunity Creation

Creating a new opportunity captures essential information about a potential deal.

### Creation Steps

#### Step 1: Start Creation

Click **Add Opportunity** from the pipeline or list view

#### Step 2: Fill in Key Details

##### Basic Information

- **Opportunity Name** (required) – Clear title describing the potential project or deal
- **Opportunity Type** – Classifies the deal (e.g., new project, service, product sale)
- **Start and End Dates** – Initial timeline for the opportunity
- **Expiry Date** – The date by which the opportunity is expected to close

##### Business Assignment

- **Cost Centre / Business Sector** – Associates the opportunity with the appropriate business unit
- **Partner / Customer** – Link to an existing customer or lead
- **Responsible Salesperson** (required) – Assign a staff member who will manage the opportunity
- **Priority** – Indicates urgency or importance (Low, Medium, High)

##### Financial Estimates

- **Estimated Price** – Optional monetary value for forecasting revenue
- **Client Price** – Expected client-facing price
- **Estimated Hours** – Approximate effort if opportunity requires time‑based work

##### Description

- **Summary / Description** – Provide background information, client needs, and objectives

#### Step 3: Save

- Mandatory fields must be completed before saving
- Opportunity is created in the first stage
- Typically marked as **Draft** until further actions are taken

### After Creation

You can:
- Upload documents
- Add products/services
- Schedule activities
- Assign team members
- Begin estimation

## 8. Opportunity Stages & Statuses

Opportunities progress through a series of stages, each representing a milestone in the sales cycle.

### Typical Stages

#### 1. Initiation

Capturing initial details and qualifying the opportunity

#### 2. Site Visit

Performing on‑site assessments or inspections

#### 3. Resources Inquiry

Identifying resource requirements and availability

#### 4. Estimation

Developing cost and time estimates

#### 5. Review

Obtaining managerial or peer review

#### 6. Submission

Finalizing proposals and submitting offers

### Stage Statuses

At each stage, an opportunity can have one of several statuses:

| Status | Description |
|--------|-------------|
| Draft / Open | Early stages before serious work begins |
| In Progress | Actively working through tasks or preparing proposals |
| Pending Approval | Awaiting review or authorization; changes may be locked |
| Approved / Won | Opportunity has been accepted; ready for conversion |
| Lost / Cancelled | Opportunity was not successful or was withdrawn |

### Stage Progression

- Stages advance sequentially
- Status movement may include optional steps
- Opportunities might be moved back to an earlier stage if additional information is required
- Some statuses are marked as **final**, meaning the opportunity cannot progress further in that stage
- Others are **optional**, allowing the opportunity to skip them if not needed

### Configuration

Administrators configure:
- Which statuses are optional or final
- Who may approve transitions
- Stage sequence and requirements

## 9. Opportunity Details View

The detail page provides a comprehensive view of an individual opportunity.

### General Information

The basic data entered during creation plus any updates:
- Responsible salesperson
- Cost centre
- Partner
- Business sector
- Estimated price/hours
- Expiry date
- Progress percentage

### Stage and Status Timeline

A chronological record of:
- Stage transitions
- Approvals
- Rejections
- Notes

This audit trail helps track how the opportunity has evolved.

### Tabs or Sections

#### Activities

- Phone calls
- Meetings
- Emails
- Tasks
- Calendar events associated with the opportunity

#### Products / Services

Items or milestones with:
- Quantities
- Unit prices
- Unit of measure
- Estimated totals

#### Estimates / Costing

Detailed job estimations and cost breakdowns, including:
- Margin
- Discount
- Submission price

#### Documents & Attachments

Uploaded files such as:
- Proposals
- Specifications
- Drawings
- Correspondence

#### Notes & Discussions

- Internal notes
- Comments
- Discussions among team members

#### Members

List of staff members collaborating on the opportunity

#### Approvals

- Current approval state
- Assigned approvers
- Actions taken

### Action Buttons

The detail view provides buttons to:
- Update information
- Change stages
- Request approval
- Convert the opportunity to a project/budget (once all required approvals are obtained)

## 10. Opportunity Activities & Follow‑ups

To manage engagement with partners or clients effectively, the module records all activities related to an opportunity.

### Activity Types

#### Tasks and Calendar Events

- Assign tasks such as scheduling site visits
- Preparing proposals
- Following up on client inquiries
- Each task can have:
  - Due date
  - Responsible staff member
  - Reminders

#### Notes

- Log conversation summaries
- Meeting outcomes
- Internal comments
- Only visible to internal staff

#### Discussions

- Create discussion threads to collaborate with team members
- Replies are threaded
- Files can be attached

#### Emails

- Integrate with email systems
- Fetch opportunity‑related emails
- Link them directly to the opportunity record

#### Pinned Opportunities

Mark important opportunities as pinned for quick access

### Benefits

Keeping activities up to date ensures that:
- Team members stay informed
- Deadlines are met
- Opportunity progresses smoothly
- Communication history is preserved

## 11. Opportunity Estimates & Costing

During the estimation stage, you can develop cost estimates for the opportunity.

### Job Estimation

Create one or more estimates that outline:
- Resources required
- Materials needed
- Labor requirements

Each estimate includes:
- List of items
- Quantities
- Unit of measure
- Unit price
- Total price
- Margin
- Discount
- Additional notes

### Item Specifications

Define technical specifications for each estimated item:
- Size
- Weight
- Power rating
- Units and codes

### Currency & Pricing

- Specify currency for each estimate
- Convert or update prices as needed
- Support for multiple currencies

### Summary Figures

View:
- Total estimated cost
- Total submission price
- Client price for comparison
- Profit margins

### Purpose

Estimates help:
- Gauge the opportunity's profitability
- Required for approval
- Included in proposals or budgets

## 12. Opportunity Products / Services

Opportunities may include products or services offered to the customer.

### Features

#### Add Products or Milestones

List deliverables with:
- Descriptions
- Quantities
- Unit prices
- Due dates

#### Define Services

Specify:
- Service offerings
- Contract terms
- Consultation hours

#### Track Progress

- Assign colors or indicators to milestones
- Visualize completion

#### Calculate Values

- Automatically compute line totals
- Overall totals

### Benefits

Organizing products and services helps ensure that:
- Proposals are accurate
- All customer requirements are addressed
- Revenue is properly forecasted

## 13. Documents & Attachments

Document management within the Opportunities module keeps all related files in one place.

### Upload Files

Attach:
- Proposals
- Specifications
- Drawings
- Vendor quotations
- Supporting documents

Files can be:
- Visible to internal staff only
- Shared with customers

### External Links

Store external file links (e.g., from cloud storage or collaboration tools)

### Versioning

- Update documents as revisions occur
- Retain history of previous versions

### Notes & Descriptions

Add subject lines or descriptions to describe each file's purpose

### Lifecycle

Files remain associated with the opportunity throughout its lifecycle and are automatically transferred when the opportunity converts to a project.

## 14. Opportunity Approval Workflow

Approvals enforce compliance with business policies and ensure that only qualified opportunities move forward.

### Key Aspects

#### Approval Stages

Specific statuses within each stage can require approval before progressing

Example: Moving from Estimation to Review may require approval from finance or management

#### Approvers

- Designate staff members or teams as approvers
- System supports multiple approvers
- Optional approvers depending on opportunity complexity

#### Templates & Conditions

Administrators can create approval templates defining:
- Which statuses require approval
- Who approves them
- Conditions such as value thresholds or partner type

Templates help standardize approvals across opportunities

#### Approval Actions

Approvers can:
- Approve
- Reject
- Request changes

When rejected, the opportunity returns to a previous status with notes explaining the decision

#### Audit Trail

The system records:
- Who approved or rejected each status
- Timestamps
- Comments

#### Locking

Fields and activities may be locked while awaiting approval to prevent unauthorized changes

### Importance

Approvals are essential to:
- Maintain governance
- Ensure qualified opportunities progress
- Only after all required approvals are obtained can an opportunity be converted to a project or budget

## 15. Opportunity Conversion (to Project / Budget)

Once an opportunity is Won and approved, it can be converted into a project or budget.

### Conversion Process

#### Eligibility Check

The opportunity must have:
- Final approved status
- Required approvals completed
- Estimates completed

Opportunities marked as Lost or Cancelled cannot be converted

#### Data Transfer

Key information is copied to the new project or budget:
- Client details
- Description
- Estimated costs
- Milestones
- Activities
- Documents

This avoids re‑entering data and ensures continuity

#### Project Creation

- Creates a new project record in the Projects module
- Links back to the opportunity
- Opportunity record is flagged as converted
- Further edits may be restricted

#### Budget Creation

- Optionally generate budgets from the estimates
- Producing cost items for procurement or financial planning

#### Audit & Locking

- After conversion, certain opportunity fields are locked
- Preserves historical accuracy
- Fields locked may include: status, price, dates

### Significance

Conversion marks the culmination of the opportunity lifecycle and triggers the start of execution activities in other modules.

## 16. Opportunity Reports & Forecasting

Reporting tools help managers understand pipeline health and revenue projections.

### Report Types

#### Stage & Status Reports

- View counts and values of opportunities at each stage and status
- Identify stages with excessive delays or high attrition

#### Win/Loss Analysis

Analyze reasons for lost opportunities:
- Price
- Competition
- Timing
- Other factors

#### Forecasting

- Calculate expected revenue
- Weight opportunities based on probability of winning
- Anticipated closing date

#### Custom Filters

Generate reports by:
- Country
- Business sector
- Sales team
- Partner

Export data for further analysis in spreadsheets or business intelligence tools

#### Graphical Dashboards

Use charts and graphs to visualize:
- Trends over time
- Monthly won deals
- Average cycle duration
- Pipeline velocity

### Benefits

Reports empower leadership to:
- Make informed decisions
- Allocate resources
- Forecast revenue
- Identify improvement areas

## 17. Integration with Other Modules

The Opportunities module connects seamlessly with other components of the ERP system.

### Customers & Leads

- Opportunities can be created from customer records or lead conversions
- Customer information (contact details, organization) is inherited

### Projects

- Upon conversion, a project is created with all relevant data
- Project tasks, milestones, and budgets mirror those defined in the opportunity

### Budgets

- Cost estimates and product/service items feed directly into budget management
- Budgets can be reviewed and approved separately

### Tenders & RFQs

- For government or large corporate tenders
- Opportunities capture tender details and track submission deadlines
- Enabling alignment with procurement processes

### Resource Management

- Link resource inquiries to capacity planning
- Track whether resources (personnel or equipment) are available for the proposed dates

### Emails & Collaboration Tools

- Integration with email systems
- Collaboration platforms (e.g., Microsoft Teams)
- Fetch emails, store them, and manage documents via channels

### Benefits

These integrations ensure:
- Continuity of information across the enterprise
- Reduce duplication of effort
- Consistent data across modules

## 18. Permissions & Roles

User roles determine what actions each person can perform.

### Common Roles

| Role | Permissions |
|------|-------------|
| Sales Representatives | Create opportunities, update details, add notes, upload documents, progress opportunities through early stages |
| Responsible Owners | Assigned to oversee progress, coordinate tasks, update estimates, assign team members |
| Approvers | Managers or designated staff who can approve or reject opportunities at specific stages |
| Administrators | Configure stages, statuses, approval templates, permissions, and integration settings; can override restrictions |
| Viewers / Auditors | View opportunities and associated documents for monitoring and compliance; cannot edit |

### Best Practices

Administrators should define roles carefully to ensure:
- Data integrity
- Compliance with internal controls
- Appropriate access levels

## 19. Common Sales Scenarios

Below are examples of how sales teams might use the Opportunities module.

### Scenario 1: Inbound Inquiry

1. A prospective client submits a request via the website
2. A salesperson creates an opportunity
3. Schedules a site visit
4. Moves it to the Resources Inquiry stage to determine required manpower and equipment
5. After preparing estimates, they request approval
6. Once approved, submit a proposal

### Scenario 2: Existing Customer Upsell

1. A project manager identifies an upsell opportunity with an existing client
2. They create a new opportunity linked to the customer
3. Estimate additional work
4. Use quick approvals because relationship history reduces risk

### Scenario 3: Tender Response

1. The organization plans to bid on a government tender
2. The opportunity captures:
   - Tender documents
   - Submission deadlines
   - Required bonds
   - Multiple approval stages
3. After final submission, the opportunity awaits the tender result
4. Marked as Won or Lost accordingly

### Scenario 4: Cancelled Opportunity

1. During estimation, the client decides to postpone the project
2. The opportunity is moved to the Cancelled status
3. Notes record the reason
4. Record is retained for potential future reactivation

These scenarios illustrate how the module supports diverse sales activities.

## 20. Best Practices & Tips

- **Keep Opportunities Up to Date** – Regularly update stages, statuses, and estimates; accurate data improves forecasting and reporting
- **Use Notes and Discussions** – Document meeting outcomes, key decisions, and client feedback; this history is invaluable when handing opportunities to colleagues or auditors
- **Leverage Approval Templates** – Configure templates to automate who approves which stages based on opportunity value, type, or partner
- **Attach Relevant Documents Early** – Uploading proposals, drawings, and specifications early makes collaboration easier and ensures everyone has the latest version
- **Monitor Expiry Dates** – Use expiry and start/end dates to manage follow‑ups and avoid missing submission deadlines
- **Pin High‑Priority Opportunities** – Pin important deals so they appear at the top of your list
- **Standardize Naming Conventions** – Use consistent naming patterns for opportunities to improve searchability
- **Review Pipeline Regularly** – Schedule regular pipeline reviews to identify stalled opportunities
- **Track Win/Loss Reasons** – Document why opportunities are won or lost to improve future performance
- **Collaborate with Team Members** – Use discussions and task assignments to keep everyone aligned

## 21. Known Limitations / Notes

- **Deletion Restrictions** – Once an opportunity is converted to a project or budget, it cannot be deleted and certain fields become locked to preserve the audit trail
- **Stage Sequence** – Stages progress in a predetermined order; skipping stages or revisiting previous ones may require administrator intervention
- **Approval Dependency** – Opportunities cannot advance beyond approval‑required statuses without the designated approver's action
- **Customization Scope** – The number of stages, statuses, and approval templates can be configured by administrators but cannot be changed by regular users
- **Integration Configurations** – Email and collaboration integrations require setup by IT administrators
- **Data Sensitivity** – User roles and permissions must be carefully managed to control access to opportunities and associated documents
- **Browser Support** – The module is optimised for modern browsers; outdated browsers may not display interactive features correctly
- **Concurrent Editing** – Multiple users editing the same opportunity simultaneously may cause conflicts; system implements locking mechanisms
