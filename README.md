# Org Chart - Power BI Visual

[![Version](https://img.shields.io/badge/version-2.0.0.0-blue.svg)](https://github.com/pbimap/orgchart)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Power BI](https://img.shields.io/badge/Power%20BI-Compatible-orange.svg)](https://powerbi.microsoft.com/)

A custom Power BI visual for rendering interactive organization charts. Built with D3.js, it supports hierarchical data visualization with employee/manager relationships, rich cards, zoom/pan controls, and full formatting integration.
<img width="1405" height="614" alt="image" src="https://github.com/user-attachments/assets/4a86466b-03cb-49c1-aec5-9bda8d8ef82f" />

## Features

- **Hierarchical Layouts**: Vertical (top-down) or horizontal orientations with automatic spacing and expand/collapse for levels (up to 6).
- **Rich Cards**: Display names, titles, departments, avatars (from URLs), details, and metrics (up to 6 badges). Customizable alignment, shadows, borders, and colors.
- **Interactivity**: Zoom & pan (scale 0.01–100), node selection with path highlighting, tooltips (up to 20 fields), and Power BI cross-filtering.
- **Toolbar**: Compact rail with toggle for layout switch, expand/collapse all, and fit-to-view.
- **Data Support**: Bind Employee ID (grouping), Manager ID (grouping for parent links), Display Name, Title, Division, Image URL, Details (up to 5), Metrics (measure, up to 6), and Tooltips (grouping, up to 20).
- **Performance**: Handles large datasets with pruning for collapsed nodes and cycle detection in hierarchies.

- Test in Power BI Desktop by importing the `.pbiviz`.

Compatible with Power BI Desktop (API 5.3.0+) and Power BI Service.

## Usage

### Data Binding
- **Required**: Employee ID (unique grouping), Manager ID (grouping for parent links).
- **Recommended**: Display Name (grouping), Title (grouping), Division (grouping), Image URL (grouping for avatars).
- **Optional**: Details (grouping, up to 5 for card text), Metrics (measure, up to 6 for badges), Tooltips (grouping, up to 20).

Example dataset structure:
| Employee ID | Manager ID | Display Name | Title | Division | Image URL | Metric 1 |
|-------------|------------|--------------|-------|----------|-----------|----------|
| 1          | null      | CEO Name    | CEO  | Exec    | https://... | 100     |
| 2          | 1         | VP Name     | VP   | Sales   | https://... | 50      |

### Basic Setup
1. Add the visual to your report.
2. Drag fields to the visual's buckets (e.g., Employee ID to "Employee Id", Manager ID to "Manager Id").
3. The chart renders automatically—root nodes have no manager.
4. Use toolbar for layout/zoom; format pane for styles.

### Test Data  
https://github.com/pbimap/orgchart/blob/main/data/Test_data.csv
<img width="1460" height="601" alt="image" src="https://github.com/user-attachments/assets/67d10414-dbad-4bec-a734-30dd74a35bcd" />  

#### Sample Data format:
<img width="1062" height="526" alt="image" src="https://github.com/user-attachments/assets/9efca58e-f824-4971-a335-06f0a60ec706" />

<img width="1366" height="768" alt="search_with_auto_Suggestion_highlight_zoom" src="https://github.com/user-attachments/assets/d3537e63-3c82-4a7b-bac1-defada27f43d" />  
<img width="1366" height="768" alt="screenshot3_select_highlight_to_root" src="https://github.com/user-attachments/assets/d8d31aaf-1e3f-4120-b33a-1708abb388af" />  
<img width="1366" height="768" alt="screenshot1" src="https://github.com/user-attachments/assets/335ccf48-d48d-4ba8-8226-18a4c9cf7d9d" />  
<img width="1366" height="768" alt="screensho2_tooltip" src="https://github.com/user-attachments/assets/3d85fd72-cd50-4f51-a3f1-f11556c522be" />  
<img width="1366" height="768" alt="configurable" src="https://github.com/user-attachments/assets/4d70151a-6dec-4423-800d-8bfcc9798eed" />  


## License

MIT License. See [LICENSE](LICENSE) for details.

## Support

- [GitHub Issues](https://github.com/pbimap/orgchart/issues)
- Email: pbimap@outlook.com
