# Item–Item Collaborative Filtering Recommender System
A complete implementation and evaluation of an item–item collaborative filtering movie recommender system using the Pearson correlation coefficient as the similarity measure.
The project uses the MovieLens 100k Dataset and evaluates four different rating-prediction functions across multiple experiments.

# 🎯 Project Goal

The objective of this project is to:

- Implement an item–item collaborative filtering recommender system
- Use Pearson similarity to select the top-N nearest neighbors
- Implement four different prediction functions based on weighted averages
- Evaluate the system using standard recommendation metrics
- Compare performance across multiple experimental setups

# 🧮 Prediction Functions

Given a user **u**, a target movie **i**, and a number of neighbors **N**, the system retrieves the **N most similar items** (based on Pearson similarity) that **user u has already rated**.

Four prediction functions are implemented:

### 1. Weighted Average

A classic weighted mean where weights = Pearson similarity.

### 2. Weighted Average with Bias Adjustment

- Implements the approach described in lecture 11, slide 53:
- Adjusts each neighbor rating by removing the neighbor user's average rating
- Adjusts final prediction by reinserting the target user's mean

### 3. Weighted Average with Weight Based on Common Users

- Weights are a function of the number of users who have rated both items:
- More common users → larger weight
- The weight function is user-defined and documented in the report

### 4. Weighted Average with Weight Based on Item Rating Variance

- Weights depend on each neighbor item's rating variance:
- Higher variance → higher weight
- The weight function is user-defined and documented in the report

## 🧪 Experimental Setup
### Train–Test Split

The dataset is randomly divided into:

**- 80% Training set
- 20% Testing set**

### Evaluation Metrics

For every experiment, the following are computed:
**1. Mean Absolute Error (MAE)
2. Macro-Averaged Precision
3. Macro-Averaged Recall
4. Confusion Matrix**

💡 A movie is considered **relevant** if the rating ≥ 3.

# Requirements
1. Python 3 installed <br />
2. Numpy installation with pip --> pip install numpy
# Teminal Screenshot
![ΣτιγμιότυποΕκτέλεσηςΚώδικα](https://github.com/Permalized/Python-Recommender-System/assets/85862074/8c0fdc12-d130-4363-8fcc-8bf489e5aaaa)

