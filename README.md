# Project Report: Electrical Grid Stability Analysis

## Project Overview
In this project, we aim to analyze and predict the stability of an electrical grid under Distributed Smart Grid Control (DSGC) using a simulated dataset. The dataset simulates a 4-node architecture, including one electricity producer and three consumers, with 10,000 instances and 12 attributes.

## Dataset Description
The dataset comprises various features related to power production/consumption, adaptation willingness, and adaptation time.

### Attributes
- `p[x]`: Power produced or consumed by each node (`p1` to `p4`).
- `g[x]`: Adaptation willingness of each node (`g1` to `g4`).
- `tau[x]`: Time for each node to adapt their production/consumption (`tau1` to `tau4`).

### Target Variables
- `stab`: Numerical value indicating grid stability (positive value indicates instability).
- `stabf`: Categorical version of `stab`, representing the stability status.

## Data Preprocessing
- **Target Variable Selection**: We focused on `[Your choice of target variable]` for [reasons].
- **Feature Engineering**: [Describe any new features you created].
- **Data Cleaning**: [Details about data cleaning steps].

## Exploratory Data Analysis (EDA)
- **Feature Distributions**: [Summary of feature distributions].
- **Correlation Analysis**: [Key findings from correlation analysis].
- **Insights**: [Any interesting insights from EDA].

## Model Development
- **Model Selection**: We experimented with [list of models] and chose [best performing model] based on [criteria].
- **Feature Scaling**: Implemented [type of scaling] to standardize the feature set.
- **Train-Test Split**: Data was split into training and testing sets.

## Model Evaluation
- **Classification Approach**: [Details on metrics like accuracy, precision, recall, F1-score, and ROC-AUC, if applicable].
- **Regression Approach**: [Details on metrics like MSE, RMSE, and MAE, if applicable].
- **Cross-Validation**: [Results and insights from cross-validation].

## Results and Interpretation
- **Model Performance**: [Discuss the performance of your model].
- **Feature Importance**: [Discuss which features were most important in predicting grid stability].
- **Practical Implications**: [Discuss how the findings can be applied in a real-world scenario].

## Conclusions and Recommendations
In summary, our exploration of various machine learning models on a given dataset revealed the following key findings:

Linear Regression Models:

Implementation: Utilized closed-form solution, gradient descent, and stochastic gradient descent. Performance Metrics: Consistently demonstrated the ability to handle the data with full rank characteristics. Results: All three models performed similarly with a Sum of Squared Errors (SSE) around 1.47 and an R2 score of 0.63. Cross-validation: The k-fold cross-validation results reinforced the reliability of the closed-form solution, providing consistent and satisfactory performance metrics, including SSE, Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R2 score.

Neural Network Model:

Predictive Capabilities: Exhibited strong predictive capabilities. Optimal Cutoff: Achieved an optimal cutoff at 0.6. Classification Performance: Yielded an accuracy of 92.05%, sensitivity of 92.08%, and AUC-ROC score of 0.98. Balance: Demonstrated a well-balanced classification performance, capturing a substantial portion of positive instances while maintaining high overall accuracy.

Logistic Regression:

Performance: Provided competitive results. Metrics: Achieved an accuracy of 91.2%, precision of 81.22%, and recall of 96.18%. Best Cutoff: Identified the best cutoff value as 0.4. Additional Consideration: Logistic regression is computationally less expensive than neural networks, especially for small to moderately sized datasets. However, considering the dataset size and model complexity, the computational cost of neural networks may become more justifiable, particularly when leveraging hardware acceleration.

**Conclusion and Recommendation:**

While linear regression models performed adequately, logistic regression and neural networks exhibited superior predictive capabilities. Considering the trade-off between computational cost and performance, logistic regression is recommended as the final model, especially for scenarios with constraints on time complexity and computation cost.
