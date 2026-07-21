# 🛍️ ShopSmart - E-Commerce Visitor Purchase Intention Predictor

An end-to-end Supervised Machine Learning project developed for **ShopSmart**, an e-commerce platform. This project aims to analyze 12,330 unique user sessions over a year to predict which visitors are likely to complete a purchase, enabling efficient marketing spend and lowering lost revenue opportunities.

## 📌 Problem Statement
ShopSmart receives thousands of daily users, but converting traffic into sales is challenging. To target the right audience, the system models continuous browsing behavior to identify purchasing intent before a session ends. 

Since the target dataset is highly **imbalanced** (fewer purchases compared to casual browsing), the system uses a **Pruned Decision Tree Classifier** optimized specifically for an **F1-Score benchmark of 0.55+**.

## 📊 Dataset Highlights
* **Total Sessions:** 12,330 individual user sessions.
* **Feature Types:** Mix of numerical and categorical variables (e.g., product pages visited, exit rates, duration, special days, month).
* **Target Metric:** Imbalanced classification tracking `Revenue` generation (True/False).

## 🛠️ Tech Stack & Key Steps
The assignment pipeline is structured inside a Jupyter Notebook with the following components:
* **Python** & **Jupyter Notebook** - Core analysis environment.
* **Pandas & NumPy** - For handling 12k+ categorical and continuous session rows.
* **Matplotlib & Seaborn** - In-depth **Exploratory Data Analysis (EDA)** tracking user duration and drop-off rates.
* **Scikit-Learn** - Preprocessing, data normalization, **Cost Complexity Pruning (ccp_alpha)**, and modeling.

## 📉 Machine Learning Workflow
1. **EDA:** Checked feature distributions, bounding outliers, and mapping session duration vs purchase conversions.
2. **Feature Preprocessing:** Encoded categorical features and applied scaling transformations to highly skewed numerical features.
3. **Imbalance Handling:** Evaluated structural metrics keeping data imbalance constraints in mind.
4. **Model Building & Pruning:** Implemented a **Decision Tree Classifier** and used pre-pruning (`max_depth`, `min_samples_leaf`) or post-pruning parameters to avoid overfitting and boost test set stability.
5. **Evaluation:** Tested against the baseline **F1-Score benchmark of 0.55**.

## 💻 Setup and Run Instructions

1. **Clone the repository:**
   ```bash
   git clone <YOUR_GITHUB_REPOSITORY_URL>
   cd <YOUR_REPO_NAME>
   ```

2. **Add ShopSmart dependencies:**
   Make sure your `requirements.txt` contains `scikit-learn`, `pandas`, `numpy`, `matplotlib`, and `seaborn`. Then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the Notebook:**
   ```bash
   jupyter notebook
   ```
   *Open your `.ipynb` notebook file and click **Kernel > Restart & Run All**.*
