# 🏪 Adventure Works Data Mart Project

## 📊 Overview
This project implements a star schema data mart based on the Adventure Works dataset using SQL Server Integration Services (SSIS). The data mart focuses on inventory management and product categorization, providing a streamlined view for analyzing product inventory levels across different categories.

## ⭐ Features
- **Star Schema Design**: Optimized dimensional modeling for efficient querying
- **SSIS Implementation**: ETL processes built using SQL Server Integration Services
- **Adventure Works Integration**: Transforms source OLTP data into a structured data mart
- **Inventory Analysis**: Focused on product inventory tracking and categorization
- **Power BI Integration**: Custom dashboards for visual analytics

## 🏗️ Architecture
The data mart follows a star schema design with:
- Central Inventory_Fact table for tracking product quantities
- Three dimension tables: Product, Category, and Inventory
- Optimized for inventory analysis and product categorization queries
- Built using Visual Studio 2022 Integration Services

## 📊 Data Model Details

### Fact Table
**Inventory_Fact**
- product_SRKey (FK)
- dim_category_SRKey (FK)
- Inventory_SRKey (FK)
- Shelf
- Bin
- Quantity

### Dimension Tables

**Dim_Product_DWH**
- product_SRKey (PK)
- ProductID
- Name
- ProductNumber
- Color
- ProductLine
- Class
- Style
- ProductSubcategoryID

**Dim_Category_DWH**
- dim_category_SRKey (PK)
- ProductSubcategoryID
- ProductCategoryID
- Subcategory_Name
- rowguid
- ModifiedDate
- Category_Name

**Dim_Inventory_DWH**
- Inventory_SRKey (PK)
- ProductID
- Shelf
- Bin
- Quantity

## 🔧 Technical Stack
- **Microsoft Visual Studio 2022**
- **SQL Server Integration Services (SSIS)**
- **SQL Server Database Engine**
- **Adventure Works Database** (source)
- **Power BI Desktop** (for visualization)

## 📦 Project Structure
```
DataMart/
├── Integration Services Project1/
│   └── DataMart.dtproj           
├── Solution Files/
│   └── DataMart.sln              
└── PowerBI/
    └── InventoryAnalysis.pbit    
```

## 🚀 Getting Started
1. Ensure you have Visual Studio 2022 with SSIS components installed
2. Install SQL Server with Adventure Works database
3. Clone this repository
4. Open `DataMart.sln` in Visual Studio
5. Configure connection managers for your environment
6. Deploy the SSIS package to your SQL Server
7. Open Power BI template and connect to your data mart

## 💡 Prerequisites
- Visual Studio 2022
- SQL Server 2022 (or compatible version)
- SQL Server Integration Services
- Adventure Works Database
- Power BI Desktop (latest version)

## 📈 Usage
The data mart enables several key analyses:
1. Track inventory levels by product and location
2. Analyze product distribution across storage locations
3. Monitor inventory by product categories and subcategories
4. Generate reports on product classification and storage

 ## 📊 Power BI Visualizations

### Overview Dashboard
![](./PowerBI/screenshots/Screenshot%202025-01-13%20011636.png)
This dashboard provides a high-level view of:
- Total inventory by category
- Product distribution across storage locations
- Top products by quantity

### Inventory Analysis
![Inventory Analysis](./PowerBI/screenshots/Screenshot%202025-01-25%20214915.png)
Detailed inventory metrics including:
- Heat maps of storage utilization
- Bin and shelf optimization
- Stock level warnings
- Category-wise distribution

<!--### Product Categories
![Product Categories](path_to_categories_dashboard.png)
Breakdown of products by:
- Main categories
- Subcategories
- Product attributes
- Storage allocation

### Key Performance Indicators (KPIs)
![KPIs](path_to_kpi_dashboard.png)
Tracking essential metrics:
- Storage efficiency
- Category-wise inventory levels
- Stock turnover rates
- Space utilization

### How to Access Visualizations
1. Open the included Power BI template file (`InventoryAnalysis.pbit`)
2. Connect to your deployed data mart
3. Refresh the data to see current metrics
4. Use the interactive filters to analyze specific aspects

## 🔍 Key Business Questions This Data Mart Can Answer
- What is the current inventory level for each product?
- How are products distributed across different storage locations?
- Which product categories have the highest inventory levels?
- How is inventory organized across shelves and bins?
- What is the relationship between product categories and storage locations? -->

## 🔄 Refresh Schedule
- SSIS packages scheduled to run daily at midnight
- Power BI reports set to refresh every 4 hours during business hours
- Incremental loads implemented for efficient data processing

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.
