
# TrendIQ – AI-Powered Trend & Demand Analyzer

## 📌 Overview
TrendIQ is a smart forecasting engine built to help e-commerce platforms detect emerging product trends and forecast demand across product, category, and attribute levels. It leverages real-world inspired data and machine learning models to generate actionable insights.

---

## 📁 Dataset Ingestion

| File | Description |
|------|-------------|
| `product_catalog.csv` | Contains product IDs, titles, categories, seasons, etc. |
| `sales_data.csv` | Daily product-level sales for one year |
| `search_trends.csv` | Historical search queries with frequency and timestamps |
| `customer_feedback.csv` | User reviews with sentiment and ratings |

---

## 🔍 Trend Detection
- `top_trending_keywords.json`: Built by comparing search query growth across two time periods.
- `trending_category_season.json`: Forecasts top rising categories by season using exponential smoothing.

---

## 🔮 Forecasting Models
- **ARIMA**: For stationary, consistent product-level forecasts
- **XGBoost**: Leverages lag features and external inputs like sentiment and rating
- **LSTM**: Deep learning model for longer sequence prediction

---

## 📈 Visualizations
- Line charts for weekly trend comparison by (category, season)
- Bar charts and forecast plots for comparative analysis

---

## 📦 Output Files
- `top_trending_keywords.json`
- `product_demand_forecast.json`
- `category_season_demand_forecast.json`
- `trending_category_season.json`

---

## 🧠 Assumptions Made
- Search query terms are loosely mapped to categories based on keyword presence.
- Customer sentiment scores are normalized using TextBlob.
- Weekly smoothing used for sparse time series data.
- Seasons are extracted from product modifiers.

---

## 🛠️ Libraries Used
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `xgboost`, `statsmodels`, `tensorflow.keras`
- `plotly` (optional for interactive charts)

---

## ▶️ How to Run
1. Open the notebook in Google Colab
2. Upload the 4 datasets
3. Run all cells from top to bottom
4. Outputs will be generated as `.json` files for evaluation
