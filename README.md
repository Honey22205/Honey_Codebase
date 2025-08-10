
# Wings R Us - WWT Competition 2025

**Team Name:** Honey  
**Project Title:** Intelligent Menu Recommendation System with Humanized Touch  
**Authors:** Honey & Shreyash  

---

## Project Overview

Our solution predicts the **top 3 most relevant items** to recommend for a customer's cart, with an emphasis on **humanized, upsell-oriented suggestions**.  
We combined **data-driven ML models** with **category-aware logic** to ensure diversity in recommendations — so customers get a mix of mains, sides, and drinks instead of repetitive items.

---

## Tech Stack

<div style="background-color:#e3f2fd;padding:10px;border-radius:8px;border:1px solid #90caf9;">
<b>Languages & Environment:</b> Python 3.11, Jupyter Notebook / Google Colab
</div>

<div style="background-color:#f1f8e9;padding:10px;border-radius:8px;border:1px solid #aed581;">
<b>Data Handling:</b> pandas, numpy, openpyxl
</div>

<div style="background-color:#fff3e0;padding:10px;border-radius:8px;border:1px solid #ffb74d;">
<b>Machine Learning:</b> scikit-learn, LightFM (Collaborative Filtering), mlxtend (Association Rules)
</div>

<div style="background-color:#fce4ec;padding:10px;border-radius:8px;border:1px solid #f48fb1;">
<b>Visualization:</b> matplotlib, seaborn
</div>

---

## Repository Structure
```

honey\_Codebase/
│
├── WingsRUs\_Recommendation\_Pipeline.ipynb   # Main Jupyter Notebook (full pipeline)
├── requirements.txt                          # Python dependencies
├── README.md                                 # Project documentation
└── output/
├── honey\_WWT\_Recommendation\_Output\_Cleaned.xlsx
├── honey\_WWT\_Recommendation\_Output\_FINAL.xlsx

```

---

## How to Run

1. **Install dependencies**  
```

pip install -r requirements.txt

```

2. **Place the provided datasets** in the project directory or adjust paths in the notebook:
- `order_data.csv`
- `customer_data.csv`
- `store_data.csv`
- `test_data_question.csv`

3. **Run the notebook**  
Open `WingsRUs_Recommendation_Pipeline.ipynb` in Jupyter Notebook or Google Colab and execute all cells in order.

4. **Generated Outputs**  
- `honey_WWT_Recommendation_Output_Cleaned.xlsx` → Cleaned from junk values.  
- `honey_WWT_Recommendation_Output_FINAL.xlsx` → Category-aware, humanized final file.

---

## Model Workflow

1. **Data Loading & Cleaning**  
- Handle missing values, standardize text, remove irrelevant tokens.

2. **Feature Engineering**  
- Build customer-item interaction matrix.
- Generate frequent itemsets with Apriori.

3. **Model Training**  
- Collaborative Filtering using LightFM.
- Cosine similarity fallback model.

4. **Post-Processing**  
- Remove unwanted tokens (`ToGo`, `Delivery`, JSON fragments).
- Apply category-aware replacement for diverse, human-like recs.

5. **Export**  
- Save final recommendations as Excel file for submission.

---

## Business Impact

- **Upselling**: Suggests complementary items to increase average order value.
- **Customer Experience**: Avoids repetitive or irrelevant suggestions.
- **Operational Fit**: Can be integrated into POS or mobile ordering apps.

---
```

