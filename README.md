# Tableau Sales Dashboard Project

## Project Overview
This project demonstrates the creation of an interactive Tableau dashboard using the **Sample Superstore Sales dataset**. The dashboard visualizes sales, profit, order quantity, and customer data across different regions, product categories, and segments. It also showcases the use of calculated fields, filters, and interactivity among multiple visuals.

The project is designed to provide insights into sales performance and customer behavior, making it suitable for business analysis and decision-making.

---

## Table of Contents
1. [Dataset](#dataset)  
2. [Project Structure](#project-structure)  
3. [Key Steps and Procedures](#key-steps-and-procedures)  
   - [Importing Data](#importing-data)  
   - [Creating & Formatting Visuals](#creating--formatting-visuals)  
     - [Bar Chart](#bar-chart)  
     - [Pie Chart](#pie-chart)  
     - [Scatter Plot](#scatter-plot)  
     - [Line Chart](#line-chart)  
   - [Creating the Dashboard](#creating-the-dashboard)  
4. [Key Features](#key-features)  
5. [Usage](#usage)  
6. [License](#license)  

---

## Dataset
- **Source:** Sample Superstore dataset (Excel file)  
- **Tables Used:** `Orders`  
- **Columns:**  
  - Row ID, Order ID, Order Date, Order Priority  
  - Order Quantity, Sales, Discount, Shipping Mode  
  - Profit, Unit Price, Shipping Cost  
  - Customer Name, City, Zip Code, Customer Segment  
  - Product Category, Product Sub-Category, Product Name  

---

## Project Structure

```text
Tableau-Sales-Dashboard/
├── data/
│   └── Sales_Profit.xlsx        # Dataset
├── dashboard/
│   └── Sales_Profit.twbx        # Tableau workbook
├── visuals/
│   ├── Bar_Chart.png                 # Screenshot of Bar Chart
│   ├── Pie_Chart.png                 # Screenshot of Pie Chart
│   ├── Scatter_Plot.png              # Screenshot of Scatter Plot
│   └── Line_Chart.png                # Screenshot of Line Chart
├── README.md                         # Project documentation
└── LICENSE.md                        # MIT License
'''
---

## Key Steps and Procedures

### Importing Data
1. Open **Tableau Desktop Public Edition**.  
2. Connect to **Microsoft Excel** and select `Sample Superstore.xlsx`.  
3. Load the **Orders** table into Tableau.  
4. Explore columns such as Sales, Profit, Customer Segment, Product Category, and Order Date.  

---

### Creating & Formatting Visuals

#### Bar Chart
- Represents **Total Profit by Region** and **Customer Segment**.  
- Steps:
  1. Drag `Profit` to Rows and `Region` to Columns.  
  2. Create a **calculated field** for unit price grouping:
     ```text
     IF [Unit Price] <= 2500 THEN 'A'
     ELSEIF [Unit Price] <= 5000 THEN 'B'
     ELSE 'C'
     END
     ```
  3. Customize chart: hide headers, add borders, show data labels, format title and font.  
  4. Drag `Customer Segment` to Color and Label for better segmentation visualization.  

#### Pie Chart
- Shows **Total Sales by Region** with percentage contribution.  
- Steps:
  1. Drag `Sales` to Angle and `Region` to Color.  
  2. Add data labels: region names, sales values, and percent of total.  
  3. Customize colors, legends, and chart title.  

#### Scatter Plot
- Visualizes the **relationship between Sales and Profit** for different customers.  
- Steps:
  1. Drag `Profit` to Columns and `Sales` to Rows.  
  2. Add `Customer Name` to Detail in Marks shelf.  
  3. Format chart: axis font size, color, bold/italic styles, chart title formatting.  

#### Line Chart
- Represents **Total Order Quantity by Month**.  
- Steps:
  1. Drag `Order Date` to Columns and `Order Quantity` to Rows.  
  2. Adjust granularity to Month.  
  3. Format chart: remove gridlines, hide headers, add data labels.  
  4. Apply filters across visuals using the **Unit Price Grouping** field.  

---

### Creating the Dashboard
- Steps:
  1. Create a **New Dashboard**.  
  2. Drag all charts (Line, Pie, Bar, Scatter) onto the dashboard.  
  3. Resize charts, add borders, and adjust formatting.  
  4. Apply filters for interactivity.  
  5. Enable **"Use as Filter"** for charts to interact dynamically.  
  6. Save the workbook as `Tableau Dashboard One`.  

---

## Key Features
- Interactive dashboard with multiple chart types.  
- Visualizes **profit, sales, and order quantities** by region, customer segment, and month.  
- Custom calculated fields for **unit price categorization**.  
- Clean, formatted visuals with customized titles, labels, colors, and borders.  
- Filters applied to control data across all charts.  

---

## Usage
1. Open `Tableau_Dashboard.pbix` in **Tableau Desktop Public Edition**.  
2. Interact with charts by clicking on segments or using filters.  
3. Explore insights like top-performing regions, customer segments, and monthly trends.  

---

## License
This project is licensed under the **MIT License**. See [LICENSE.md](LICENSE.md) for details.
