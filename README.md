# 🛒 RFM Customer Segmentation Analysis

This project performs an end-to-end **RFM (Recency, Frequency, Monetary)** segmentation analysis on real-world retail transaction data. It includes data cleaning, scoring, customer classification, and interactive visualizations to support marketing strategy and business decision-making.

---

## 📦 Dataset

- **Source**: [Online Retail Listing – Kaggle](https://www.kaggle.com/datasets/ilkeryildiz/online-retail-listing)
- **Description**: Historical transaction data for a UK-based online retailer between 2009–2011. Includes invoices, customer IDs, product codes, purchase dates, and pricing.

---

## 🧭 Project Steps

1. 📥 **Data Loading and Initial Parsing**  
   Load the dataset, fix encoding issues, and convert raw date and price formats into structured values.

2. 🧾 **Dataset Overview and Initial Insights**  
   Perform type inspection, null value checks, and outlier detection to understand dataset integrity.

3. 🔎 **Exploratory Data Analysis (EDA)**  
   Explore distributions of transactions, quantities, and spending behavior to form hypotheses and identify cleaning needs.

4. 🧼 **Data Cleaning for RFM Segmentation**  
   Remove rows with missing or invalid data (e.g., negative quantities, returns, bad debt). Construct a `TotalPrice` metric.

5. 📊 **RFM Metrics Calculation**  
   Group data by `Customer ID` to compute:
   - **Recency**: Days since last purchase
   - **Frequency**: Number of unique invoices
   - **Monetary**: Total amount spent

6. 🔢 **Calculate and Score RFM Metrics**  
   Assign RFM scores (1–5) using quintiles. Combine these into `RFM_Segment` codes and aggregate `RFM_Score`.

7. 🧩 **Segment Customers and Export RFM Results**  
   Label customers into business segments (e.g., *Champions*, *At Risk*, *Hibernating*) and export a CSV with all enriched features.

8. 📊 **Interactive RFM Dashboard with Plotly**  
   Visualize customer segments with dynamic bar charts, box plots, pie charts, and scatter plots for data storytelling and strategic interpretation.

---

## 🧠 Insights & Strategy

| Segment             | Behavior                                   | Suggested Action                              |
|---------------------|--------------------------------------------|------------------------------------------------|
| **Champions**        | Frequent, recent, high spenders            | Reward loyalty, early access, VIP perks       |
| **Loyal Customers**  | Frequent and fairly recent buyers          | Upsell and strengthen brand affinity          |
| **Potential Loyalists** | Recently active, low frequency          | Welcome series, nurture campaigns             |
| **New Customers**    | Very recent first-time buyers              | Onboarding journey and second-purchase offer  |
| **At Risk**          | Previously active, now silent              | Reactivation discounts, feedback collection   |
| **Hibernating**      | Low value and long inactive                | Occasional re-engagement or sunset strategy   |
| **Others**           | Undefined behavior                        | Monitor, analyze, or test with marketing pilots|

---

## 📁 Outputs

- `rfm_customer_segments.csv` – Cleaned customer table with RFM metrics, scores, segments.
- Plotly dashboard – Interactive visual analysis of customer patterns.

---

## 🛠️ Tools & Libraries

- Python (Pandas, Plotly)
- Google Colab / Jupyter Notebook
- Quantile-based binning, Lambda functions
- Exploratory Data Analysis (EDA)

---

## 📄 License & Usage

This project is open for educational and non-commercial analysis.  
All data belongs to the original author as hosted on Kaggle.

---

## 🚀 Author

Developed by [Your Name] – [GitHub Profile or LinkedIn (Optional)]  
For questions or collaboration, feel free to reach out!

