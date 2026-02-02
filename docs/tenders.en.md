# Tenders Module

## 1. Introduction

The Tenders module in the PRIZM ENERGY Admin Portal is designed to centrally manage all tender opportunities from discovery to conversion into sales opportunities. It supports manual tender entry, structured tracking, document management, analytics, and geographic visualization.

This module is typically used by:

- Business Development teams
- Tender & Bid Management teams
- Sales & Opportunity Managers
- Administrators and Management

Key capabilities include:

- Centralized tender registry
- Advanced filtering and tracking
- Tender-to-Opportunity conversion
- Document attachment management
- Activity auditing
- SWCC item catalog
- Source analytics dashboards
- Map-based tender visualization

## 2. Module Overview

The Tenders module provides comprehensive tools for:

- Managing tender opportunities
- Tracking tender lifecycle
- Converting tenders to sales opportunities
- Analyzing tender sources
- Geographic visualization
- Document management
- Audit trail maintenance

## 3. Navigation Structure

The Tenders module is organized as follows:

```
Tenders
├─ Tender List
├─ Sources Dashboard
├─ SWCC Items
└─ Maps
```

## 4. Navigation to Tenders

### How to Access

1. Log in to the PRIZM ENERGY Admin Portal
2. From the left sidebar, click **Tenders**
3. The system opens the Tender List page by default

### Sub-Sections

- **Tenders** – Main tender list and management
- **Sources Dashboard** – Analytics by tender source
- **SWCC Items** – Reference catalog for SWCC tenders
- **Maps** – Geographic visualization of tenders

## 5. Tender List Page

The Tender List Page provides a complete overview of all tenders in the system.

### Main Components

#### ① Add New Tender

- Button used to create a new tender record
- Opens the Add Tender form

#### ② Search & Filters

- Keyword search (tender number, title, description)
- Filters by:
  - Status
  - Source
  - Category
  - Date ranges (created, closing, floating)
- Filters update the table in real time

#### ③ Tenders Table

Typical columns:

- Tender Number
- Tender Title / Description
- Source
- Client / Issuer
- Category
- Opening Date
- Closing Date
- Status

Features:

- Column sorting
- Pagination
- Adjustable page size

#### ④ Row Actions

- Click tender number/title → Tender Detail View
- Optional quick actions:
  - Edit
  - Delete (permission-based)

## 6. Add Tender Page

Used to manually register a new tender.

### Form Fields

#### Basic Information

- **Tender Title** (required)
- **Tender Number / Reference**
- **Source** (Etimad, SWCC, Manual, etc.)
- **Client / Issuing Authority**
- **Category / Business Line**
- **Location / Region**

#### Dates

- **Floating Date**
- **Closing Date** (required)

#### Financial / Reference

- **Fees**
- **Purchase Link**
- **Tender Type**

#### Description

- Tender scope and notes
- Internal remarks

#### Offers Table

- Offer Title
- Tenderer Name
- Total Price
- Delivery Completion
- Bank Guarantee
- Remarks
- Supports multiple rows

### Actions

- **Submit** – Saves tender
- **Cancel** – Discards changes

## 7. Tender Detail View

Central workspace for a single tender.

### Layout Overview

#### ① Tender Summary

Displays:

- Tender Number
- Description
- Source
- Client
- Dates
- Status

#### ② Actions

- Edit Tender
- Convert to Opportunity
- Delete / Archive (permission-based)

#### ③ Tabs

- Convert to Opportunity
- Attachments
- Activity Log
- (Optional) SWCC Items linkage

## 8. Convert to Opportunity Tab

Used when a decision is made to pursue a tender.

### Fields

- **Opportunity Code**
- **Responsible Employee**
- **Field / Department**
- **Priority**
- **Job Type**
- **Estimated Value** (if applicable)

### Behavior

Clicking **Convert**:

- Creates a linked Opportunity record
- Updates tender status
- Prevents duplicate conversions
- After conversion, a link to the opportunity is shown

## 9. Attachments Tab

Central repository for all tender documents.

### Features

- Upload files (PDF, DOCX, XLSX, images)
- Drag & drop support
- Download attachments
- Delete attachments (permission-based)

### Best Practices

- Upload original RFP documents
- Attach clarifications, addendums
- Keep filenames meaningful
- Use latest versions only

## 10. Activity Log Tab

Provides a full audit trail.

### Logged Events

- Tender creation
- Field updates
- Date changes
- Attachments added/removed
- Conversion to opportunity
- System-generated actions

### Columns

- Timestamp
- Tender Number
- Action
- Source
- User (Full Name)

### Filters

- Date range
- Created / Updated dates

## 11. SWCC Items List

Reference catalog for SWCC-standard item numbers.

### Table Columns

- Item Number
- Item Description
- Item Count
- Related Tender Numbers

### Features

- Advanced filtering
- Search by item number or description
- Color-coded counters
- Clickable item and tender links

### Use Cases

- Validate tender BOQs
- Cross-reference SWCC documentation
- Ensure item consistency

## 12. Sources Dashboard

Analytics view summarizing tender sources.

### Dashboards Include

#### Top Sources

- Top 10 tender sources by count

#### Tenderer Performance

- Top awarded tenderers
- Breakdown by:
  - Award count
  - Award value

### Business Value

- Identify most valuable tender platforms
- Track source effectiveness
- Support strategic decisions

## 13. Maps View

Geographical visualization of tenders.

### Filters

- Source Name
- Activity Name
- Client Name

### Map Features

- Interactive markers
- Click marker → tender summary
- Link to tender details
- Clustered view for dense areas

### Use Cases

- Regional planning
- Site visit coordination
- Geographic tender distribution analysis

## 14. Best Practices & Tips

- Always verify closing dates
- Convert to opportunity only when approved
- Keep attachments updated
- Use sources consistently for accurate analytics
- Review activity logs for audit and accountability
- Maintain consistent naming conventions
- Update tender status regularly
- Archive completed tenders appropriately
