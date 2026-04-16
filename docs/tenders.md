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

**Field Guide:**

1. **Tender Number** - Unique tender identifier
2. **Tender Description** - Detailed tender description
3. **Status** - Active or inactive status
4. **Source** - Tender source platform (e.g., Etimad, eSupply)
5. **Client** - Issuing organization
6. **Floating Date** - Tender publication date
7. **Closing Date** - Submission deadline
8. **Fees** - Tender participation fees
9. **Purchase Link** - External tender URL
10. **Tender Type** - Tender classification
11. **Offer Title** - Bid/offer title in offers table
12. **Tenderer Name** - Bidding company name in offers table

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

**Field Guide:**

1. **Opportunity Name** - Name for the new opportunity
2. **Client** - Customer or organization name
3. **Estimated Value** - Expected contract revenue
4. **Probability** - Win likelihood percentage
5. **Expected Close Date** - Target closing date
6. **Assigned To** - Responsible team member

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

## 15. Automated Tender Scraping

The Tenders module includes a powerful **automated scraping engine** that fetches tender data from multiple external sources without manual intervention.

### Cron Jobs

Seven automated cron jobs run on configurable intervals:

| Cron Job | Source | Description |
|----------|--------|-------------|
| **DEWA Status** | DEWA | Scrapes the DEWA tender documents page for new and updated tenders |
| **DEWA Tenders** | DEWA | Scrapes DEWA tender opening results (bidders, prices, awards) |
| **7x Oracle** | 7x | Fetches tenders from the 7x Oracle procurement system |
| **Etimad Documents** | Etimad | Fetches tender documents from Saudi Etimad platform |
| **Etimad Notifications** | Etimad | Fetches notification alerts from Etimad (piggybacks on document fetch) |
| **Etimad Details** | Etimad | Scrapes detailed information for each Etimad tender |
| **DEWA Info Mailbox** | Outlook | Fetches tenders forwarded to the DEWA info mailbox via Outlook API |

### Scraper Monitor

Navigate to **Tenders > Scraper Monitor** to oversee all scraping operations:

- View status of each cron job (Success, Failed, Running)
- See last run time and last result message
- **Configurable intervals** — Change scraping frequency (5min to 24h) directly in the grid
- **Manual run** — Trigger any cron job on-demand
- **Cron logs** — View full execution history for troubleshooting
- **Activity logs** — Track scraping activity per source

### AI-Assisted Scraping

The scraper includes:

- **AI Captcha solving** — Automatically solves captchas encountered during scraping
- **PDF parsing** — Extracts data from tender PDF documents
- **OCR** — Reads scanned tender documents using Tesseract OCR
- **Arabic text processing** — Stemming and analysis for Arabic tender content
- **Browser automation** — Selenium WebDriver for dynamic page scraping

## 16. Etimad Notifications

The module provides **real-time Etimad tender notifications** directly in the admin header navbar.

### Notification Features

- **Bell icon** in the top navigation bar with unread count badge
- **Auto-polling** every 60 seconds for new notifications
- **Dropdown panel** showing the last 20 notifications (displayed in RTL Arabic)
- **Mark as read** — Individual or bulk "Mark all read"
- **Smart linking** — System matches notifications to tenders by tender ID, tender ID string, or tender number, with fallback to the Etimad URL

### Notification Matching Logic

1. Direct `tender_id` match (set during cron insert)
2. Match by `tenderIdString` extracted from notification link
3. Match by `tender_number` (Etimad internal reference)
4. Fallback: Direct link to Etimad website

!!! note "Permission Required"
    Etimad notifications are visible to administrators by default. Non-admin users require the `etimad_notifications` view permission.

## 17. Permission-Layered Document Access

Tender documents are organized into **permission-controlled folders** integrated with SharePoint:

| Folder | Permission Required | Description |
|--------|-------------------|-------------|
| **01 - Customer Documents** | `tenders` | Client-facing tender documents |
| **02 - Internal Technical** | `tenders_technical` | Internal technical analysis and specifications |
| **03 - Internal Commercial** | `tenders_commercial` | Pricing, costing, and commercial documents |
| **05 - Dispatch** | `tenders_commercial` | Submission and dispatch records |

This layered approach ensures that sensitive commercial and technical information is only accessible to authorized staff, while customer documents remain available to the broader tender team.

## 18. Portal Credentials

The module adds a **Portal Credentials** tab to customer profiles (admin only), allowing storage of login credentials for external tender portals associated with each client.

## 19. Permissions Reference

The module uses **5 permission groups**:

| Permission Group | Capabilities | Description |
|-----------------|-------------|-------------|
| **tenders** | view_own, view (global), create, edit, delete | Main tender access |
| **tenders_technical** | view (global) | Access to Internal Technical documents |
| **tenders_commercial** | view (global) | Access to Internal Commercial + Dispatch documents |
| **etimad_notifications** | view | Receive Etimad notification alerts in navbar |
| **etimad_own_credentials** | view (Own Credentials) | Use personal Etimad credentials for manual operations |

## 20. Global Search

Tenders are included in the system-wide global search. Search by:

- **Tender Number** — Unique tender identifier
- **Tender Description** — Description of the tender scope

Results are grouped by tender number and link directly to the tender detail view.

## 21. Best Practices & Tips

![Top Tenderers Performance](./tenders/img/top_tenderers_awarded_etimad_value_list.png)

- Always verify closing dates before submission
- Convert to opportunity only when approved
- Keep attachments updated in the correct document layer
- Use sources consistently for accurate analytics
- Review activity logs for audit and accountability
- Maintain consistent naming conventions
- Update tender status regularly
- Monitor the **Scraper Monitor** for failed cron jobs
- Check **Etimad Notifications** regularly for updates from Saudi tenders
- Archive completed tenders appropriately
- Ensure portal credentials are up to date for automated scraping
