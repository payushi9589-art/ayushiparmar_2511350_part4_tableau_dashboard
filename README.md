### **Retail Sales \& Profitability Executive Dashboard**





##### 1\. Business Problem Summary





The retail leadership team requires an executive dashboard to monitor business performance across multiple operational areas, including sales, profitability, customer segments, product categories, shipping performance, discounts, and product returns.

The objective of this project is to transform raw transactional data into an interactive Tableau dashboard that enables executives to monitor key performance indicators (KPIs), identify business risks, uncover growth opportunities, and support data-driven decision-making.

\--------------------------------------------------





##### 2\. Dataset Description



The project uses a retail sales dataset containing order-level transaction information.

The dataset includes the following information:

##### 

##### 

##### Date Fields

* Order Date
* Ship Date





##### Geographic Fields

* Region
* State
* City



##### Customer Information

* Customer ID
* Customer Segment



##### Product Information

* Category
* Sub-Category
* Product Name



##### Sales Information

* Sales
* Profit
* Quantity
* Discount



##### Shipping Information

* Ship Mode
* Delivery Days



##### Return Information

* Return Flag

The dataset provides sufficient information to analyze business performance from sales, profitability, logistics, and customer perspectives.

\--------------------------------------------------





##### 3\. Tableau Workbook Description



The Tableau workbook contains one executive dashboard supported by multiple worksheets and calculated fields.

###### 

###### 

###### Worksheets Included



* Sales Trend
* Regional Performance
* Category Profitability
* Customer Segment
* Shipping Performance
* Discount vs Profit
* Return Analysis





###### KPI Sheets





* Total Sales
* Total Profit
* Profit Margin









###### Dashboard

Retail Sales \& Profitability Executive Dashboard

The dashboard integrates all worksheets into a single interactive executive reporting interface.

\-----------------------------------------------









##### 4\. Calculated Fields Created





The following calculated fields were created in Tableau.





|Calculated Field|Formula|Purpose|
|-|-|-|
|Profit Margin|`SUM(\[Profit]) / SUM(\[Sales])`|Measures overall profitability.|
|Cost|`SUM(\[Sales]) - SUM(\[Profit])`|Estimates operational cost.|
|Average Order Value|`SUM(\[Sales]) / COUNTD(\[Order ID])`|Measures average revenue per order.|
|Return Rate|`SUM(\[Return Flag]) / COUNTD(\[Order ID])`|Calculates percentage of returned orders.|
|Shipping Delay Bucket|`IF \[Delivery Days] <=2 THEN "Fast Delivery" ELSEIF \[Delivery Days] <=5 THEN "Standard Delivery" ELSE "Delayed Delivery" END`|Categorizes shipping performance.|

\--------------------------------------------------

# 

# 

##### 5\. Dashboard Components



The executive dashboard contains:

### 

###### KPI Cards





* Total Sales
* Total Profit
* Profit Margin



###### Visualizations





* Sales Trend Over Time
* Regional Sales and Profit
* Category Profitability
* Customer Segment Performance
* Shipping Performance
* Discount vs Profit Analysis
* Return Analysis

These visualizations provide executives with a comprehensive overview of business performance.

\--------------------------------------------------





###### 6\. Filters and Interactions Used



###### Interactive Filters



The dashboard includes the following interactive filters:

* Region
* State
* Category
* Customer Segment
* Ship Mode
* Order Date





###### Dashboard Interaction



A dashboard filter action was implemented where selecting a region automatically updates all related charts.

This enables users to perform interactive exploratory analysis without creating additional dashboards.

\--------------------------------------------------





##### 7\. Key Business Insights





The dashboard revealed several important business insights:

* Overall sales remain stable throughout the year with seasonal peaks.
* The South region generates the highest sales and profit.
* Technology is the most profitable product category.
* Copiers are the highest-profit sub-category.
* Home Office customers generate the highest sales.
* Higher discounts reduce profitability.
* Standard shipping has the longest delivery time.
* Furniture has the highest return rate.
* Improving discount strategy and reducing returns could significantly increase profitability.

\--------------------------------------------------





##### 8\. Dashboard Story Summary





The dashboard provides leadership with a connected view of overall business performance rather than isolated charts.

The analysis begins with high-level KPIs before exploring sales trends, regional performance, category profitability, customer behavior, shipping efficiency, discount impact, and return patterns.

The dashboard demonstrates that the business is financially healthy while identifying opportunities to improve profitability through optimized discount strategies, improved shipping performance, and reduced product returns.

\--------------------------------------------------

# 

# 

##### 9\. Assumptions and Limitations



###### Assumptions



* Sales and Profit are stored in the same currency.
* Order Date and Ship Date are valid date fields.
* Delivery Days correctly represents shipping duration.
* Return Flag accurately indicates returned orders.
* Geographic fields are complete and standardized.
* No duplicate Order IDs exist.

###### 

###### 

###### Limitations



* The dashboard uses historical data only.
* External market conditions are not included.
* Customer demographics are unavailable.
* Inventory information is not included.
* Marketing campaign effectiveness is not measured.
* Predictive forecasting is outside the scope of this dashboard.

\--------------------------------------------------

# 

# 

##### **Conclusion**



The Retail Sales \& Profitability Executive Dashboard successfully transforms transactional retail data into an executive decision-support tool. By combining KPIs, interactive filters, calculated fields, and business-focused visualizations, the dashboard enables leadership to monitor performance, identify operational risks, evaluate profitability, and uncover opportunities for business growth.

