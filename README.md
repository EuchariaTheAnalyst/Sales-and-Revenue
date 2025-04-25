
# Table Of Content
1.[Project Overview](Project-Overview)
2.[Dataset Summary](Dataset-Summary)
3.[Project Steps](Project-Steps)
4.[Dashboard](Dashboard)
5.[Excel Features Utilized](Excel-Features-Utilized)
6.[Insights & Observations](Insights-&-Observations)
7.[Recommendations](Recommendations)
8.[Conclusion](Conclusion)


# Sales and Revenue Analysis (Excel Dashboard)

## Project Overview

This project presents a comprehensive analysis of customer shopping behavior using Microsoft Excel. The goal was to clean, organize, and visualize transaction data in order to extract insights, monitor key performance indicators (KPIs), and support strategic decision-making through an interactive dashboard.

---

## Dataset Summary

- **File Name:** `CSD.csv`  
- **Total Records:** 99,457  
- **Columns:** 10  

### Column Descriptions:

| Column Name     | Description                                               |
|------------------|-----------------------------------------------------------|
| `invoice_no`     | Unique identifier for each transaction                   |
| `customer_id`    | Unique customer ID                                       |
| `gender`         | Customer gender (Male/Female)                            |
| `age`            | Age of the customer                                      |
| `category`       | Product category purchased                               |
| `quantity`       | Number of items bought                                   |
| `price`          | Price per unit                                           |
| `payment_method` | Mode of payment (Cash, Credit Card, etc.)               |
| `invoice_date`   | Date of the transaction                                  |
| `shopping_mall`  | Mall where purchase was made                             |

---

## Project Steps

### 1. Data Cleaning

- Removed duplicate and empty rows.
- Standardized inconsistent text entries (e.g., capitalization in `category`, `payment_method`).
- Converted `invoice_date` to proper Excel date format.
- Extracted **Month**, **Day** and **Year** using Excel formulas:
  ```excel
  =TEXT(invoice_date, "mmm")   → Month
  =TEXT(invoice_date, "yyyy")  → Year
  =TEXT(invoice_date, "ddd")   → Day
  ```

### 2. Data Transformation

- Added a new calculated column `REVENUE`:
  ```excel
  =quantity * price
  ```
  This column was the basis for revenue-related analysis.

- Added a new column `Age_group`:
```excel
  =IF(D2<=25,"18-25",IF(D2<=35,"26-35",IF(D2<=45,"36-45",IF(D2<=55,"46-55", "56+"))))
  ```
  This column grouped age into different groups.

### 3. Pivot Table Summaries

Generated several pivot tables to analyze and summarize key metrics:

- **Total Revenue by Shopping Mall**
- **Quantity Sold by Product Category**
- **Transactions by Gender**
- **Payment Method Preferences**
- **Monthly Sales Trends**
- **Customer Segmentation by Age Groups**

### 4. Dashboard Design

Created a **dynamic and interactive Excel Dashboard** with:

#### KPI Cards
- **Total Revenue**  
- **Total Quantity Sold**  
- **Total Number of Transactions**

#### Charts and Visualizations
- **Bar Chart:** Revenue by Shopping Mall  
- **Column Chart:** Quantity by Product Category  
- **Line Chart:** Sales Trend Over Time  
- **Doughnut Chart:** Payment Method Distribution  
- **Pie Chart:** Gender Distribution  

#### Filters (Slicers)
- Gender   
- Day of the Week  
- Month  
- Year  
- Age Groups

---

## Dashboard
<img width="922" alt="Image" src="https://github.com/user-attachments/assets/e5814cbe-7afc-4cce-afe2-576eb77c7792" />

---

## Excel Features Utilized

- Pivot Tables & Pivot Charts  
- Slicers for interactive filtering  
- Named Ranges  
- Data Validation (for filtering inputs)  
- Key Excel Functions:  
  ```excel
  IF(), TEXT(), YEAR(), MONTH(), DAY()
  ```

---

## Insights & Observations

- **Revenue Concentration:** A significant portion of revenue was driven by a few malls, suggesting a strong customer base in those locations.
- **Top-Selling Categories:** Clothing and Food & Beverage emerged as the highest-selling product categories.
- **Gender Split:** Slightly more transactions were made by female customers (60%) than males (40%).
- **Age Dynamics:** Customers aged **36–45** and **56+** accounted for the largest volume of purchases.
- **Payment Behavior:** Cash remained the most common payment method, though credit and debit card usage is growing.
- **Sales Trend:** Monthly sales remained relatively stable with minor peaks, suggesting consistent consumer behavior throughout the year.

---

## Recommendations

1. **Boost Online & Card Payment Promotions**  
   Encourage more use of digital payments for faster checkout and better tracking.

2. **Focus on High-Converting Categories**  
   Prioritize marketing and inventory for top-performing categories like **Clothing**.

3. **Age-Specific Campaigns**  
   Launch personalized promotions for the dominant 26–45 age group.

4. **Enhance Customer Retention**  
   Leverage customer ID data to build loyalty programs for repeat buyers.

5. **Invest in Top-Performing Malls**  
   Concentrate product variety and promotional efforts on malls generating the highest revenues.

---

## Conclusion

This Excel-based sales dashboard empowers the business to explore customer behavior, monitor sales KPIs, and make informed decisions. With over **99,000** transactions analyzed, this tool provides valuable visibility into category performance, customer segments, and payment trends — all of which can help drive smarter marketing, sales, and operational strategies.# Sales-and-Revenue
