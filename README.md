# Superstore Sales Analysis & Forecasting

**End-to-end analysis and time-series forecasting** of the classic Superstore dataset (~10,000 orders, $2.26M revenue).

Goal: Understand business performance, uncover actionable insights, and build reliable monthly sales forecasts using Prophet.

## Project Highlights

### 1. Business & KPI Overview
- Total revenue: **$2,261,537** across **4,922 unique orders** and **793 customers**
- Average Order Value (AOV): **$459**
- Average revenue per customer: **$2,853**
- Strong geographic concentration: **West (31.4%) + East (29.6%) = ~61%** of revenue

### 2. Key Insights Discovered
- **Category dominance**: Technology = **36.4%** of revenue despite fewer orders
- **Customer power law**: Top 1 customer (Sean Miller) = **1.11%** of total revenue  
  Top 10 customers = **6.8%** of revenue
- **Peak day**: March 18, 2015 → **$28,107** (12× average daily sales), 80% from one Cisco TelePresence product
- **Shipping insight**: Standard Class dominates volume (~60%) and revenue proportionally — no strong premium-shipping correlation with higher value
- **Segment behavior**: Home Office & Corporate have highest AOV (~$461–475); Consumer is largest but lowest AOV

### 3. Visualizations Created
- Top 10 states & customers bar charts
- Region revenue share pie chart
- Peak day product breakdown bar chart
- Shipping mode: Orders % vs Revenue % comparison
- Segment: Customer share vs Revenue share + AOV overlay
- Monthly sales trend line

### 4. Time-Series Forecasting (Prophet)
- Built monthly sales forecasts for:
  - **Total sales**
  - **By Region** (West, East, Central, South)
- Used Prophet with yearly seasonality + custom Q4 regressor
- Created 12-month ahead forecasts (future unknown period)
- Compared against seasonal naive baseline (same month avg previous years)
- Exported forecasts to CSV files:
  - `superstore_total_sales_forecast.csv`
  - `superstore_forecast_[region].csv` (per region)
  - `superstore_forecast_all_regions_and_total.csv`
  - `superstore_future_forecast_next_12_months.csv`


### Technologies Used
- Python, pandas, numpy
- matplotlib, seaborn
- Prophet (facebook/prophet)
- scikit-learn (metrics)
- XGBoost (baseline comparison)

### Business Takeaways
- Strong seasonality → Q4 / holiday periods drive spikes
- High customer & geographic concentration → focus retention & regional marketing
- Reliable forecasts enable better inventory & cash-flow planning

### Next Steps / Potential Extensions
- Add Black Friday / Cyber Monday holiday flags
- Forecast by product category
- Customer-level lifetime value prediction
- Deploy dashboard (Streamlit / Dash)

Feel free to ⭐ the repo or fork it!

Questions / feedback? → Open an issue or reach out.
