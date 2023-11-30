# Project Report: Online Shopping Intention Analysis

## Problem Statement
E-commerce platforms face the challenge of accurately predicting user purchasing intent. Understanding the factors influencing whether a visitor will make a purchase or not is crucial for targeted marketing. This project aims to analyze user interactions on an online shopping platform and build a predictive model to identify potential buyers.

## Goal
Develop a predictive model to effectively classify online shopping sessions into two categories: those resulting in a purchase and those that do not. By leveraging machine learning techniques and insights gained from exploratory data analysis (EDA), the objective is to enhance the platform's understanding of user behavior and contribute to targeted marketing strategies.

## Dataset
The dataset encompasses various features, including administrative and informational page engagements, product-related interactions, duration metrics, and user-specific attributes. The target variable is 'Revenue,' indicating whether a user completed a purchase during the session.

## EDA & Visualizations
### Key Insights:
- **Monthly Visitor Trends:** May, November, and March exhibit high visitor traffic, suggesting potential seasonal patterns that can guide marketing strategies.
- **Visitor Type Distribution:** Returning visitors dominate, especially on weekdays, highlighting the importance of customer retention strategies.
- **Imbalanced Data:** 'False' is the predominant entry for the 'Revenue' variable, indicating an imbalance that needs addressing for effective model training.
- **Seasonal Trends:** Increased purchases in May and November suggest strategic opportunities for targeted marketing.

### Visualizations (Refer to images in the repository):
1. **Monthly Visitor Trends:** Highlighting the influx of visitors during specific months.
2. **Visitor Type Distribution:** Comparing the frequency of returning and new visitors.
3. **Page Engagement vs. Purchase:** Illustrating the correlation between page-related engagement and the likelihood of a purchase.
4. **Weekend vs. Weekday Purchase Behavior:** Analyzing how purchase behavior varies between weekends and weekdays.

### Feature Selection
Recursive Feature Elimination (RFE) identified relevant features, reducing dimensionality and improving model interpretability.

### Handling Imbalanced Data
Synthetic Minority Over-sampling Technique (SMOTE) addressed imbalanced data, creating synthetic samples to balance class distribution.

## Models Used
Two models were explored: Support Vector Machine (SVM) and Logistic Regression.

### SVM Model:
- Initial performance decline after balancing imbalanced data.
- Hyperparameter tuning using GridSearchCV, optimizing for the f1-score.
- Improved performance with an average test accuracy of 85%, precision of 85%, recall of 100%, and an f1-score of 92%.

### Logistic Regression Model:
- Superior overall prediction performance compared to SVM.
- Higher precision and recall rates, with an f1-score of 94% for buyers.

## Final Outcome
Logistic Regression, optimized through hyperparameter tuning, demonstrated proficiency in predicting potential buyers. With an accuracy of 89%, improved recall, and an enhanced f1-score, the model achieved a balanced trade-off between precision and recall.

### Key Findings:
1. **Impact of Bounce Rates on Revenue:**
   Pages with lower bounce rates strongly indicate revenue generation. A reduction in bounce rates by up to 0.04 increased the odds of a customer making a purchase by 55%.

2. **Significance of Page Value:**
   Higher Page Value is a robust indicator of revenue generation. Approximately 43% of all visits resulted in revenue for pages with a Page Value score greater than 0.

3. **Optimal Traffic Periods:**
   November displayed the most favorable traffic ratios, with odds of a purchase increasing by 275% compared to previous months. December, with substantial traffic, presents an opportunity for targeted efforts to maximize revenue generation.

## Further Improvement Suggestions
1. **Complex Feature Engineering:**
   Explore more sophisticated feature engineering techniques for enhanced model generalization.

2. **Non-linear Classifiers:**
   Consider implementing non-linear classifiers to capture more complex relationships within the data.

3. **Increased Granularity:**
   Collect data at a more granular level, such as weekly, for a more detailed understanding of patterns.

4. **Expanded Data Collection:**
   Increase the volume of samples to further enrich the dataset.

5. **Diversified Feature Set:**
   Acquire additional dimensions and features, such as page-level information, for a more comprehensive analysis.

This project provides valuable insights into online shopping behavior, emphasizing actionable findings for marketing strategies and laying the foundation for future enhancements to the predictive model.
