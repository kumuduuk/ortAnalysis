# Online Retail Transation Analysis Project 

This project focuses on data exploration, cleaning, analysis, and visualisation. It analyses online retail transaction data to understand customer behaviour, identify popular products, and provide insights that help optimise pricing and marketing strategies.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* The "Online Retail Transaction" dataset contains information on transactions made by customers through an online retail platform. The dataset includes data on the products that were purchased, the quantity of each product, the date and time of each transaction, the price of each product, the unique identifier for each customer who made a purchase, and the country where each customer is located. This dataset can be used to analyze customer behavior and preferences, identify popular products, and optimize pricing and marketing strategies. The dataset is well-suited for data analysis and machine learning applications, as it contains a large volume of transactional data that can be used to train predictive models and make data-driven decisions.

    #### Column Descriptors
        - StockCode: A code used to identify the product that was purchased
        - Description: A brief description of the product that was purchased
        - Quantity: The quantity of the product that was purchased
        - InvoiceDate: The date and time that the purchase was made
        - UnitPrice: The price of one unit of the product that was purchased
        - CustomerID: The unique identifier for the customer who made the purchase
        - Country: The country where the customer who made the purchase is located
## Business Requirements
* Analyse online retail transaction data to understand customer behaviour, identify popular products, and optimise pricing and marketing strategies. Provide insights into customer behaviour, popular products, and pricing strategies to improve sales and marketing efforts.



## Hypothesis and how to validate?
1. High-spending customers drive the majority of total sales.

        Validation:
        - Segment customers based on total spending (e.g., Low, Medium, High).
        - Calculate the total sales contribution of each segment.


2. Sales follow clear seasonal or monthly patterns.

        Validation:
        - Group transactions by month and plot total sales over time.
        - Identify peaks and dips in the trend line.


3. A few products generate a large share of revenue.

        Validation:
        - Rank products by total sales.
        - Visualize the top 10 products.


4. Frequent customers tend to have higher total spending.

        Validation:
        - Group by customer and calculate purchase frequency and total spent.
        - Plot frequency vs. total sales.

## Project Plan
### High-Level Steps for the Analysis

#### 1. Data Collection:

    1. Used the Online Retail dataset (one year of transaction records) as the source.
    2. Imported the data into a Jupyter Notebook environment using pandas.

#### 2. Data Cleaning & Preparation:

    1. Removed duplicates and irrelevant records (e.g., adjustments and invalid credit notes).
    2. Handled missing values in key fields such as Description and CustomerID.
    3. Standardised data types for performance and consistency.
    4. Filtered and aligned credit and sales transactions to ensure data accuracy.

#### 3. Feature Engineering:

    1. Extracted time-based features such as year, month, day, and weekday.
    2. Calculated TotalSales as Quantity × UnitPrice.

#### 4. Exploratory Data Analysis & Visualisation:

    1. Descriptive statistics to understand overall sales performance.
    2. Trend analysis over time (daily and monthly).
    3. Customer segmentation based on spending and frequency.
    4. Product performance analysis to identify top sellers.

#### 5. Insights & Interpretation:

    1. Identified customer behaviour patterns.
    2. Highlighted key products contributing to revenue.
    3. Provided actionable insights for pricing and marketing strategies.

### Rationale for Methodologies

- Pandas and NumPy were used for their flexibility and efficiency in handling large transactional datasets.
- Descriptive statistics provided a solid foundation for understanding data distribution and overall trends.
- Trend analysis and segmentation were selected to uncover customer behaviour patterns and sales cycles, which are directly useful for marketing and pricing strategies.
- Data visualisation (Matplotlib and Seaborn) made insights more interpretable and business-friendly.
- This approach balances analytical rigour with business relevance, ensuring results can support decision-making.


## Ethical considerations
* The dataset is used for this analysis does not cointain any private or sensitive information.

## Development Roadmap

### Challenges and strategies

1. While cleaning the data, I removed duplicate rows, which caused the index to become non-linear. I hadn’t realized earlier that this could lead to confusion during join or merge operations. To avoid such issues, it’s good practice to use reset_index(drop=True) after removing rows (e.g., dropping duplicates, NA values, or applying filters) unless the original index needs to be preserved.

2. I initially converted the CustomerID column to a category datatype, but this caused errors during the groupby operation. To resolve the issue, I converted CustomerID (and StockCode) to string before performing the grouping.

3. I found there were 3 records with 'adjust bad debt' description. 
   - These are accounting adjustments, not actual sales.
   - Keeping them would distort total sales and product/customer analysis.
   - Removing them ensures clean, analysis-ready transaction data.

* What new skills or tools do you plan to learn next based on your project experience? 


## Main Data Analysis Libraries
- Pandas is used for data exploration and cleaning.
- Matplotlib is used for visualisation.
- Seaborn is used for visualisation.
- Plotly is used for interactive visualisation.


## Credits 

- The dataset was downloaded from [Kaggle](https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset).
- For this project I have used the [Code Institute Project Template](https://github.com/Code-Institute-Org/data-analytics-template/tree/main).
- I used Code Institute learning materials to review visualisation techniques.


## Acknowledgements
* Special Thanks for Code institute team and my group members.