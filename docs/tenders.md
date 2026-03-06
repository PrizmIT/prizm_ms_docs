# Tenders Module

## 1. Introduction

The Tenders module in the PRIZM ENERGY Admin Portal is designed to centrally manage all tender opportunities from discovery to conversion into sales opportunities. It supports manual tender entry, structured tracking, document management, analytics, and geographic visualization.

![Tenders Overview](./tenders/img/tender_list_summary_view.png)

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

![Tenders Dashboard](./tenders/img/tender_statistics_by_status.png)

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

![Tenders Navigation](./tenders/img/tender_crons_automation_list.png)

3. The system opens the Tender List page by default

### Sub-Sections

- **Tenders** – Main tender list and management
- **Sources Dashboard** – Analytics by tender source
- **SWCC Items** – Reference catalog for SWCC tenders
- **Maps** – Geographic visualization of tenders

## 5. Tender List Page

The Tender List Page provides a complete overview of all tenders in the system.

![Tender List Main View](./tenders/img/tender_list_swcc_arabic.png)

### Main Components

#### ① Add New Tender

- Button used to create a new tender record
- Opens the Add Tender form

#### ② Search & Filters

- Keyword search (tender number, title, description)

![Tender List Filters](./tenders/img/tender_list_filter_presets.png)

- Filters by:
  - Status
  - Source
  - Category
  - Date ranges (created, closing, floating)
- Filters update the table in real time

#### ③ Tenders Table

Typical columns:

![Tender List Table](./tenders/img/tender_list_summary_view.png)

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

![Add Tender Form](./tenders/img/add_tender_form.png)

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

![Tender Detail Summary View](./tenders/img/tender_detail_main_arabic.png)

### Layout Overview

#### ① Tender Summary

Displays:

- Tender Number
- Description
- Source
- Client
- Dates
- Status

#### ② Tabs

![Tender Detail View Tabs](./tenders/img/tender_detail_tabs_view.png)

- Main
- Convert to Opportunity
- Attachments
- Activity Log

#### ③ Tender with Offers

![Tender Detail with Offer Cards](./tenders/img/tender_detail_with_offer_cards.png)

#### ④ RFQ Items

![RFQ Items Tab](./tenders/img/tender_rfq_items_tab.png)

#### ⑤ BOQ Items

![BOQ Items Tab](./tenders/img/tender_boq_items_tab.png)

![BOQ Items with Sync](./tenders/img/tender_boq_items_sync_tab.png)

#### ⑥ Actions

![Tender Detail Actions](./tenders/img/tender_detail_esupply_lots.png)

- Edit Tender
- Convert to Opportunity
- Delete / Archive (permission-based)

## 8. Convert to Opportunity Tab

Used when a decision is made to pursue a tender.

### Fields

![Convert To Opportunity Form](./tenders/img/convert_to_opportunity_form.png)

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

![Tender Attachments Tab](./tenders/img/tender_attachments_with_file.png)

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

![Tender Activity Log View](./tenders/img/tender_activity_log_tab.png)

### Logged Events

- Tender creation
- Field updates
- Date changes
- Attachments added/removed
- Conversion to opportunity
- System-generated actions

### Columns

![Tender Activity Log List](./tenders/img/tender_activity_log_history.png)

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

![SWCC Items List](./tenders/img/swcc_items_number_list.png)

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

### Item Detail

![SWCC Item Detail](./tenders/img/swcc_item_tenders_detail.png)

### Use Cases

- Validate tender BOQs
- Cross-reference SWCC documentation
- Ensure item consistency

## 12. Sources Dashboard

Analytics view summarizing tender sources.

![Tender Sources Dashboard Overview](./tenders/img/sources_dashboard_overview_map.png)

### Dashboards Include

#### Top Sources

![Top Matches Bids per Source](./tenders/img/sources_top_matches_bids.png)

- Top 10 tender sources by count

#### Tenderer Performance

![Tenderer Performance Overview](./tenders/img/swcc_tenderer_performance_stats.png)

- Top awarded tenderers
- Breakdown by:
  - Award count
  - Award value

![Tenderer Performance Detail](./tenders/img/tenderer_performance_company_detail.png)

![Tenderer Participation and Awards Chart](./tenders/img/tenderer_participation_awards_timeline.png)

![Suppliers per Source](./tenders/img/source_suppliers_list.png)

### Business Value

- Identify most valuable tender platforms
- Track source effectiveness
- Support strategic decisions

## 13. Maps View

Geographical visualization of tenders.

![Geographic Tenders Map Main View](./tenders/img/maps_etimad_general_heat.png)

![Multiple Maps Overview](./tenders/img/maps_multi_region_grid.png)

### Filters

- Source Name
- Activity Name
- Client Name

### Map Features

![Interactive Map Marker Details](./tenders/img/maps_marker_popup_detail.png)

- Interactive markers
- Click marker → tender summary
- Link to tender details
- Clustered view for dense areas

![Heat Map View](./tenders/img/maps_etimad_heat_map.png)

### Use Cases

- Regional planning
- Site visit coordination
- Geographic tender distribution analysis

## 14. Advanced Tender Insights

### Tender Lifecycle & Status Evolution

Managing a tender requires understanding its progression through various stages, from floating to award.

![Top Tenderers Awarded from Etimad](./tenders/img/top_tenderers_awarded_etimad_value.png)

### Category & Business Line Breakdown

Grouping tenders by industry or business line helps in resource allocation.

![Top Tenderers Participated by Count](./tenders/img/top_tenderers_participated_count.png)

### Geographic Distribution Mapping

Strategic mapping of tender locations across regions.

![Top Tenderers Participated by Value](./tenders/img/top_tenderers_participated_value.png)

### Tender Award Process Tracking

Detailed tracking of the award lifecycle and vendor selection performance.

![Top Sources Mean Value of Participants Per Tender](./tenders/img/sources_mean_value_top.png)

### Financial & Risk Management

Tracking bank guarantees and tender fees is critical for risk mitigation.

![Bottom Sources Mean Value of Participants Per Tender](./tenders/img/sources_mean_value_bottom.png)

![Top Sources by Distribution Ratio Descending](./tenders/img/sources_distribution_ratio_desc.png)

### Deadline & Timeline Management

Monitoring closing dates and floating timelines to avoid missed opportunities.

![Top by Distribution Ratio Ascending](./tenders/img/sources_distribution_ratio_asc.png)

### User Roles & Responsibility Assignment

Assigning tenders to the right personnel ensures accountability.

![Top Mismatches Bids per Source](./tenders/img/sources_mismatches_bids.png)

## 15. Best Practices & Tips

![Top Tenderers Performance](./tenders/img/top_tenderers_awarded_etimad_value_list.png)

- Always verify closing dates
- Convert to opportunity only when approved
- Keep attachments updated
- Use sources consistently for accurate analytics
- Review activity logs for audit and accountability
- Maintain consistent naming conventions
- Update tender status regularly
- Archive completed tenders appropriately
