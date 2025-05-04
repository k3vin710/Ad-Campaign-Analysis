# Ad-Campaign-Analysis

By: Kevin Pattni

## Project Overview

This project aims to analyze and track key performance metrics for two platforms used to process orders: **Shopify** and **Checkout Champ (CoC)**. The objective is to generate various business metrics, including order count, revenue, unique customers, and more, both for each platform and combined across both platforms.

## Data Sheets

The dataset consists of the following sheets:

-   **Analysis Sheet:** Contains the metrics we aim to track.
-   **Expenses Sheet:** Contains the expenses required for the metrics calculations.
-   **GREEN Sheets:** These sheets provide customer data broken down by year and platform.

## Objective

The goal is to use the raw data provided from each platform to calculate and report the following metrics:

-   **Metrics by Platform and Year:**
    -   These metrics will be tracked for each platform (Shopify and CoC) by year.
-   **Combined Metrics by Year:**
    -   These metrics will be calculated by combining data from both platforms for each year.
-   **Overall Metrics:**
    -   These will provide a summary of all years, combining data from both platforms.

## Approach

### Assumptions

Since we received a combined budget for 2022 for Facebook and Google ads, we will use the ratio of ad spend between 2023 and 2024 to allocate the expenses between Shopify and CoC.

### Ad Spend Distribution (2022 - 2024)

| Platform               | Facebook Ads                                    | Google Ads                               |
|------------------------|-------------------------------------------------|------------------------------------------|
| 2022                   | $440,274.02 (Shopify), $101,263.05 (CoC)        | Shopify: $88,054.80, CoC: $352,219.22   |
| 2023                   | Shopify: $278,635.14, CoC: $1,362,406.20      | Shopify: $214,277.17, CoC: $62,311.53    |
| 2024 (up to 8/31/24)   | Shopify: $533,977.67, CoC: $1,835,500.61     | Shopify: $251,005.28, CoC: $25,935.00    |

### Additional Calculation Requirements

-   Use **Power Query Editor** to find unique customers.

## Key Performance Indicators (KPIs)

-   **Order Count (Shopify and CoC):**
    -   Formula: `Sum of orders processed per platform.`
    -   Purpose: Determines total sales volume on each platform.
-   **Unique Customers (Shopify and CoC):**
    -   Formula: `Count of distinct customer emails per platform.`
    -   Purpose: Measures unique customer reach on each platform.
-   **Revenue (Shopify and CoC):**
    -   Formula: `SUM(Total Sales - Refunds)` for each platform.
    -   Purpose: Tracks revenue per platform after accounting for refunds.
-   **Average Order Value (AOV):**
    -   Formula: `Revenue / Order Count` (calculated separately for Shopify and CoC).
    -   Purpose: Provides insights into average customer spending per order on each platform.
-   **Cost Per Sale (CPS):**
    -   Formula: `Total Ad Spend / Order Count` for each platform.
    -   Purpose: Assesses ad spend efficiency on each platform.
-   **Customer Cost by Year:**
    -   Formula: `Total Ad Spend / New Customers` for each platform.
    -   Purpose: Measures the cost to acquire new customers.
-   **Customer Lifetime Value (LTV) by Year Acquired:**
    -   Formula: `AOV * Avg # of Orders per Customer` (calculated for each platform and then combined if needed).
    -   Purpose: Estimates long-term revenue per customer on each platform.
-   **Return on Ad Spend (ROAS):**
    -   Formula: `Revenue / Total Ad Spend` (calculated for each platform).
    -   Purpose: Tracks revenue generated for each ad dollar spent.
-   **Weighted Average Order Value (AOV Weighted):**
    -   Formula: `(Shopify AOV * Shopify Orders + CoC AOV * CoC Orders) / (Shopify Orders + CoC Orders)`
    -   Purpose: Provides an overall AOV considering both platforms.
-   **Cost Per Acquisition (CPA):**
    -   Formula: `Total Ad Spend / Total Unique Customers` (after accounting for shared customers across Shopify and CoC).
    -   Purpose: Measures customer acquisition efficiency across both platforms.

## Setup Instructions

1.  Clone the Repository:
    ```bash
    git clone https://github.com/k3vin710/Ad-Campaign-Analysis.git
    ```
2.  Open Excel:
    Open the provided Excel file and navigate to the relevant sheets for analysis.
3.  Use Power Query Editor:
    Power Query Editor should be used to extract unique customer data for analysis.
4.  Perform Calculations:
    Follow the formulas mentioned under KPIs to calculate the metrics for both Shopify and CoC platforms.

## Conclusion

This project allows us to analyze the performance of Shopify and CoC platforms based on various business metrics. By evaluating these KPIs, we can derive insights into platform performance, customer acquisition, and ad spend efficiency.
