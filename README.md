# Insurance-Claim-Prediction
Tried several different approaches for this problem. The following gave the best results.
1. Dataset has 58592 rows and 44 columns
2. Target variable is unbalanced (93% samples belong to class 0)
3. 42 independent variables (15 numerical)
4. Used heatmap to find that features are highly co-related to each other.
5. Used variance inflation factor to get rid of multicollinearity. Features with high VIF score were dropped
6. Used Catboost algorithm. Initial prediction resulted in a f1 score of 0
7. Tuned parameter scale_pos_weight to tackle the problem of majority of samples belonging to class 0.
8. Optimum f1 score at scale_pos_weight=10
