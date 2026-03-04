ACNH-Isolation-Behaviour-Prediction
=====================

## Overview:
This project investigates how social isolation during the COVID-19 pandemic influenced in-game behaviours in *Animal Crossing: New Horizons (ACNH)*. Using a multinational dataset of player activity and psychological indicators, the study combines exploratory data analysis, feature engineering, and machine learning to identify behavioural patterns associated with different durations of self-isolation.

The project applies data mining techniques and supervised machine learning to predict isolation duration based on player actions within the game. By analysing behavioural variables and engagement trends, the research highlights how video games functioned as a coping mechanism and social interaction platform during extended periods of social distancing.

The analysis demonstrates that specific in-game activities strongly correlate with the duration of isolation, and that machine learning models can effectively classify isolation lengths based on behavioural patterns.

## Project Report

Full project report available here:

[Project Report – Predicting Social Isolation Duration from Animal Crossing Gameplay Behaviour](report.pdf)

The report presents the full methodology, experimental analysis, and predictive modelling approach used to analyse the relationship between pandemic isolation and gaming behaviour.

## Key Features:
- Behavioural Data Analysis: Exploration of player gaming behaviour during COVID-19 isolation periods using visual analytics.
- Feature Engineering: Extraction of behavioural variables representing player actions within the game environment.
- Machine Learning Classification: Implementation of a CatBoostClassifier to predict isolation duration from behavioural data.
- Class Imbalance Handling: Application of SMOTE to balance minority classes and improve model generalisation.
- Hyperparameter Optimisation: Automated tuning using Optuna to maximise model performance.
- Behavioural Trend Visualisation: Use of charts and heatmaps to analyse relationships between isolation duration and gameplay patterns.

## Tasks Breakdown

### 1. Exploratory Data Analysis
Initial analysis explored how isolation length varied across regions and gaming habits. Visualisations such as bar charts and heatmaps were used to identify patterns in self-reported isolation durations and player activity.

The analysis revealed that most participants reported isolating for more than a month, highlighting the prolonged impact of pandemic restrictions. :contentReference[oaicite:0]{index=0}

### 2. Feature Selection
Behavioural variables representing in-game actions (E1–E28) were extracted from the dataset. These features capture player behaviours such as exploration, item collection, and social interactions.

Feature importance analysis identified key activities such as bug collection, resource management, and social interactions as strong predictors of isolation duration.

### 3. Handling Class Imbalance
The dataset exhibited imbalance across isolation categories. To address this, the **Synthetic Minority Oversampling Technique (SMOTE)** was applied to generate synthetic samples for underrepresented classes, allowing the model to learn meaningful patterns across all categories.

### 4. Model Development
A **CatBoostClassifier** was selected due to its ability to handle imbalanced datasets and provide built-in feature importance evaluation.

The dataset was split into:
- Training set (60%)
- Validation set (20%)
- Test set (20%)

Stratified sampling ensured balanced representation across isolation categories.

### 5. Hyperparameter Optimisation
Model parameters were optimised using **Optuna**, applying Tree-Structured Parzen Estimators (TPE) and 5-fold stratified cross-validation to evaluate performance across multiple configurations.

Key parameters optimised included:
- Iterations
- Tree depth
- Learning rate
- L2 regularisation
- Bagging temperature

### 6. Model Evaluation
The final model achieved strong predictive performance:

- Validation Accuracy: 97%
- Test Accuracy: 94%

These results demonstrate that player behavioural patterns can be used to reliably predict the duration of social isolation.

### 7. Behavioural Insights
The analysis showed that players experiencing longer isolation periods tended to shift from casual gameplay toward more strategic and immersive activities.

Examples include:
- Resource planning and exploration
- Collecting in-game items
- Maintaining social interaction through in-game gifting systems

These behaviours indicate that gaming served both as a coping mechanism and as a way to maintain social engagement during pandemic restrictions.

## Technologies Used:
- Python
- CatBoost
- Optuna
- SMOTE (Imbalanced Learning)
- Pandas
- NumPy
- Matplotlib / Seaborn
- Machine Learning
- Data Mining Techniques

## Contributors:
- **Sandra Guran**
- **Ayesha Rahman**
- **Natalie Leung**

## Academic Context
This project was completed as part of a university data mining coursework analysing behavioural datasets to explore real-world impacts of the COVID-19 pandemic on digital interaction and gaming behaviour.

## Disclaimer
This repository was created for academic research purposes. The models and findings are intended for educational and analytical use only.
