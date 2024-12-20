# Forest-Cover-Type-Prediction
The Forest Cover Type Prediction project aims to classify areas of forest land into different cover types based on cartographic and ecological data. The dataset includes features such as elevation, aspect, soil type, and hydrology distances, with a target variable Cover_Type representing seven distinct forest cover types. This project is a multiclass classification problem that leverages machine learning techniques to improve prediction accuracy.

## Data Analysis and Preprocessing
 ### Exploratory Data Analysis (EDA)
- Dataset Composition:
  - Rows and Columns: 15,120 rows and 56 columns.
  - Target Variable: Cover_Type includes 7 classes, with no significant class imbalance.
- Key Insights:
  - Elevation has a strong influence on forest cover types, with distinct ranges correlating with specific classes.
  - Soil types exhibit clear patterns associated with certain forest covers, suggesting categorical importance.
  - Features like Horizontal Distance to Hydrology and Vertical Distance to Hydrology displayed linear trends with Cover_Type.
  - Aspect and hillshade variables showed weaker correlations but added nuance to predictive modeling.
### Data Preprocessing
- Scaling: Applied StandardScaler to normalize continuous features, improving model convergence.
- Feature Engineering:
  - Engineered interaction features such as combined distances to hydrology.
  - One-hot encoding applied to categorical variables like Soil_Type to retain interpretability.
- Dimensionality Reduction: PCA was evaluated but not implemented, as feature importance analysis indicated no significant multicollinearity.
- Train-Test Split: The dataset was split into 80% training and 20% testing subsets, ensuring representative sampling.

##  Modeling and Evaluation
### Models Implemented:
1) Random Forest Classifier:
   - Best overall model, achieving high accuracy and generalizability.
   - Low variance across validation folds, highlighting stability.
2) Gradient Boosting:
   - Provided competitive accuracy but showed slight overfitting on the training set.
3) Support Vector Machine (SVM):
   - Effective for smaller data subsets but computationally expensive for the full dataset.
4) Multi-Layer Perceptron (MLP):
   - Balanced performance but required extensive hyperparameter tuning to avoid overfitting.
### Evaluation Metrics:
![download](https://github.com/user-attachments/assets/16d3880a-6669-46ac-845f-bc4887244623)

1) Random Forest Classifier:
   - Accuracy: 89%
   - Precision, Recall, F1-Score: Balanced across all classes, indicating consistent performance.
2) Gradient Boosting:
   - Accuracy: 87%
   - Slight recall reduction for underrepresented classes.

## Feature Importance
### Top Features:
- Elevation: Most predictive feature, closely correlated with forest cover types.
- Soil_Type: Played a critical role, with one-hot encoded categories revealing distinct importance.
- Horizontal and Vertical Distance to Hydrology: Enhanced predictive power when combined as engineered features.
- Wilderness Areas: Added value in segregating forest types across ecological zones.


## Conclusion and Future Work
### Conclusion:
- The Random Forest Classifier emerged as the optimal model for forest cover type prediction, offering a robust combination of accuracy, stability, and interpretability. The project successfully utilized feature engineering and machine learning techniques to achieve an 89% accuracy rate.

### Future Directions:
- Implement ensemble techniques such as stacking or blending to integrate model strengths.
- Explore geospatial data for contextual feature enhancement, including topographic and climatic overlays.
- Investigate deep learning models like Convolutional Neural Networks (CNNs) for automated feature extraction.
- Experiment with dimensionality reduction methods to optimize computational efficiency without sacrificing accuracy.
