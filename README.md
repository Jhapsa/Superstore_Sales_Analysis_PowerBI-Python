
# 📊 Superstore Sales Dashboard – Power BI + Python Integration

## 👤 Author
**Biswarup Das**

## 📌 Project Overview

This project presents an **interactive sales dashboard** built using **Power BI**, with **Python** integration for data preprocessing and advanced visuals.

The dashboard analyzes sales data from a fictional Superstore to extract business insights such as:
- Sales trends across months
- Regional sales distribution
- Category-wise performance

---

## 🛠 Tools Used

- 📘 **Power BI Desktop**
- 🐍 **Python (Pandas, Matplotlib)** *(used inside Power BI)*
- 📁 Dataset: `Sample - Superstore.csv`
- 💡 Data Source: [Kaggle – Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

---

## 🔄 Data Cleaning (via Python Script)

Used **Python script inside Power BI** to clean the dataset and create a new `MonthYear` column for time-series analysis.

```python
import pandas as pd

df = pd.read_csv("C:/Users/ASUS/Downloads/Sample_Superstore.csv", encoding='latin1')
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['MonthYear'] = df['Order Date'].dt.strftime('%b-%Y')
```

🔹 Implemented via:
> **Home → Get Data → Python script**

---

## 📈 Visualizations in Power BI

| Visualization | Purpose |
|---------------|---------|
| 📉 Line Chart | Show **monthly sales trend** using `MonthYear` |
| 📊 Bar Chart | Compare **sales by Region** |
| 🍩 Donut Chart | Breakdown of **sales by Category** |
| 📦 Card Visuals | Show total sales in selected filters |
| 🧮 Python Visual | Custom bar chart created using Matplotlib |
| 🎛 Slicers | Filters by Region & Category |

---

## 📊 Key Insights

- 🔝 **Technology** category generated the highest sales (~36% of total).
- 🌍 **West** region led in total revenue (~$730K).
- 📆 **December** was the strongest sales month.
- 🔻 **February** saw the lowest sales (~$60K), suggesting seasonal dips.

---

## 📦 Deliverables

- `Superstore_Dashboard.pbix` – Power BI file with all visuals
- `dashboard_screenshot.png` – Visual export of dashboard
- `Insights.txt` – Business observations based on the dashboard
- `README.md` – Project documentation (this file)
- `LICENSE` – MIT License

---

## 📄 License

This project is open source under the **MIT License**.  
See the [LICENSE](./LICENSE) file for more details.

---

## 📬 Contact

Have suggestions, feedback, or want to collaborate?  
Reach out to **Biswarup Das** via GitHub or LinkedIn.

---
