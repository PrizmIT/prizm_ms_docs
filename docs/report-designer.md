# Report Designer

## 1. Introduction

The **Report Designer** is a WYSIWYG (What You See Is What You Get) report builder integrated into the Prizm Management System. It enables users to design custom report layouts, connect to database sources, bind data fields visually, and export polished reports — all from within the browser.

### Key Capabilities

- Connect to MySQL databases and other data sources (PostgreSQL, SQL Server, REST API, GraphQL, JSON, CSV, Excel)
- Design custom report layouts with headers, footers, and detail rows
- Bind data fields directly to the report canvas via drag-and-drop
- Preview reports with live data from the database
- Print and export reports (PDF, HTML, Excel, CSV, Word)
- Auto-save for crash recovery

## 2. Module Overview

The Report Designer module provides comprehensive tools for:

- Configuring data connections and datasets
- Creating and managing report templates
- Designing reports with a full visual editor
- Previewing reports with real-time data
- Exporting reports in multiple formats
- Managing report lifecycle (draft, published, archived)

## 3. Navigation Structure

The Report Designer module is organized as follows:

```
Report Designer
├─ Manage Reports
└─ Settings
    ├─ Connections
    ├─ Datasets
    └─ General
```

## 4. Navigation to Report Designer

### How to Access

1. Log in to the Prizm Management System
2. From the left sidebar, click **Report Designer**
3. Sub-menu items appear:
    - **Manage Reports** — Main report list with AG Grid
    - **Settings** — Connections, Datasets, and General configuration

## 5. Settings: Connections

**Path:** Report Designer > Settings > Connections

![Settings Connections](report-designer/img/settings_connections.png)

Connections define **where** your data lives — database servers, API endpoints, or file sources. Each connection stores credentials securely on the server (never sent to the browser).

**Screen Elements:**

| # | Element | Description |
|---|---------|-------------|
| 1 | **Connections Tab** | Currently active settings tab |
| 2 | **Datasets Tab** | Switch to dataset management |
| 3 | **General Tab** | Switch to general settings |
| 4 | **+ New Connection** | Create a new data connection |
| 5 | **Type Filter** | Filter connections by source type |
| 6 | **Status Filter** | Filter by active/inactive status |
| 7 | **Reset** | Clear all filters |

### Creating a Connection

#### Step 1: Select Source Type

Click **+ New Connection** to open the connection wizard.

![Connection Wizard - Source Type](report-designer/img/connection_wizard_source_type.png)

Choose from 9 supported source types:

| Category | Source Types |
|----------|-------------|
| **Databases** | MySQL, PostgreSQL, SQL Server |
| **APIs** | REST API, GraphQL |
| **Files** | JSON File, CSV File, Excel File |
| **Other** | In-Memory |

#### Step 2: Connection Details

![Connection Wizard - Details](report-designer/img/connection_wizard_details.png)

For MySQL connections, fill in:

| Field | Description |
|-------|-------------|
| **Name** | A descriptive name (e.g., "Production MySQL") |
| **Description** | Optional notes about this connection |
| **Host** | Database server address (e.g., `localhost`) |
| **Port** | Default `3306` for MySQL |
| **Database** | Database name |
| **Username** | Database credentials |
| **Password** | Database credentials (stored server-side only) |
| **SSL** | Disabled / Required / Preferred |

#### Step 3: Test and Save

1. Click **Test Connection** — must show a green checkmark
2. Click **Finish** to save the connection

### Editing a Connection

- Click the **pencil icon** in the grid row
- The wizard opens pre-filled at the Connection Details step

### Deleting a Connection

- Click the **trash icon** in the grid row
- If any datasets reference this connection, deletion is **blocked** with a warning showing the linked dataset names

---

## 6. Settings: Datasets

**Path:** Report Designer > Settings > Datasets

![Settings Datasets](report-designer/img/settings_datasets.png)

Datasets define **what** data to fetch from a connection. Each dataset stores a query, field mappings, and references a connection.

**Screen Elements:**

| # | Element | Description |
|---|---------|-------------|
| 1 | **+ New Dataset** | Create a new dataset |
| 2 | **Actions** | Edit (pencil) and Delete (trash) icons per row |
| 3 | **Name** | Dataset name (bold) |
| 4 | **Connection** | Linked connection name |
| 5 | **Type** | SQL, REST, GraphQL, etc. |
| 6 | **Reports** | Number of reports currently using this dataset |

### Creating a Dataset

Click **+ New Dataset** to open the 3-step wizard.

#### Step 1: Define

![Dataset Wizard - Define](report-designer/img/dataset_wizard_define.png)

**Field Guide:**

1. **Dataset Name** — Required, must be unique (e.g., "Staff Members", "Tasks Dataset")
2. **Description** — Optional notes about the dataset
3. **Connection** — Select from saved connections dropdown
4. **Test Connection** — Must pass before the query section unlocks
5. **SQL Query** — Write your SELECT query in the dark code editor
6. **Execute Query** — Must succeed to proceed; preview table shows first rows

#### Step 2: Fields

- Auto-populated from query results
- Check/uncheck fields to include in the dataset
- Edit field names, data types, and display labels
- Add calculated fields if needed

#### Step 3: Preview

- Data table with selected fields
- Configuration summary
- Click **Finish** to save

### Grid Columns

| Column | Description |
|--------|-------------|
| **Name** | Dataset name (bold) |
| **Connection** | Linked connection name |
| **Description** | Optional description |
| **Type** | SQL, REST, GraphQL, etc. |
| **Reports** | Number of reports using this dataset |
| **Active** | Active status |

---

## 7. Managing Reports

**Path:** Report Designer > Manage Reports

![Manage Reports](report-designer/img/manage_reports.png)

The main reports page displays all saved reports in an AG Grid table.

**Screen Elements:**

| # | Element | Description |
|---|---------|-------------|
| 1 | **+ New Report** | Opens an empty designer canvas |
| 2 | **Status Filter** | Filter by All, Draft, or Published |
| 3 | **Category Filter** | Filter by report category |
| 4 | **From Date** | Filter by creation date range (start) |
| 5 | **To Date** | Filter by creation date range (end) |
| 6 | **Status Dropdown** | Additional status filtering |
| 7 | **Reset** | Clear all filters |
| 8 | **Actions** | Per-report actions: Edit (pencil), Preview (eye), Delete (trash) |
| 9 | **Report Name** | Click to open the report |
| 10 | **Status** | Draft or Published badge |

### Report Actions

| Action | Icon | Description |
|--------|------|-------------|
| **Edit** | Pencil | Opens the designer with this report loaded |
| **Preview** | Eye | Opens the report viewer with live data |
| **Delete** | Trash | Soft-deletes the report (can be recovered) |

---

## 8. Creating a New Report

1. Go to **Manage Reports**
2. Click **+ New Report**
3. The designer opens with an empty canvas
4. Add a dataset (see [Adding Data to a Report](#10-adding-data-to-a-report))
5. Drag fields or components onto the canvas
6. Click **Save** (see [Saving a Report](#12-saving-a-report))

---

## 9. The Designer Canvas

![Designer Canvas](report-designer/img/designer_canvas.png)

The designer is the core visual editor with multiple panels and tools.

**Screen Elements:**

| # | Element | Description |
|---|---------|-------------|
| 1 | **Menu Bar** | File, Edit, View, Insert, Format, Help menus |
| 2 | **Toolbar** | Quick-access buttons: New, Open, Save, Undo/Redo, Cut/Copy/Paste, Font controls, Bold/Italic/Underline, Alignment, Colors, Zoom |
| 3 | **Left Panel Tabs** | Toolbox, Data, Outline |
| 4 | **Toolbox** | Draggable components (TextBox, Image, Line, Rectangle, Ellipse, Table, Chart, Barcode, Gauge, Subreport, CheckBox) |
| 5 | **Page Header** | Band that repeats on every page |
| 6 | **Report Header** | Band that appears on the first page only |
| 7 | **Detail** | Band that repeats for each data row |
| 8 | **Report Footer** | Band that appears on the last page only |
| 9 | **Page Footer** | Band that repeats on every page |
| 10 | **Right Panel** | Properties, Groups, Params, Styles tabs |
| 11 | **Design / Preview** | Switch between design mode and live preview |

### Menu Bar Options

| Menu | Options |
|------|---------|
| **File** | New, Open, Save, Save As, Page Setup, Export options, Close |
| **Edit** | Undo, Redo, Cut, Copy, Paste, Delete, Select All |
| **View** | Zoom controls |
| **Insert** | TextBox, Image, Line, Rectangle, Ellipse, Table, Chart, Barcode, Gauge, Subreport |
| **Format** | Bold, Italic, Underline, Alignment |
| **Help** | About |

### Left Panel Tabs

| Tab | Purpose |
|-----|---------|
| **Toolbox** | Draggable components to add to the report |
| **Data** | Dataset tree with fields; click **+ Dataset** to add data sources |
| **Outline** | Hierarchical view of all bands and components |

### Right Panel Tabs

| Tab | Purpose |
|-----|---------|
| **Properties** | Selected component's configurable properties |
| **Groups** | Data grouping configuration |
| **Params** | Report parameters definition |
| **Styles** | Shared style definitions for consistent formatting |

---

## 10. Adding Data to a Report

![Data Panel](report-designer/img/designer_data_panel.png)

1. Click the **Data** tab in the left panel
2. Click **+ Dataset**
3. The dataset picker dialog opens, showing all saved datasets from Settings

![Dataset Picker](report-designer/img/dataset_picker.png)

4. Click a dataset to add it to the report
    - Already-added datasets show an "Already added" badge
    - Each entry displays: Name, Description, Type, Field count, Connection name
5. The dataset appears in the Data tree with expandable fields
6. **Drag fields** from the tree onto the canvas to create bound TextBoxes
    - A header label is auto-created in the Report Header band

### Dataset Actions in Data Panel

- **Edit** (pencil icon) — Opens dataset properties
- **Remove** (X icon) — Removes the dataset from this report only (does not delete from Settings)

---

## 11. Adding Components

### From Toolbox

1. Click the **Toolbox** tab in the left panel
2. Click a component type
3. The component is inserted into the Detail band

### From Data Panel

- Drag a field from the dataset tree onto any band
- A **TextBox** bound to `=Fields.fieldname` is created automatically
- A matching header label is auto-created in the Report Header band

### Component Types

| Type | Description |
|------|-------------|
| **TextBox** | Text content or data-bound expression (e.g., `=Fields.name`) |
| **Image** | Static image, server-hosted, or URL-based image |
| **Line** | Horizontal or vertical separator line |
| **Rectangle** | Bordered rectangle shape |
| **Ellipse** | Circle or oval shape |
| **Table** | Multi-column data table with resizable columns |
| **Chart** | Chart visualization |
| **Barcode** | Barcode element for labels and tracking |
| **Gauge** | Gauge visualization |
| **Subreport** | Embedded sub-report within the main report |
| **CheckBox** | Boolean checkbox for yes/no fields |

### Selecting and Manipulating Components

- **Click** a component to select it (blue handles appear)
- **Ctrl+Click** for multi-select
- **Drag** to move components between bands
- **Drag handles** to resize
- **Delete key** to remove selected components

---

## 12. Saving a Report

![Save Modal](report-designer/img/save_modal.png)

Click **Save** (toolbar button or **Ctrl+S**) to open the save modal.

**Field Guide:**

| # | Field | Required | Description |
|---|-------|----------|-------------|
| 1 | **Report Name** | Yes | Must be unique; real-time validation checks availability |
| 2 | **Description** | No | Optional description of the report's purpose |
| 3 | **Category** | No | Optional category for filtering in Manage Reports |
| 4 | **Status** | Yes | Draft or Published |
| 5 | **Save/Update** | — | Click to save (new) or update (existing) |

### Auto-Save

- Reports auto-save to **localStorage** for crash recovery
- If the browser closes unexpectedly, reopening "New Report" will offer to restore the previous work

### File > Close

- Returns to the Manage Reports page
- Warns about unsaved changes if any exist

---

## 13. Previewing a Report

### From the Designer

- Click the **Preview** tab at the bottom of the canvas
- Or press **F5**
- The report renders with live data from the connected database

### From Manage Reports

- Click the **Preview** (eye) icon on a report row
- Opens the standalone viewer page

![Preview with Data](report-designer/img/preview_with_data.png)

**Screen Elements:**

| # | Element | Description |
|---|---------|-------------|
| 1 | **Report Title** | Name of the previewed report |
| 2 | **Back to List** | Return to Manage Reports |
| 3 | **Refresh** | Reload report with latest data |
| 4 | **Edit** | Open the report in the designer |
| 5 | **Print** | Open browser print dialog |
| 6 | **PDF** | Export as PDF via print dialog |
| 7 | **Excel** | Export as Excel file |
| 8 | **CSV** | Export as CSV file |
| 9 | **Word** | Export as Word document |
| 10 | **HTML** | Download as self-contained HTML file |
| 11 | **Report Content** | Rendered report pages with live data, paginated |

---

## 14. Working with Images

### Inserting an Image

1. Click **Image** in the Toolbox, or use **Insert > Image** from the menu
2. The Image Picker dialog opens with 3 tabs:

| Tab | Description |
|-----|-------------|
| **Server** | Browse previously uploaded images as thumbnails; click **Upload Image** to add new files |
| **URL** | Paste an external image URL with live preview |
| **Embed** | Drag & drop or browse for a local file (embedded as base64) |

3. Click **Select** to insert the chosen image

### Image Properties

- **Source** — Image URL or path (with Browse button to reselect)
- **Sizing** — Fit Proportional, Fit, Clip, or Stretch

### Upload Rules

- Supported formats: JPG, PNG, GIF, SVG, WebP
- Maximum file size: 5 MB
- Duplicate filenames receive automatic sequence numbers (photo.png, photo_1.png, photo_2.png)

---

## 15. Printing and Exporting

### Print

1. Click **Print** in the preview toolbar
2. A clean window opens with only the report pages
3. The browser's print dialog appears automatically
4. Choose a printer or "Save as PDF"

### Export Formats

| Format | Method |
|--------|--------|
| **PDF** | Via browser print dialog (Save as PDF) |
| **HTML** | Downloads a self-contained .html file |
| **Excel** | Exports via the exporter module |
| **CSV** | Exports via the exporter module |
| **Word** | Exports via the exporter module |

Export buttons appear in both the designer preview toolbar and the standalone viewer toolbar.

---

## 16. Deleting a Report

1. Go to **Manage Reports**
2. Click the **Delete** (trash) icon on a report row
3. Confirm the deletion dialog
4. The report is **soft-deleted** (can be recovered from the database)

---

## 17. Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| **Ctrl+N** | New Report |
| **Ctrl+O** | Open Report |
| **Ctrl+S** | Save Report |
| **Ctrl+Z** | Undo |
| **Ctrl+Y** | Redo |
| **Ctrl+C** | Copy |
| **Ctrl+V** | Paste |
| **Ctrl+X** | Cut |
| **Ctrl+A** | Select All |
| **Ctrl+B** | Bold |
| **Ctrl+I** | Italic |
| **Ctrl+U** | Underline |
| **Delete** | Delete selected component |
| **F5** | Toggle Preview |
| **Escape** | Return to Design from Preview |

!!! note "Backspace Key"
    Backspace does **not** delete components — this prevents accidental deletion while editing text fields. Use the **Delete** key instead.

---

## 18. Best Practices & Tips

- **Connections store credentials server-side** — passwords never reach the browser
- **Datasets reference connections** — change a password once, all datasets using that connection update automatically
- **Use the Data panel** to drag fields directly onto the canvas for fast layout creation
- **Preview frequently** to check your layout with real data (F5)
- **Save often** — use Ctrl+S; auto-save to localStorage provides crash recovery
- **Table components** support column resize (drag column edges) and header editing (double-click)
- **Use categories** to organize reports for easy filtering in the Manage Reports grid
- **Publish reports** only when they are finalized and ready for end users
