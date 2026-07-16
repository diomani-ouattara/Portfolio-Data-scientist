# Hi, I'm Diomani Ouattara 👋

### Certified Data Scientist | MIT | Apziva AI Resident | Edmonton, AB 🇨🇦

I'm a data scientist with experience blending **machine learning**, **predictive modeling**, and **operational analytics** with a background in IT management and international logistics. I turn complex datasets into decisions that actually move the needle.

---

## 🧠 Tech Stack

**Languages & Databases**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

**Machine Learning & Data Science**

![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EB4C2C?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

**Visualization**

![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

## ⭐ Apziva AI Residency Projects

Two end-to-end machine learning projects completed during my AI Residency at **[Apziva](https://www.apziva.com/)**, each solving a real business problem for a client — from raw data to model selection, evaluation, and actionable business recommendations.

### 1️⃣ Customer Happiness Prediction — Logistics & Delivery

**📓 Notebook:** [`0hhwPRi6B4fBj84R.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/0hhwPRi6B4fBj84R.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/0hhwPRi6B4fBj84R.ipynb)

**The Business Problem**

A fast-growing logistics and delivery startup wanted to know **which customers are unhappy — and why — before they churn**. Using a customer survey (126 responses, six 1–5 satisfaction ratings covering delivery timeliness, order accuracy, pricing, courier service, and app experience), the goal was to predict overall happiness with **at least 73% accuracy** and identify the minimal set of survey questions that actually matter.

**Project Flow**

| Step | What I Did | Why It Matters |
|---|---|---|
| 1. Data Quality Audit | Checked shape, dtypes, missing values, and statistical summary | Confirmed a clean, complete dataset before modeling |
| 2. Exploratory Data Analysis | Class balance plot, per-feature boxplots vs. target, correlation heatmap | Found a mild class imbalance (55% happy) and no strong feature correlations — every feature carried independent signal |
| 3. Stratified Train/Test Split | 80/20 split, stratified on the target | Preserves class proportions so the test set is a fair benchmark |
| 4. Baseline Modeling (all 6 features) | Trained Logistic Regression, Random Forest, and Gradient Boosting; evaluated on **both** train and test sets | Best test accuracy was only 65% — and the train/test gap exposed heavy overfitting on such a small dataset |
| 5. Feature Selection | Ranked features with Random Forest importance; kept the **top 3** | Fewer features = less overfitting on 126 rows, plus a shorter survey for the business |
| 6. Retrain & Compare | Re-ran all three models on the reduced feature set | **Gradient Boosting reached 73.1% test accuracy (F1 = 0.76) — meeting the 73% client target** |
| 7. Business Insights | Analyzed low-rating patterns among unhappy customers; translated model output into operations changes | The model is only useful if the client knows what to fix |

**Key Results & Impact**

- ✅ **73.1% test accuracy** with Gradient Boosting — client target met
- ✂️ Showed that **half of the survey questions can be dropped** with no loss of predictive power — the client can shorten its survey and increase response rates
- 📦 Delivery-experience features (order completeness, on-time delivery, order accuracy) dominate happiness — leading to concrete recommendations: automatic compensation for late deliveries, weekly courier feedback loops, and app UX improvements

---

### 2️⃣ Term Deposit Subscription Prediction — European Banking

**📓 Notebook:** [`c4f8JGcuEvcMtTJI.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/c4f8JGcuEvcMtTJI.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/c4f8JGcuEvcMtTJI.ipynb)

**The Business Problem**

A European bank runs large phone-based marketing campaigns to sell term deposits, but only **~7% of calls convert**. Using **40,000 call records** (customer demographics, finances, and campaign history), the goal was to build a classifier with **at least 81% accuracy under 5-fold cross-validation**, and — just as importantly — tell the bank *who* to call and *when*.

**Project Flow**

| Step | What I Did | Why It Matters |
|---|---|---|
| 1. Load & Inspect | Audited 40,000 × 14 dataset: types, missing values, target distribution | Revealed a **severe class imbalance (~7% "yes")** — plain accuracy alone would be misleading, so ROC-AUC and Average Precision were tracked throughout |
| 2. Exploratory Data Analysis | Distributions by subscription outcome, subscription rate by every categorical feature, correlation matrix | Surfaced the patterns (call duration, seasonality, job type) that later drove both features and business advice |
| 3. Feature Engineering | Built 5 new features: log-transformed balance, high-balance flag, over-contacted flag, age life-stage buckets, duration in minutes | Captured non-linear effects (U-shaped age curve, balance outliers) that raw columns hide |
| 4. Model Tournament | 5 models — Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost — under **5-fold stratified cross-validation**, with class weighting for the imbalance; compared via accuracy boxplots, ROC curves, and Precision-Recall curves | Out-of-fold evaluation gives an honest estimate of real-world performance |
| 5. Best-Model Deep Dive | Full evaluation of Gradient Boosting on train / CV / test: classification reports, confusion matrix, overlaid ROC & PR curves | Verified the model generalizes rather than memorizes |
| 6. Feature Importance | Ranked drivers of subscription | Call duration, month, and customer age lead — and duration is flagged as a *post-call* signal, used for agent coaching rather than pre-call targeting |
| 7. Customer Segmentation | Sliced conversion by job, age band, call duration, and month; combined the best slices into one high-value segment | Gives the bank an explainable targeting rule that works even without the model |
| 8. Recommendations | Consolidated scorecard + prioritized action list | Turns the analysis into a campaign playbook |

**Key Results & Impact**

- ✅ **93.6% cross-validated accuracy** with Gradient Boosting (ROC-AUC 0.949) — **beating the 81% target by more than 12 points**; all five models cleared the bar
- 🎯 Identified a **high-value customer segment converting at 20.1% vs. a 7.2% baseline — a 2.78× uplift** (students/retirees, under-25 and 55+ age bands, engaged calls)
- 📅 Seasonality insight: March, September, October, and December convert best, while May gets the most calls with below-average results — a clear budget-reallocation opportunity
- 📵 Found that more than 3 contact attempts *hurts* conversion — recommended a hard cap of 3 calls per customer per campaign
- 🚀 Proposed next steps: deploy the model as a lead-scoring API, retrain monthly, and A/B test model-ranked call lists against random dialing

---

## 🚀 Other Projects

### 🚌 NYC Bus Ride Duration Prediction
> Engineered features from **1.5M+ rows** of public transit data (time of day, weather, holidays) to predict trip durations using Gradient Boosting — achieving a **15% improvement in RMSE** over baseline.

`Python` `Pandas` `Scikit-learn` `Random Forest` `Gradient Boosting`

### 🏥 Hospital Length of Stay (LOS) Prediction
> Built a regression model for HealthPlus hospital to predict patient discharge timelines from clinical and demographic data available at admission. Achieved a Mean Absolute Error of **±2.1 days**, enabling better allocation of beds, equipment, and staff — and surfaced the factors that drive long stays.

`Python` `Neural Networks` `Regression Analysis`

### ✈️ Travel Package Purchase Prediction
> Binary classification model identifying customer segments most likely to purchase a travel package. Achieved **85% ROC-AUC**, providing a targeted marketing framework projected to increase conversion rates by **15–20%**.

`Logistic Regression` `Random Forest` `Classification`

### 👥 HR Employee Attrition Prediction
> Classification model predicting which employees are at risk of leaving, so retention incentives can be focused where they matter. Identified the key factors driving attrition, helping People Operations cut retention spending without losing top talent.

`Python` `Classification` `Feature Importance`

### 🎓 Skool — Lead Conversion Prediction
> For an ed-tech startup, built an ML model to score which leads are most likely to convert to paid customers, identified the factors driving conversion, and profiled high-potential leads — enabling smarter allocation of the sales team's time.

`Python` `Classification` `Customer Profiling`

### ☕ AB Roasters — Coffee Quality Prediction
> Regression model predicting roasted coffee quality (0–100) from **17 sensor variables** — chamber temperatures across five compartments, raw-material volume, and humidity — so the company can price its beans accurately.

`Python` `Regression` `Sensor Data`

### 🛒 BigMart & SuperKart — Retail Sales Forecasting
> Predictive models estimating product- and store-level sales across multi-outlet retail chains (1,559 products, 10 stores for BigMart; quarterly revenue forecasts for SuperKart) — driving inventory planning and revealing which product and store properties boost sales.

`Python` `Regression` `Sales Forecasting`

### 🚗 Cars4U — Used Car Price Prediction
> Pricing model for the Indian pre-owned car market, predicting used car prices to power a differential pricing strategy — with EDA, modeling, and business recommendations on the factors that most affect resale value.

`Python` `Regression` `Pricing Strategy`

### 📺 Effects of Advertising on Sales
> Regression case study quantifying how TV, radio, and newspaper ad budgets each drive sales — and predicting sales from a given advertising mix.

`Python` `Linear Regression` `Marketing Analytics`

### 📈 Network Stock Portfolio Optimization
> Applied Modern Portfolio Theory to historical stock data to optimize asset allocation and maximize the Sharpe ratio.

`Python` `Financial Analysis` `Statistical Modeling`

---

## 📊 Areas of Expertise

- Predictive Modeling & Statistical Analysis
- Feature Engineering & Data Wrangling
- Imbalanced Classification & Model Evaluation (ROC-AUC, Precision-Recall)
- Time Series Analysis & A/B Testing
- Deep Learning (ANN) & Recommendation Systems
- Supply Chain & Logistics Optimization
- Cross-Validation, Bootstrapping, Customer Segmentation

---

## 🎓 Education & Certifications

| Credential | Institution | Year |
|---|---|---|
| AI Residency Program | Apziva | 2026 |
| Data Science & Machine Learning: Making Data-Driven Decisions | MIT Institute for Data, Systems and Society | 2023 |
| Supply Chain Logistics, Operations and Planning | Rutgers University | 2020 |
| Bachelor's in Network Administration | Institute of Technology, Abidjan | 2010 |

---

## 💼 A Note for Hiring Managers & Recruiters

If you're evaluating my work, the two **Apziva residency notebooks** above are the best place to start — they show how I operate end-to-end on real client problems:

- **I start with the business question, not the algorithm.** Both projects open with a clear target set by the client (73% and 81% accuracy) and end with recommendations a non-technical stakeholder can act on.
- **I evaluate honestly.** Stratified splits, 5-fold cross-validation, train-vs-test comparisons to expose overfitting, and imbalance-aware metrics (ROC-AUC, Average Precision) instead of headline accuracy alone.
- **I ship insights, not just models.** Survey questions to cut, customer segments with a 2.78× conversion uplift, contact-attempt caps, seasonal budget shifts — every project closes the loop from prediction to decision.

I'm currently open to **data scientist / ML roles** — ideally remote or based in Edmonton, AB. Let's talk.

---

## 🌍 About Me

- 🇨🇦 Based in **Edmonton, AB**
- 🗣️ Fluent in **English** and **French (Native)**
- 🤝 Volunteer at **Hope Mission, Edmonton** — food distribution & inventory for 50+ community members weekly
- 💼 10+ years in IT management and international logistics (oil & gas, West Africa)

---

## 📬 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://https://www.linkedin.com/in/david-diomani-ouattara-b48493214/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:odiomani@yahoo.com)
