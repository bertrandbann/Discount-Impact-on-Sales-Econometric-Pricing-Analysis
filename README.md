# Discount-Impact-on-Sales-Econometric-Pricing-Analysis# Discount Impact on Sales – Econometric Pricing Analysis

## Project Overview

This project investigates how discounts influence sales performance using a large-scale beverage retail transaction dataset containing approximately **9 million observations**.

Using econometric modelling techniques and Python, the analysis evaluates the relationship between:

- Discounts
- Customer type
- Product categories
- Purchase quantity
- Sales revenue

The project applies an **Ordinary Least Squares (OLS)** regression model to quantify the impact of pricing and customer behaviour on transaction performance while also simulating different discount strategies to assess potential revenue outcomes.

---

# Business Problem

Retail businesses frequently use discounts to stimulate demand, increase customer acquisition, and improve inventory turnover. However, excessive discounting can reduce transaction value and negatively impact profitability.

The objective of this project was to answer the following business questions:

- Do discounts increase or reduce sales revenue?
- Which products contribute the most to transaction value?
- How do B2B and B2C customers differ in purchasing behaviour?
- Which product categories generate stronger commercial performance?
- How could pricing simulations support revenue optimization?

---

# Dataset Information

The dataset contains approximately **8.99 million beverage sales transactions**.

## Main Variables

| Variable | Description |
|---|---|
| Order_ID | Unique order identifier |
| Customer_ID | Unique customer identifier |
| Customer_Type | B2B or B2C customer segment |
| Product | Beverage product sold |
| Category | Beverage category |
| Quantity | Quantity purchased |
| Discount | Discount applied to the order |
| Unit_Price | Product unit price |
| Total_Price | Total transaction value |
| Region | Sales region |
| Order_Date | Transaction date |

---

# Tools & Technologies

- Python
- Pandas
- NumPy
- Statsmodels
- Matplotlib
- Seaborn
- Econometrics / OLS Regression

---

# Data Preparation

Several preprocessing and feature engineering steps were performed before modelling.

## Data Cleaning

- Converted date columns into datetime format
- Removed unnecessary identifiers
- Checked missing values and data consistency
- Encoded categorical variables using dummy variables

## Feature Engineering

The target variable was transformed using a logarithmic function:

```python
df["Log_sales"] = np.log(df["Total_Price"])
```

The logarithmic transformation was applied to:
- stabilize variance
- reduce skewness
- improve regression interpretability

---

# Econometric Model

An **Ordinary Least Squares (OLS)** regression model was developed to estimate the relationship between sales revenue and pricing-related variables.

## Model Equation

\[
Log(Sales) = \beta_0 + \beta_1(Discount) + \beta_2(Quantity) + \beta_3(Customer\ Type) + \beta_n(Product\ Dummies) + \epsilon
\]

---

# Model Performance

| Metric | Value |
|---|---|
| Observations | 8,999,910 |
| R-squared | 0.848 |
| Adjusted R-squared | 0.848 |
| F-statistic | 1.169e+06 |

The model explains approximately **84.8% of the variation in sales revenue**, demonstrating strong explanatory performance.

---

# Key Insights

## Discounts Significantly Impact Sales Revenue

The regression analysis shows that larger discounts are associated with substantially lower transaction revenue after controlling for quantity purchased, customer type, and product mix.

This suggests that aggressive discounting strategies may negatively impact revenue performance and profitability.

---

## Quantity Purchased Positively Drives Revenue

The model estimates that each additional unit purchased is associated with approximately **4.15% higher sales revenue**.

This confirms the importance of purchase volume in revenue generation.

---

## B2B Customers Generate Higher Transaction Value

B2C customers were associated with approximately **26.7% lower sales revenue** compared to B2B customers.

This suggests that commercial customers contribute more significantly to revenue performance due to larger order sizes and repeat purchasing behaviour.

---

## Premium Alcohol Products Generate Strong Revenue Contribution

Premium products such as:

- Veuve Clicquot
- Moët & Chandon
- Johnnie Walker
- Jack Daniels
- Tanqueray

were associated with substantially higher transaction values relative to lower-priced beverage categories.

This highlights the strong commercial value of premium beverage segments.

---

## Soft Drinks and Bottled Water Products Generate Lower Revenue Contribution

Products such as:

- Coca-Cola
- Sprite
- Mountain Dew
- Volvic
- Vittel

displayed significantly lower transaction value relative to premium beverage products.

This reflects the lower unit pricing of standard soft drink and bottled water categories.

---

# Discount Simulation Analysis

To extend the commercial application of the project, a pricing simulation framework was developed.

The simulation evaluated how predicted revenue changes under different discount scenarios:

| Scenario |
|---|
| Current Discount |
| Discount +5% |
| Discount +10% |
| Discount -5% |
| Discount -10% |

The objective was to assess whether discount increases improve revenue performance or whether reducing discounts could better preserve transaction value.

This transforms the project from descriptive analytics into a commercial decision-support framework.

---

# Business Implications

## Pricing Strategy Optimization

The analysis demonstrates how businesses can use econometric modelling to optimize discount strategies and improve pricing decisions.

Potential applications include:

- Revenue optimization
- Promotion effectiveness analysis
- Product pricing strategy
- Discount policy evaluation

---

## Customer Segmentation

The project highlights important differences between B2B and B2C purchasing behaviour, enabling businesses to:

- target high-value customers
- personalize promotions
- improve customer retention strategies

---

## Product Portfolio Management

The model identifies which products contribute most significantly to transaction value.

This can support:

- inventory prioritization
- premium product positioning
- commercial planning
- category management

---

# Limitations

While the model demonstrates strong explanatory performance, several limitations should be acknowledged:

- The relationship between discounts and revenue may also reflect product mix effects
- Some multicollinearity may exist due to the large number of product dummy variables
- The model is primarily explanatory rather than predictive
- External variables such as seasonality, competition, or macroeconomic factors were not included

---

# Future Improvements

Potential future enhancements include:

- Price elasticity modelling
- Time-series forecasting
- Revenue optimization simulations
- Customer lifetime value analysis
- Power BI dashboard development
- Machine learning forecasting models

---

# Skills Demonstrated

- Econometric Modelling
- OLS Regression
- Pricing Analytics
- Revenue Analysis
- Customer Segmentation
- Statistical Interpretation
- Business Insight Generation
- Feature Engineering
- Data Cleaning & Preprocessing
- Python for Data Analytics

---

# Project Outcome

This project demonstrates how large-scale transactional data combined with econometric modelling can support pricing strategy evaluation, customer segmentation, and commercial decision-making.

The analysis provides a strong example of applying quantitative methods to solve real-world business and revenue optimization problems.
