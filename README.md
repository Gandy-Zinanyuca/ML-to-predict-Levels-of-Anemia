# ML-to-predict-Levels-of-Anemia

1. Overview

This project applies Machine Learning techniques to predict the levels of anemia (No Anemia, Mild, Moderate, Severe) in individuals using health survey data (e.g., ENDES). The study explores multiple algorithms, compares their performance, and discusses their potential use in clinical decision support systems.

2. Dataset

Source: National Demographic and Health Survey (ENDES).

Target variable: Levels of Anemia

0: No anemia

1: Mild anemia

2: Moderate anemia

3: Severe anemia (if included)

3. Features:

Clinical: iron consumption.

Demographic: socioeconomic indicators.

Geographic: rural/urban.

4. Methodology

- Data Preprocessing
- Missing values handled using KNN Imputer.
- Class imbalance mitigated with SMOTE oversampling.
- Features scaled using StandardScaler.

5. Models Evaluated

- Logistic Regression
- Random Forest
- Neural Network (Keras Sequential)
- Hyperparameter tuning with Optuna

6. Evaluation Metrics

- Accuracy, Recall, Precision, F1-score
- Confusion Matrix

7. Results

- Logistic Regression: simple yet effective baseline.
- Random Forest: best overall performance, with balanced recall across classes.
- Neural Network: captured complex patterns but was more sensitive to data quality.

Confusion matrix revealed misclassifications between moderate and severe anemia, highlighting the need for richer data.

8. Key Findings

- Simple models (Logistic Regression, Random Forest) often outperform more complex ones when data is imbalanced or noisy.
- Random Forest provided the best balance between accuracy and interpretability.
- Neural Networks require larger, cleaner datasets to fully leverage their potential.

9. Future Work
Enrich dataset with:
Clinical/nutritional features (iron intake, medical history).
Geographic/contextual variables (altitude, rurality, healthcare access).
Explore advanced algorithms: XGBoost, LightGBM, CNNs (for images/maps).
Integrate spatial and temporal analysis (previous ENDES waves).
Build decision support prototypes for public health programs (MINSA).
Improve model interpretability with tools like SHAP or LIME.
