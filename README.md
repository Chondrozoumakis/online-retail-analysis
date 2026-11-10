# Online Retail Case Study: Sales Analysis and A/B Test Proposal

Analysis of one year of transactions from a UK-based online gift retailer. I clean the raw data, explore where and when revenue is generated, and design an A/B test to increase revenue.

**Notebook:** [`online_retail_analysis.ipynb`](online_retail_analysis.ipynb)

## Business question
When, where and through which products does the store generate its revenue, and which A/B test could increase it?

## Data
- Source: [UCI Machine Learning Repository, Online Retail data set](https://archive.ics.uci.edu/dataset/352/online+retail)
- Period: 1 December 2010 to 9 December 2011
- 541,909 transaction lines, 8 columns
- The data has no cost information, so the analysis is about revenue, not profit.

## What I did
1. **Cleaned the data** and documented every step: removed duplicates, set cancellations aside, removed zero and negative values and non-product codes (postage, fees, vouchers), and removed two huge orders that were cancelled right after being placed. The notebook contains a table with the rows removed at each step.
2. **Explored the sales** by month, hour and weekday, country, product and customer, and looked at cancellations.
3. **Designed an A/B test** (free-delivery threshold to raise average order value) with hypothesis, metrics, guardrails, sample size and duration calculated from the data.

## Main findings
- Revenue is strongly seasonal and peaks in November.
- Sales happen on weekdays during office hours, concentrated around midday, and there are no Saturday transactions.
- The United Kingdom generates the large majority of revenue.
- Revenue is spread over a long tail of products; no single product dominates.
- A minority of customers brings in a large share of revenue, and most customers order more than once.
- A few very large baskets pull the average order value well above the median, which led to the A/B test proposal.

The exact figures are printed in the "Conclusions" section of the notebook.

## How to run it
1. Download `Online Retail.xlsx` from the UCI link above and place it in the same folder as the notebook.
2. Install the requirements: `pip install -r requirements.txt`
3. Open `online_retail_analysis.ipynb` in Jupyter or Google Colab and run all cells.

## Tools
Python, pandas, NumPy, Matplotlib

## Limitations
One year of data only, no cost data, about 25% of rows without a customer ID, and the A/B test is a design on paper that has not been run.
