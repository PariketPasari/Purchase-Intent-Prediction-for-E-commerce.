# Project Report: Online Shopping Intention Analysis

## Problem Statement
E-commerce platforms face the challenge of accurately predicting user purchasing intent. Understanding the factors influencing whether a visitor will make a purchase or not is crucial for targeted marketing. This project aims to analyze user interactions on an online shopping platform and build a predictive model to identify potential buyers.

## Goal
Develop a predictive model to effectively classify online shopping sessions into two categories: those resulting in a purchase and those that do not. By leveraging machine learning techniques and insights gained from exploratory data analysis (EDA), the objective is to enhance the platform's understanding of user behavior and contribute to targeted marketing strategies.

## Dataset
The dataset encompasses various features, including administrative and informational page engagements, product-related interactions, duration metrics, and user-specific attributes. The target variable is 'Revenue,' indicating whether a user completed a purchase during the session.

## EDA & Visualizations

### Key Insights:
- **Page Interaction Analysis:** Product-Related Pages: A substantial correlation exists between engagement on Product-Related pages (both views and duration) and the likelihood of a purchase. Visitors spending more time on these pages demonstrate a higher probability of making a purchase.
Engagement Metrics Analysis
- **Bounce and Exit Rates:** Sessions with lower bounce and exit rates are more likely to result in purchases. Elevated exit and bounce rates signify lower user engagement and a reduced likelihood of sales.
- **Influence of PageValues:** Higher PageValues strongly correlate with a greater likelihood of transactions, underscoring the importance of this metric in assessing user purchase intent.
- **Visitor Type Analysis:** New Visitor Type: Returning Visitors are more frequent but exhibit a lower likelihood to make a purchase compared to New Visitors. This highlights the significance of strategies targeting both visitor retention and conversion.
- **Effective Traffic Sources:** traffic Type 5: This traffic source stands out as the most significant contributor to sessions leading to purchases.
Trend Analysis over Time
- **Seasonal Trends:** There is a noticeable surge in purchases during May and November. The data suggests that these months are critical periods for implementing targeted marketing and sales initiatives.
  
### Visualizations Findings:
- Significant visitor traffic is observed in May, November, and March, warranting further analysis
-  Most visitors are returning visitors who visit the site multiple times.
- Most visitors are of the Returning Visitor type.
- Weekday traffic is higher than weekend traffic, prompting further analysis.
- Revenue data is highly imbalanced, with 'false' as the most occurring entry.
- Plots show increased new visitors in May, November, and December, with a surge in overall traffic during November, May, March, and December.
- Returning Visitors have more sessions, but the percentage of buyers among them is lower compared to non-buyers. New Visitors show a similar purchase rate to non-buyers, suggesting higher engagement.
- Sessions resulting in purchases have higher average views on Product-Related pages, indicating the significance of engagement in driving purchases.
- Average time spent on Product-Related pages is higher for buyers, supporting the trend observed in page view counts.
- Although total Buyer sessions are lower on weekends, the percentage of purchases is higher, suggesting higher purchase completion rates on weekends.

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
During this predictive modeling phase, we employed Logistic Regression to forecast potential Buyers within the Online Retail Dataset. The initial model displayed proficiency in recognizing Non-Buyers, but encountered difficulties accurately classifying the True class (Buyers) due to class imbalance. Through subsequent hyperparameter tuning using GridSearchCV, we improved the model, achieving a better balance between precision and recall. Optimized for the f1-score, the tuned model demonstrated an accuracy of 89% on the test set, with notable enhancements in recall and f1-score. These improvements indicate an enhanced ability to distinguish potential Buyers from Non-Buyers, as evidenced by the following metrics:

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
