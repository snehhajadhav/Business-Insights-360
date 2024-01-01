# Business-Insights-360
## Title: Business Insights 360 Dashboard for Finance, Sales, Marketing and Supply Chain

**Project Short Info:**	

AtliQ Hardwares, a consumer electronics company, is currently undergoing rapid expansion. However, it faces challenges in competing with other companies as a significant portion of their reports still relies on Excel. My objective is to introduce an advanced analytics solution utilizing Power BI. This implementation aims to empower the company with valuable insights, facilitating more informed decision-making processes."	

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiMzZiZDNjNzQtZGI2Mi00ZjA4LTllZjgtZjA3MmM5MDc2MDYyIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Tech stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## PowerBI techniques Learnt

-	What are all the questions should be asked before staring the project
-	Creating calculated columns
-	creating measure using DAX language
-	Data modeling
-	Using Bookmarks to switch between two visuals
-	Page navigation with buttons
-	Using divide function to prevent zero division errors
-	creating date table using m language
-	Dynamic titles based on the applied filters
-	Using KPI indicators
-	Conditional formatting the values in visuals using icons or background color
-	Data validation techniques
-	PowerBi services
-	Publishing reports to PowerBi services
-	Setting up personal gateway to set up the auto refresh of data
-	PowerBi App creation
-	Collaboration, workspace, access permissions in PowerBi services



## Business related terms

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Gross Margin
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

## Company’s back ground
AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel

- Retailers
- Direct
- Distributors

AtliQ Hardwares, a consumer electronics company, is currently undergoing rapid expansion. However, it faces challenges in competing with other companies as a significant portion of their reports still relies on Excel. My objective is to introduce an advanced analytics solution utilizing Power BI. This implementation aims to empower the company with valuable insights, facilitating more informed decision-making processes."

Initiate the project with a comprehensive kickoff session. Clarify the project's purpose, objectives, and address any questions stakeholders may have about its scope and significance.

### Questions to ask before starting with dashboard

- What is the objective of building this PowerBi dashboard?
- In what terms the success of this project will be measured?
- What will be time dead-line of the project?
- do the stakeholders expecting pre-view before the actual release?
- What are all the hopes stakeholders have out of this project?
- what are all fears the stakeholder have in terms of building this dashboard?
- Who are all will be using this dashboard and for what purpose?
- what are all expectation the stakeholders have, by the completion of this project?
- What can go wrong while building this project?
- what are all the resources/ data needed to build this dashboard?
- is there any inputs from stakeholders in terms of design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

### Dataset **Understanding.**

Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

Dimension table : It will have the static data like details of customer and products

Fact table : It will have the data about the transactions

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
                - Networking
                - Storage
                  
 - There are 14 different categories, Like Internal HDD, keyboard
        - There are different variants available for the same product
    - fact_forecast_monthly
        - This table is used to forecast the customer’s need in advance, which can help in
            - Higher customer satisfaction
            - Reduced cost in warehouses for storage purpose
        - The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
        - All the date of the month will be replaced by the start date of the month
        - It will have all the column names and in the end it will have the forecast quantity need of the customer
    - fact_sales_monthly
        - This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
- gdb056
    - freight_cost
        - This table has details of travel cost and other cost for each market with fiscal year
    - gross_price
        - Has the details of gross prices with product code
    - manufacturing_cost
        - Has the details of manufacturing cost with product code with year
    - Pre_invoice_dedutions
        - Has the details of pre invoice deductions percentage for each cutomer with year
    - Post_invoice_deductions
        - Post invoice deductions and other deductions details

## Importing data into PowerBi

- As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential

## Data Model

- Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.
- Poor data modeling affects the over all performance of the report.
- Following Good practices of data modeling is must. Refer this page to get to know the good practices [Blog](https://addendanalytics.com/blog/data-modelling-best-practices/)
- In this project, we have followed Snowfall data modeling method.

<img src="https://github.com/Naveen-S6/Business_Insights_360/blob/main/Resources/Data_model.png" class="center">

### Dashboard designing

Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required



