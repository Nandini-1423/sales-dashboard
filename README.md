# sales-dashboard

### Dashboard Link : https://github.com/Nandini-1423/sales-dashboard/blob/main/SALES%20DASHBOARD.pbix

## Problem Statement

To create a comprehensive sales dashboard using Power BI that provides actionable insights into the sales performance of a tech company. The dashboard should help stakeholders understand sales trends, identify top-performing products and regions, monitor the performance of sales supervisors, and track key sales metrics.

### Steps Followed for Creating the Sales Dashboard in Power BI

1. Data Preparation and Cleaning
- Loading Data: Loaded the dataset from the provided Excel file 
   into Power BI.
- Data Cleaning:
  - Removed duplicates to ensure data integrity.
  - Handled missing values by filling or removing them as 
     necessary.
  - Standardized date formats for consistency.
  - Ensured numeric fields were correctly formatted (e.g., sales, 
    cost, quantity).
  - Verified that state codes and names were correctly mapped.
  - Ensured all necessary relationships between tables 
       (Sales_Data, State_list, Supervisor) were correctly 
     established.
    
2. Data Transformation
- Calculated Columns and Measures:
  - Created calculated columns and measures using DAX for key metrics:
   - Total Sales: SUM(Sales_Data[Total_Sales])
   - Total Cost: SUM(Sales_Data[Total_Cost])
   - Total Quantity: SUM(Sales_Data[Quantity])
   - Total Count: COUNT(Sales_Data[Order_Number])
   - Total Profit: SUM(Sales_Data[Total_Sales]) - 
       SUM(Sales_Data[Total_Cost]
    
 Data Modeling:
 - Defined relationships between the tables:
   - Sales_Data[State_Code] and State_list[State_Code]
   - Sales_Data[Assigned Supervisor] and Supervisor[Supervisor]
  

3. Dashboard Creation
  - Cards for Key Metrics:
    - Created card visuals for displaying Total Sales, Total Cost, Total Quantity, Total Count, and Total Profit.
  - Column Chart:
    - Created a column chart to show category-wise quantity sold.
    - Set the x-axis to Sales_Data[Category] and y-axis to SUM(Sales_Data[Quantity]).
  - Map Chart:
    - Created a map chart to display state-wise profit.
    - Used State_list[State] for location and SUM(Sales_Data[Total Profit]) for values.
  - Pie Chart:
    - Created a pie chart to show total sales by brand.
    - Used Sales_Data[Brand] for the legend and SUM(Sales_Data[Total_Sales]) for values.
  - Slicer for Supervisor Image:
    - Added a slicer visual to filter data based on supervisor.
    - Used Supervisor[Supervisor] and included images from Supervisor[Image_URL].
     
4. for creating new column following DAX expression was written
   - On the right side ,data column -click on right side of sales data and select New Measure and type:
     - Total Profit Calculation:
     -  Defined a DAX measure for total profit:
        - Total Profit = SUM(Sales_Data[Total_Sales]) - SUM(Sales_Data[Total_Cost])

5. Interactivity and Filters
- Interactive Filters:
  - Added filters for date range, product category, brand, and state.
- Drill-Down Capabilities:
  - Enabled drill-down functionality on the column chart to explore data by month or region.
- Detailed Transaction View:
  - Provided a table visual to display detailed sales transactions with options for drill-through.
    
6. Testing and Validation
  - Tested all visuals to ensure they displayed correct and expected values.
  - Validated DAX measures and calculated columns for accuracy.
  - Ensured all interactive filters worked seamlessly across visuals.

# Snapshot of Dashboard (Power BI Services)
 
![dashboard image](https://github.com/user-attachments/assets/9e8c6b22-caf7-474b-ab4d-07953fe15528)

# Report Snapshot (Power BI Desktop)

