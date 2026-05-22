# 🎮 Mobile Game In-App Purchases Analysis

An end-to-end **data mining and analytics project** focused on understanding user spending behavior in a mobile game using exploratory data analysis, clustering, and genetic algorithm-based feature selection.

---

## 📌 Project Overview

This project analyzes in-app purchase data from a mobile game to:

* Understand user spending behavior
* Identify patterns across demographics, countries, and payment methods
* Segment players into meaningful behavioral clusters
* Optimize monetization strategy using data-driven insights

The dataset includes user-level features such as:

* Age
* Session count
* Session duration
* Country
* Game genre
* Payment method
* In-app purchase amount

---

## 🧰 Tools & Libraries

* Python
* Pandas, NumPy
* Matplotlib, Seaborn, Plotly
* Scikit-learn
* Scikit-learn-extra (K-Medoids)
* SciPy (Hierarchical clustering)
* Genetic Algorithms (custom implementation)

---

## 📊 Exploratory Data Analysis (EDA)

Key insights from the analysis:

### 💰 Spending Distribution

* In-app purchase amounts are highly **right-skewed**
* A small group of users (“whales”) generates most of the revenue

### 🌍 Country Insights

* Significant variation in spending across countries
* Some regions show consistently higher monetization potential

### 🎮 Game Genre Analysis

* Certain genres produce higher average spending behavior
* Suggests genre strongly influences monetization success

### 💳 Payment Methods

* Different payment methods show different average spending levels
* Optimization of payment options can improve revenue flow

### 📈 Correlation Insights

* Strong positive correlation between **SpendingSegment** and **InAppPurchaseAmount**
* Negative correlation between **Age** and spending → younger users tend to spend less

---

## 🧠 Clustering & User Segmentation

Hierarchical clustering was used to segment users into behavioral groups.

### 🔵 Cluster 0: Free-to-Play Users (Majority)

* Low or near-zero spending
* Stable engagement (session count & duration)
* Represent the bulk of the player base

**Business Strategy:**

* Ad-based monetization (rewarded ads)
* Low-cost starter packs
* Conversion-focused promotions

---

### 🟡 Cluster 1: High-Value Users (Whales)

* Very high in-app purchases
* Higher session frequency
* Shorter session duration (quick purchase behavior)

**Business Strategy:**

* VIP rewards and loyalty programs
* Exclusive content and cosmetics
* Dedicated customer support
* Avoid intrusive ads

---

## 🧬 Genetic Algorithm (Feature Selection)

A custom **Genetic Algorithm (GA)** was implemented to optimize feature selection for clustering.

### ⚙️ How it works:

* Each chromosome represents a subset of features
* Fitness is calculated using:

  * K-Medoids clustering
  * Silhouette score
  * Feature penalty to reduce complexity

### 🔁 GA Process:

1. Initialize random population
2. Evaluate fitness using clustering quality
3. Select best individuals (tournament selection)
4. Apply crossover and mutation
5. Repeat for multiple generations

### 🎯 Outcome:

* Selected most informative features
* Improved clustering quality and separation

---

## 🤖 Fuzzy + Clustering Hybrid System

A hybrid decision system was implemented:

1. Input user data is scaled
2. Genetic algorithm selects optimal features
3. K-Medoids assigns cluster type
4. Fuzzy logic system estimates:

   * Player monetization score

This enables more flexible and interpretable user profiling.

---

## 📉 Key Business Insights

* Revenue follows a **Pareto distribution (80/20 rule)**
* A small % of users contribute most revenue
* User segmentation is essential for monetization strategy
* Behavioral patterns vary strongly across demographics

---

## 🚀 Conclusion

This project demonstrates how **data mining techniques can be applied to mobile game analytics** to improve monetization strategies.

By combining:

* EDA
* Clustering
* Genetic Algorithms
* Fuzzy logic

We can better understand player behavior and design targeted business strategies for different user groups.
