# Hi, I'm Diomani Ouattara 👋

### Data Scientist | MIT Professional Education (IDSS) | Apziva AI Resident | Edmonton, AB 🇨🇦

I'm a data scientist with experience blending **machine learning**, **predictive modeling**, **applied NLP**, and **operational analytics** with a background in IT management and international logistics. I turn complex datasets into decisions that actually move the needle.

---

## 🧠 Tech Stack

**Languages & Databases**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)

**Machine Learning & Data Science**

![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EB4C2C?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

**Deep Learning & NLP**

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Sentence-Transformers](https://img.shields.io/badge/Sentence--Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**Visualization**

![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

## ⭐ Apziva AI Residency Projects

Three end-to-end machine learning projects completed during my AI Residency at **[Apziva](https://www.apziva.com/)**, each solving a real business problem for a client — from raw data to model selection, evaluation, and actionable business recommendations.

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

### 3️⃣ Potential Talents — Candidate Ranking & Relevance-Feedback Search

**📓 Notebook:** [`Potential_Talents_Ranking.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/Potential_Talents_Ranking.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/Potential_Talents_Ranking.ipynb)

**The Business Problem**

A recruiting team sources candidates by typing a role keyword — *"aspiring human resources"*, *"seeking human resources"* — and gets back a raw, noisy list. They needed every candidate scored with a `fit` value in **[0, 1]**, ranked, and the whole list **re-ranked every time a recruiter stars an ideal candidate**. The catch: the `fit` column is empty. There is no label to learn from, which makes this an **unsupervised ranking problem** where the only supervision ever available is a single click.

**Project Flow**

| Step | What I Did | Why It Matters |
|---|---|---|
| 1. Exploratory Analysis | Checked for a target, counted true duplicates, parsed `connections`, profiled `location` | No `fit` values → rules out supervised regression. Roughly half the rows are exact duplicates, and `connections` is censored at `"500+"` |
| 2. Cleaning & De-duplication | Expanded HR acronyms (`HRBP`, `CHRO`, `SPHR` → full text), normalised characters, de-duplicated while **keeping** the duplicate count | **104 raw rows → 53 distinct candidates.** Expanding acronyms before encoding is the cheapest accuracy gain in the pipeline — embeddings have seen "human resources" far more than "HRBP" |
| 3. Pre-filter | Advertisement detector (phone regex, promotional punctuation, employer framing), HR domain-lexicon check, near-duplicate detection at cosine > 0.97 | **The worst entries score *highest*.** A staffing-agency ad contains the query phrase verbatim, so similarity ranks it top — only a *structural* detector catches it. Everything is flagged, never silently deleted |
| 4. Hybrid Representation | SBERT (`all-MiniLM-L6-v2`) dense embeddings **+** TF-IDF 1–2 grams, with an automatic TF-IDF + SVD fallback | The two fail in opposite ways: dense supplies recall and handles synonyms ("People Development Coordinator" *is* an HR role), sparse supplies precision and never confuses "aspiring" with "director" |
| 5. Base Fitness Score | Query expansion into several paraphrases, then 60% dense / 40% lexical fusion | Averaging paraphrase embeddings puts the query at the *centre* of the concept rather than on one phrasing, which measurably stabilises the ranking |
| 6. Evaluation Framework | Wrote a documented 0–3 **graded relevance rubric**, then measured with NDCG / recall@k / MAP | With no labels, every claim needs an explicit reference. Graded relevance captures that a sitting CHRO is a poor fit *for an "aspiring HR" search* while still being a real HR person |
| 7. Starring Engine | Three fused feedback channels: nearest-ideal similarity (**max**, not mean), L2-regularised logistic re-weighting on TF-IDF, and a Rocchio query update | Max keeps two different starred profiles as **separate poles of attraction** instead of collapsing them into a meaningless midpoint. The logistic channel can seize on one decisive token (`student`) immediately |
| 8. Star Experiment | 40 random star subsets per star count; starred profiles removed from **both** the list and the evaluation set; measured against a no-feedback control given the same stars | Guards against the two classic traps — self-congratulation (of course a starred candidate ranks highly) and luck (one sequence proves nothing). The control drifts upward on its own, and **that drift is the real baseline** |
| 9. Automatic Cut-off | Null-calibration against ~100 unrelated job titles (robust z-score via median/MAD), then three-estimator banding — knee, Gaussian mixture, Otsu | Min-max scores always put the best candidate at 1.0 *even if nobody is suitable*. Asking "how much better than a random professional?" means the same thing for every role — that's what makes the threshold transfer |
| 10. Bias Audit | Correlation of `connections` with relevance, counterfactual location-swap test, MMR diversity re-ranking, feedback-weight caps | Automation doesn't remove bias, it **scales** it — a biased ranker mistreats every candidate, consistently, while looking objective |

**Key Results & Impact**

- ✅ **NDCG@10 in the mid-90s** against the stated keyword — and honest about *why*: many titles literally contain the query, so keyword search is already adequate for the easy part of this problem
- ⭐ **Roughly 4× recall@10** of still-unseen ideal candidates within four stars, versus **~2× for a no-feedback control** receiving the same stars — the average ideal climbs **~7 positions, from page two onto page one**. The first star is worth the most
- 🧹 **104 raw rows → 53 distinct candidates**, with staffing-agency job ads removed by a structural detector rather than by a similarity score that actively favours them
- 🎚️ **A cut-off that transfers across roles:** the same untouched code and constants keep a full review queue for HR roles and collapse to almost nobody for *"full-stack software engineer"* or *"registered nurse"* — with **zero per-role tuning**
- ⚖️ **`connections` proven to be a fairness trap:** its correlation with relevance is statistically indistinguishable from zero *and negatively signed* — the target persona (aspiring, entry-level) has the **fewest** connections while senior executives sit at the 500+ ceiling. Excluded from scoring; `location` proven non-influential by a counterfactual swap test rather than merely promised
- 🔁 Shipped as a production wrapper (`search` / `star` / `reject` / `results`) with three-band output — **shortlist / review / reject** — so uncertainty is surfaced to the recruiter instead of hidden behind one arbitrary line

`Python` `Sentence-Transformers (SBERT)` `Scikit-learn` `TF-IDF` `Logistic Regression` `Gaussian Mixture Models` `NDCG / MAP` `Bias Auditing`

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
- Imbalanced Classification & Model Evaluation (ROC-AUC, Precision-Recall, Average Precision)
- NLP & Information Retrieval — sentence embeddings, hybrid retrieval, relevance feedback, topic modeling
- Deep Learning — ANNs, CNNs, transfer learning, data augmentation
- Recommendation Systems — collaborative filtering, matrix factorization, content- and rank-based
- Unsupervised Learning — PCA, t-SNE, K-Means, hierarchical clustering, Gaussian mixtures
- Network & Graph Analysis — centrality measures
- Ranking Evaluation — NDCG, MAP, Recall@K
- Responsible AI — bias auditing, disparate impact analysis, counterfactual testing
- Time Series Analysis & A/B Testing
- Cross-Validation, Bootstrapping, Customer Segmentation
- Supply Chain & Logistics Optimization

---

## 🎓 Education & Certifications

| Credential | Institution | Year |
|---|---|---|
| AI Residency Program | Apziva | 2026 |
| Data Science & Machine Learning: Making Data-Driven Decisions | MIT Institute for Data, Systems and Society | 2023 |
| Supply Chain Logistics, Operations and Planning | Rutgers University | 2020 |
| Bachelor's in Network Administration | Institute of Technology, Abidjan | 2010 |

### 📚 MIT Applied Coursework

Case studies completed within the MIT Professional Education program, grouped by module:

**Unsupervised Learning** — genomic sequence clustering (verifying the three-letter codon structure in *Caulobacter crescentus* by unsupervised learning alone), country socio-economic clustering, US education-institute PCA, AllLife Bank credit-card customer segmentation, LDA topic modeling on faculty text, and PCA-based face identification.

**Recommendation Systems** — Spotify music, Yelp restaurant, book, and Amazon product recommenders spanning rank/knowledge-based, similarity-based collaborative filtering, matrix factorization, and clustering-based approaches.

**Deep Learning** — rice-variety classification (5 classes, CNN), SVHN street-view digit recognition (ANN *and* CNN), Audio MNIST spoken-digit recognition from MFCC spectrograms, brain-tumor MRI classification with data augmentation and transfer learning, plant-seedling classification (12 species), food image classification, UCLA admission-chance prediction, and data-scientist job-change prediction.

**Networks & Graphical Models** — the CAVIAR criminal-network investigation (centrality measures tracked across phases of a network under escalating police disruption) and 3-D object tracking from noisy sensor estimates with a Kalman filter.

> These are structured course case studies rather than client engagements — listed for the breadth of methods covered, not as commissioned work.

---

## 💼 A Note for Hiring Managers & Recruiters

If you're evaluating my work, the three **Apziva residency notebooks** above are the best place to start — they show how I operate end-to-end on real client problems:

- **I start with the business question, not the algorithm.** Both projects open with a clear target set by the client (73% and 81% accuracy) and end with recommendations a non-technical stakeholder can act on.
- **I evaluate honestly.** Stratified splits, 5-fold cross-validation, train-vs-test comparisons to expose overfitting, and imbalance-aware metrics (ROC-AUC, Average Precision) instead of headline accuracy alone. In the ranking project I measured feedback against a control that receives the same stars and ignores them — because the honest baseline is the drift, not zero.
- **I audit for bias before it ships.** The ranking engine excludes network size and location from scoring on documented evidence, and proves location-invariance with a counterfactual test rather than asserting it in a disclaimer.
- **I ship insights, not just models.** Survey questions to cut, customer segments with a 2.78× conversion uplift, contact-attempt caps, seasonal budget shifts — every project closes the loop from prediction to decision.

I'm currently open to **data scientist / ML roles** — remote or based in Edmonton, AB. Let's talk.

---

## 🌍 About Me

- 🇨🇦 Based in **Edmonton, AB**
- 🗣️ Fluent in **English** and **French (Native)**
- 🤝 Volunteer at **Hope Mission, Edmonton** — food distribution & inventory for 50+ community members weekly
- 💼 12 years in IT management and international logistics (oil & gas, West Africa)

---

## 📬 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/diomani-ouattara)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:odiomani@yahoo.com)
