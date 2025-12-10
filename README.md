## 📲 Megaline Plan Recommendation: Predicting the Most Suitable Plan for Subscribers

### Project Overview

This project aims to assist Megaline in enhancing its customer experience by recommending more suitable plans to subscribers currently using legacy options. We analyze the behavior of users who have already transitioned to Megaline's newer plans—Smart and Ultra—and develop a predictive classification model. The primary goal is to achieve a minimum accuracy threshold of 0.75, validated using the provided test dataset.

### Dataset Summary

The dataset consists of 3,214 entries with 5 columns: `calls`, `minutes`, `messages`, `mb_used` (numeric features), and `is_ultra` (target variable: 1 for Ultra, 0 for Smart). No duplicate entries were found. The user distribution shows that 30.65% are Ultra users and 69.35% are Smart users, indicating an imbalanced dataset.

### Model Selection

We evaluated Logistic Regression, Decision Tree, and Random Forest models. The **Random Forest model** with `n_estimators=8` was selected as the best performer, achieving the highest validation accuracy of **0.7925**. This surpasses the project's required accuracy threshold of 0.75. While the Random Forest showed some overfitting on the training data, its strong performance on the validation set makes it the most reliable choice for predicting subscriber plans.
