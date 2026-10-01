# Hi, I'm Diomani Ouattara 👋

### Data Scientist | MIT Professional Education (IDSS) | Apziva AI Resident | Edmonton, AB 🇨🇦

I'm a data scientist with experience blending **machine learning**, **predictive modeling**, **applied NLP**, **computer vision**, and **operational analytics** with a background in IT management and international logistics. I turn complex datasets into decisions that actually move the needle — and I'm now taking models to the cloud on **AWS**.

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

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Sentence-Transformers](https://img.shields.io/badge/Sentence--Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**Cloud & Data Engineering**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![Athena](https://img.shields.io/badge/Athena-8C4FFF?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![SageMaker](https://img.shields.io/badge/SageMaker-01A88D?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![AWS Lambda](https://img.shields.io/badge/AWS%20Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)

**Visualization**

![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

## ⭐ Apziva AI Residency Projects

Four end-to-end machine learning projects completed during my AI Residency at **[Apziva](https://www.apziva.com/)**, each solving a real business problem for a client — from raw data to model selection, evaluation, and actionable business recommendations. They span tabular classification, NLP ranking, and on-device computer vision.

### 1️⃣ Customer Happiness Prediction — Logistics & Delivery

**📓 Notebook:** [`1-Predicting Customer Happiness.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/1-Predicting%20Customer%20Happiness.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/1-Predicting%20Customer%20Happiness.ipynb)

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

**📓 Notebook:** [`2-Term Deposit Subscription Prediction.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/2-Term%20Deposit%20Subscription%20Prediction.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/2-Term%20Deposit%20Subscription%20Prediction.ipynb)

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

- ✅ **ROC-AUC 0.949** with Gradient Boosting under 5-fold stratified CV — client's 81% accuracy target exceeded, all five models cleared the bar. Accuracy alone is not the headline here: predicting "no" for everyone already scores ~93%
- 🎯 **Average Precision 0.539 vs. a 0.072 random baseline** — at the chosen threshold the model reaches **64% precision at 41% recall, an 8.9× lift** over the 7.2% base rate. That lift is what makes a call list better than random dialing
- 🎯 Identified a **high-value customer segment converting at 20.1% vs. a 7.2% baseline — a 2.78× uplift** (students/retirees, under-25 and 55+ age bands, engaged calls)
- 📅 Seasonality insight: March, September, October, and December convert best, while May gets the most calls with below-average results — a clear budget-reallocation opportunity
- 📵 Found that more than 3 contact attempts *hurts* conversion — recommended a hard cap of 3 calls per customer per campaign
- 🚀 Proposed next steps: deploy the model as a lead-scoring API, retrain monthly, and A/B test model-ranked call lists against random dialing

---

### 3️⃣ Potential Talents — Candidate Ranking & Relevance-Feedback Search

**📓 Notebook:** [`3-Potential Talents Ranking.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/3-Potential%20Talents%20Ranking.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/3-Potential%20Talents%20Ranking.ipynb)

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

### 4️⃣ MonReader — Page-Flip Detection for a Mobile Document Scanner

**📓 Notebook:** [`4-MonReader_Page_Flip_Detection.ipynb`](https://github.com/diomani-ouattara/Portfolio-Data-scientist/blob/main/4-MonReader_Page_Flip_Detection.ipynb) &nbsp;|&nbsp; [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/diomani-ouattara/Portfolio-Data-scientist/blob/main/4-MonReader_Page_Flip_Detection.ipynb)

**The Business Problem**

MonReader is a phone app that scans books automatically while the user flips the pages. To capture each page in high resolution at the right moment, the app has to know **whether a page is being flipped from a single camera frame**. The data: **2,989 phone frames** (1080×1920) cut from **65 videos**, labelled *flip* / *not flip*. Metric: **F1**, with *flip* as the positive class. Bonus challenge: decide whether a whole **sequence** of frames contains a flip.

**Project Flow**

| Step | What I Did | Why It Matters |
|---|---|---|
| 1. EDA | Parsed `VideoID_FrameNumber` from every filename; checked class balance (~49% flip) and looked at what a flip actually looks like | Visual cues are a lifted corner, a curved page and motion blur on the moving page — so **blur augmentation was ruled out**, because blur is the signal |
| 2. Leakage Check | Compared video IDs and frame numbers across the official train and test folders | **All 65 test videos also appear in training**, often with test frame 20 sitting between training frames 19 and 21. The official test score will be optimistic |
| 3. Honest Validation | Held out **whole videos** (20%) as a validation set — no frame of a validation video is ever trained on | This is the realistic setting: a new book, a new hand, a new phone. Model and threshold selection use this split only |
| 4. Classical Baseline | PCA + logistic regression on 64×36 thumbnails, plus a sharpness-only (Laplacian variance) model | The pixel baseline scores **0.958 F1 on the official test but 0.822 on unseen videos** — direct proof that it memorises videos. Global sharpness alone is weak (0.23) |
| 5. Transfer Learning | Fine-tuned two **mobile-sized** ImageNet CNNs — MobileNetV3-Large and EfficientNet-B0 (~5M parameters each) — with AdamW, cosine schedule, mixed precision | The app runs on a phone, so the model must be small *and* understand the **shape** of a turning page, not global brightness |
| 6. Threshold Tuning | Picked the F1-maximising threshold on validation, applied it **unchanged** to test | Tuning on test would leak again |
| 7. Explainability | Error review of the misclassified frames + **Grad-CAM** heat maps | Confirms the model looks at the lifted page and the hand, not the background |
| 8. Sequence Detection | Aggregated frame probabilities over each clip with three rules — mean, max, and a **3-frame moving average** | The moving-average rule behaves like a real-time trigger: it ignores one-frame spikes and fires when a flip persists |
| 9. Mobile Export | Exported to **TorchScript** and measured single-frame CPU latency | Deployment-ready artefact, loadable by PyTorch Mobile / ExecuTorch or convertible to TFLite / Core ML |

**Key Results & Impact**

| Model | F1 — unseen videos (honest) | F1 — official test |
|---|---|---|
| PCA + logistic regression (baseline) | 0.822 | 0.958 |
| MobileNetV3-Large | 0.974 | 0.990 |
| **EfficientNet-B0 (selected)** | **0.994** | **0.997** |
| Sequence level, 3-frame window rule | 1.000 (21 clips) | **1.000 (115 clips)** |

- ✅ **F1 0.994 on videos the model has never seen** — the number I'd quote for a new user — and 0.997 on the official test set: **2 errors out of 597 frames**, recall 1.00 on flips
- 🔍 **Found and quantified test-set leakage** that the brief didn't mention, then built the evaluation around it instead of reporting the flattering number alone
- 🎞️ **Sequence-level challenge solved** with a 3-frame moving-average trigger — perfect F1 on all 115 test clips
- 📱 **17 MB TorchScript model, ~44 ms per frame (~23 FPS) on CPU** — fast enough to run live on a phone

`Python` `PyTorch` `torchvision` `EfficientNet` `MobileNetV3` `Transfer Learning` `Grad-CAM` `TorchScript` `Scikit-learn`

---

## ☁️ Cloud — AWS in 30 Days

**📂 Repo:** [`aws-30-days`](https://github.com/diomani-ouattara/aws-30-days) &nbsp;·&nbsp; *self-directed, in progress (Week 3 of 4)*

A data-science-focused build on AWS (`ca-central-1`), one dataset end to end: **9.5M NYC yellow-taxi trips** (Jan–Mar 2024) going **S3 → Glue / Athena → SageMaker → deployment**. Every day is committed with the numbers it produced.

| Area | What I Built | Result |
|---|---|---|
| Identity & guardrails | Root locked with MFA, IAM group + hand-written least-privilege policies, instance and execution **roles instead of copied keys** | Analyst user can read `raw/` and nothing else; the SageMaker role can't write `raw/` — tested, not assumed |
| Storage layout | Versioned S3 bucket laid out `raw/ → processed/ → features/ → models/ → outputs/`, lifecycle rule on outputs | The layout used by real data teams |
| CSV vs Parquet | Same 2.96M rows read from S3 in pandas | Parquet **5.2× smaller and 9× faster** to read, and keeps the schema |
| SQL over the lake | Glue Data Catalog (crawler vs. hand-written DDL), Athena CTAS, `year/month` partitioning | The same query scans **314 MB as CSV → 4.7 MB as partitioned Parquet** — Athena bills per byte scanned |
| Leakage-safe features in SQL | Date-based split (train Jan–Feb, validate Mar), target encoding on training months only, `total_amount` excluded because it contains the tip | 7.18M credit-card trips in a versioned `features/v1/` table |
| Event-driven Lambda | S3-triggered function logs each new file's rows and columns by reading **only the Parquet footer** | A 50 MB upload costs one 64 KB range request instead of a full download |
| SageMaker | Model trained in a notebook instance, then as managed training jobs (built-in XGBoost and script mode) | Tip model **MAE $1.24** vs. $1.33 for a one-line rule and $2.45 for the mean (R² 0.65) |

The honest read from Day 16: a one-line rule (zone tip rate × fare) already gets most of the way, because tipping is mostly a percentage of the fare. The model's gain is real but modest — and it's written down that way.

`AWS` `S3` `IAM` `EC2` `Glue` `Athena` `Lambda` `SageMaker` `CloudWatch` `boto3` `SQL` `Parquet`

---

## 🚀 Other Projects

### Applied Machine Learning

#### 🚌 NYC Bus Ride Duration Prediction
> Engineered features from **1.5M+ rows** of public transit data (time of day, weather, holidays) to predict trip durations using Gradient Boosting — achieving a **15% improvement in RMSE** over baseline.

`Python` `Pandas` `Scikit-learn` `Random Forest` `Gradient Boosting`

#### 🏥 Hospital Length of Stay (LOS) Prediction
> Built a regression model for HealthPlus hospital to predict patient discharge timelines from clinical and demographic data available at admission. Achieved a Mean Absolute Error of **±2.1 days**, enabling better allocation of beds, equipment, and staff — and surfaced the factors that drive long stays.

`Python` `Neural Networks` `Regression Analysis`

#### ✈️ Travel Package Purchase Prediction
> Binary classification model identifying customer segments most likely to purchase a travel package. Achieved **85% ROC-AUC**, providing a targeted marketing framework projected to increase conversion rates by **15–20%**.

`Logistic Regression` `Random Forest` `Classification`

#### 👥 HR Employee Attrition Prediction
> Classification model predicting which employees are at risk of leaving, so retention incentives can be focused where they matter. Identified the key factors driving attrition, helping People Operations cut retention spending without losing top talent.

`Python` `Classification` `Feature Importance`

#### 🎓 Skool — Lead Conversion Prediction
> For an ed-tech startup, built an ML model to score which leads are most likely to convert to paid customers, identified the factors driving conversion, and profiled high-potential leads — enabling smarter allocation of the sales team's time.

`Python` `Classification` `Customer Profiling`

#### ☕ AB Roasters — Coffee Quality Prediction
> Regression model predicting roasted coffee quality (0–100) from **17 sensor variables** — chamber temperatures across five compartments, raw-material volume, and humidity — so the company can price its beans accurately.

`Python` `Regression` `Sensor Data`

#### 🛒 BigMart & SuperKart — Retail Sales Forecasting
> Predictive models estimating product- and store-level sales across multi-outlet retail chains (1,559 products, 10 stores for BigMart; quarterly revenue forecasts for SuperKart) — driving inventory planning and revealing which product and store properties boost sales.

`Python` `Regression` `Sales Forecasting`

#### 🚗 Cars4U — Used Car Price Prediction
> Pricing model for the Indian pre-owned car market, predicting used car prices to power a differential pricing strategy — with EDA, modeling, and business recommendations on the factors that most affect resale value.

`Python` `Regression` `Pricing Strategy`

#### 📺 Effects of Advertising on Sales
> Regression case study quantifying how TV, radio, and newspaper ad budgets each drive sales — and predicting sales from a given advertising mix.

`Python` `Linear Regression` `Marketing Analytics`

#### 📈 Network Stock Portfolio Optimization
> Applied Modern Portfolio Theory to historical stock data to optimize asset allocation and maximize the Sharpe ratio.

`Python` `Financial Analysis` `Statistical Modeling`

---

### Software & Automation Builds

#### 🏘️ Rentora — Property Management Platform
> Full-stack SaaS MVP for the Alberta rental market: a Next.js web portal, an Expo iOS/Android app, and a shared Supabase (PostgreSQL) backend with **row-level security** so landlords, property managers, tenants and vendors each see only their own data. Properties, units, leases, rent and maintenance modelled in a relational schema.

`Next.js` `TypeScript` `Expo` `Supabase` `PostgreSQL` `Row-Level Security`

#### 🔎 Multi-Source Lead Generation Pipeline
> An AI agent directs deterministic Python tools to collect, clean, de-duplicate and enrich **~150 B2B leads** for an Edmonton contractor from OpenStreetMap, City of Edmonton open data (Socrata API) and HTML directories. Honours `robots.txt`, runs its tests offline against saved fixtures, and logs every selector fix as a regression test.

`Python` `Requests` `BeautifulSoup` `Playwright` `REST APIs` `pytest` `SQLite`

---

### Computer Vision & Deep Learning
> *MIT Professional Education coursework — course case studies, not client engagements.*

#### 🧠 Brain Tumour MRI Classification
> Binary classifier separating pituitary-tumour from no-tumour MRI scans across **1,000 images** (830 training / 170 test). Built a CNN baseline, applied **data augmentation** to control overfitting on a small medical dataset, then improved it further with **transfer learning** from a pre-trained architecture.

`Python` `TensorFlow` `Keras` `CNN` `Transfer Learning` `Data Augmentation`

#### 🌱 Plant Seedlings Classification
> Species classifier across **12 plant species** at varying growth stages (Aarhus University / University of Southern Denmark dataset), aimed at cutting the manual sorting effort that still dominates crop monitoring.

`Python` `TensorFlow` `Keras` `CNN` `Image Classification`

#### 🍚 Rice Variety Classification
> Five-class CNN separating Arborio, Basmati, Ipsala, Jasmine and Karacadag grains — the grading step that gates agricultural rice export.

`Python` `Keras` `CNN` `Multi-class Classification`

#### 🏠 SVHN Street View Digit Recognition
> Transcribing house numbers from street-level photography (600k+ labelled digits; subset used). Built **twice on identical data** — first a feed-forward ANN, then a CNN — so the two architectures could be compared directly rather than asserted.

`Python` `TensorFlow` `Keras` `ANN` `CNN`

#### 🔊 Audio MNIST Spoken-Digit Recognition
> Classifying spoken digits 0–9 by converting audio into **MFCC spectrograms** and treating sound as a 2-D image — sidestepping the storage and compute cost of raw waveform amplitudes.

`Python` `librosa` `Keras` `ANN` `Spectrogram Processing`

#### 🍞 Food Image Classification
> Auto-labelling stock photography into Bread, Soup and Vegetables-Fruits for an image agency where daily upload volume makes manual tagging impossible.

`Python` `Keras` `CNN` `Image Classification`

#### ✍️ MNIST Handwritten Digit Classification
> Baseline CNN on the classic 28×28 benchmark, evaluated and then improved — the standard proving ground for convolutional architectures.

`Python` `Keras` `CNN`

---

### Recommendation Systems
> *MIT Professional Education coursework.*

#### 🛒 Amazon Product Recommendation System
> Recommending products from customers' prior ratings at a scale where response has to be real-time — built around item-to-item collaborative filtering, the baseline approach Amazon itself uses.

`Python` `Collaborative Filtering` `Matrix Factorization`

#### 🍴 Yelp Restaurant Recommender
> **Four** recommender types built and compared on the same review corpus (~11 GB in full; subset used): knowledge/rank-based, similarity-based collaborative filtering, matrix factorization, and clustering-based.

`Python` `Collaborative Filtering` `Matrix Factorization` `Clustering`

#### 🎵 Spotify Music Recommender
> Proposing the top 10 next songs per listener by predicted likelihood of listening, from a preference database of millions of users and billions of plays.

`Python` `Rank-Based Recommenders` `Collaborative Filtering`

#### 📚 Book Recommendation System
> Three recommender types for an e-commerce reading catalogue — rank-based, similarity-based collaborative filtering, and matrix factorization.

`Python` `Collaborative Filtering` `Matrix Factorization`

---

### Unsupervised Learning & Dimensionality Reduction
> *MIT Professional Education coursework.*

#### 🧬 Genomic Data Clustering — verifying the genetic code
> Given a **300 kb fragment of the *Caulobacter crescentus* genome** and no labels whatsoever, split the sequence into non-overlapping 300-base substrings, counted 1-, 2-, 3- and 4-mer frequencies, applied PCA to expose internal structure, then clustered. **The three-letter codon structure of DNA falls out of the clustering** — a twentieth-century discovery re-derived by unsupervised learning alone.

`Python` `PCA` `K-Means` `Feature Extraction`

#### 🌍 Country Socio-Economic Clustering
> Grouping countries by development profile beyond GDP alone — across child mortality, exports, health spend, imports, income, inflation, life expectancy, fertility and GDP per capita — for government and NGO targeting.

`Python` `K-Means` `Hierarchical Clustering` `Scikit-learn`

#### 💳 AllLife Bank Credit-Card Segmentation
> Segmenting a credit-card base by spending pattern **and** past support interaction, so Marketing could run personalized campaigns and Operations could fix a service model customers rated poorly.

`Python` `Clustering` `Customer Segmentation`

#### 🏫 US Education Institutes — PCA
> Reducing a wide institutional dataset — applications, enrollment, faculty education, finances, graduation rate — to the handful of components that actually drive it.

`Python` `PCA` `Dimensionality Reduction`

#### 👤 Face Identification with Eigenfaces
> Classifying faces in photographic images by projecting them into a low-dimensional face space.

`Python` `PCA` `Eigenfaces` `Image Classification`

#### 📝 LDA Topic Modeling on Faculty Text
> Surfacing latent research themes across MIT EECS faculty pages — scraped, pre-processed, and modelled with Latent Dirichlet Allocation via stochastic variational inference.

`Python` `Web Scraping` `NLP` `LDA` `Topic Modeling`

---

### Networks, Graphical Models & Neural Networks
> *MIT Professional Education coursework.*

#### 🕸️ CAVIAR Criminal Network Analysis
> A Montreal drug-trafficking network across a two-year joint Montreal Police / RCMP investigation (**1994–1996**) — a rare chance to watch a network *restructure* under escalating seizures rather than sit still. Built and visualised the graph phase by phase, then tracked **centrality measures** to see how influence migrated between actors as the network came under pressure.

`Python` `NetworkX` `Graph Theory` `Centrality Measures`

#### 🎯 3-D Object Tracking with a Kalman Filter
> Recovering the true position and velocity of a ball moving under gravity from noisy simulated sensor readings.

`Python` `Kalman Filter` `State Estimation`

#### 🎓 UCLA Admission Chance Prediction
> Predicting a student's admission probability from their profile, to help applicants shortlist realistically.

`Python` `Neural Networks` `Classification`

#### 💼 Data Scientist Job-Change Prediction
> Predicting which training-programme candidates will seek a new job rather than join the company — and interpreting *which* factors drive that decision, so training spend isn't wasted on candidates who will leave.

`Python` `Classification` `Feature Importance`

## 📊 Areas of Expertise

- Predictive Modeling & Statistical Analysis
- Feature Engineering & Data Wrangling
- Imbalanced Classification & Model Evaluation (ROC-AUC, Precision-Recall, Average Precision)
- **Computer Vision** — image classification, CNNs, data augmentation, transfer learning (EfficientNet, MobileNetV3), Grad-CAM, TorchScript export for mobile
- **Cloud & Data Engineering (AWS)** — S3 data lakes, IAM least privilege, Glue Data Catalog, Athena SQL, partitioned Parquet, Lambda, SageMaker training
- **Audio & Signal Processing** — MFCC spectrograms, treating sound as image data
- **NLP & Information Retrieval** — sentence embeddings, hybrid retrieval, relevance feedback, LDA topic modeling, web scraping
- **Recommendation Systems** — collaborative filtering, matrix factorization, content-, rank- and clustering-based
- **Deep Learning** — ANNs, CNNs, transfer learning, TensorFlow & Keras
- **Unsupervised Learning** — PCA, t-SNE, K-Means, hierarchical clustering, Gaussian mixtures, eigenfaces
- **Graph & Network Analysis** — centrality measures, time-varying network structure
- **State Estimation** — Kalman filtering for noisy sensor data
- Classical ML — KNN, decision trees, bagging, random forest, SVM, ridge & lasso regularization
- Ranking Evaluation — NDCG, MAP, Recall@K
- Responsible AI — bias auditing, disparate impact analysis, counterfactual testing
- Time Series Analysis & A/B Testing
- Cross-Validation (stratified and grouped), Data-Leakage Detection, Bootstrapping, Customer Segmentation
- Supply Chain & Logistics Optimization

## 🎓 Education & Certifications

| Credential | Institution | Year |
|---|---|---|
| AI Residency Program | Apziva | 2026 – present |
| Data Science & Machine Learning: Making Data-Driven Decisions | MIT Institute for Data, Systems and Society | 2023 |
| Supply Chain Logistics, Operations and Planning | Rutgers University | 2020 |
| Bachelor's in Network Administration | Institute of Technology, Abidjan | 2010 |

### 📚 MIT Applied Coursework

The MIT Professional Education programme ran as **21 applied case studies** across four modules — unsupervised learning, recommendation systems, deep learning, and networks & graphical models. They are written up individually under [Other Projects](#-other-projects) above, each labelled as coursework rather than client work.

**Methods toolkit across the programme:** KNN, decision trees, bagging, random forest, linear and logistic regression, ridge & lasso, SVM, bootstrapping, cross-validation, clustering, association rules, dimensionality reduction (PCA, t-SNE), graph theory, gradient descent, activation functions and regularization — with NumPy, Pandas, Seaborn, Matplotlib, statsmodels, scikit-learn, TensorFlow and Keras.

## 💼 A Note for Hiring Managers & Recruiters

If you're evaluating my work, the four **Apziva residency notebooks** above are the best place to start — they show how I operate end-to-end on real client problems:

- **I start with the business question, not the algorithm.** Every project opens from the client's question — two with explicit accuracy targets (73% and 81%), one with a shortlist a recruiter had to trust, one with a camera trigger that has to run on a phone — and ends with recommendations a non-technical stakeholder can act on.
- **I evaluate honestly.** Stratified splits, 5-fold cross-validation, train-vs-test comparisons to expose overfitting, and imbalance-aware metrics (ROC-AUC, Average Precision) instead of headline accuracy alone. In the ranking project I measured feedback against a control that receives the same stars and ignores them — because the honest baseline is the drift, not zero. In MonReader I found that the client's test set shared videos with training, and selected the model on unseen videos instead.
- **I audit for bias before it ships.** The ranking engine excludes network size and location from scoring on documented evidence, and proves location-invariance with a counterfactual test rather than asserting it in a disclaimer.
- **I ship insights, not just models.** Survey questions to cut, customer segments with a 2.78× conversion uplift, contact-attempt caps, seasonal budget shifts, a 17 MB model that runs at ~23 FPS on CPU — every project closes the loop from prediction to decision.
- **I'm learning the production side.** My [AWS in 30 Days](https://github.com/diomani-ouattara/aws-30-days) repo takes one dataset from S3 through Athena to SageMaker, with every day's cost and result written down.

I'm currently open to **data scientist / ML roles** — remote or based in Edmonton, AB. Let's talk.

---

## 🌍 About Me

- 🇨🇦 Based in **Edmonton, AB**
- 🗣️ Fluent in **English** and **French (Native)**
- 🤝 Volunteer at **Hope Mission, Edmonton** — food distribution & inventory for 50+ community members weekly
- 💼 12 years in IT management and international logistics (oil & gas, West Africa), now a power engineer in Edmonton

---

## 📬 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/diomani-ouattara)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:odiomani@yahoo.com)
