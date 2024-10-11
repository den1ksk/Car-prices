#### English Version | [Kaggle competition](https://www.kaggle.com/competitions/playground-series-s4e9)

# Used Car Prices Prediction

### Competition Description

The goal of this competition is to predict the price of used cars based on various attributes, such as brand, model, mileage, and year of manufacture. The dataset includes information on over 188,000 cars, with attributes covering engine specifications, fuel type, transmission type, and more. This project aims to develop a model that can accurately predict car prices using machine learning techniques.

### Goal

The goal is to predict the price of used cars. For each `id` in the test set, the target variable to predict is `price`.

### Approach

This project follows a structured approach to predict car prices using machine learning models. The key steps involved were:

1. **Data Exploration:**
   - The training and testing datasets were examined to understand the characteristics of the cars and their distributions.
   - Key features such as mileage, year of manufacture, and engine specifications were visualized to identify their relationship with the car prices.

2. **Feature Engineering:**
   - New features were created, including grouping cars by brand type (premium, budget, or medium), mileage groups, and categorizing transmission and engine specifications.
   - One-Hot Encoding and Frequency Encoding were applied to categorical variables, and continuous features were scaled using StandardScaler.

3. **Data Preprocessing:**
   - Missing values were handled using appropriate strategies, including mode imputation for categorical features and filling missing data for the 'accident' and 'clean_title' columns.
   - New feature columns such as `care_age` (age of the car) and `color_category` (categorization of car colors) were added.

4. **Model Selection and Training:**
   - LightGBM (LGBMRegressor) was selected for its speed and efficiency on large datasets. The model's hyperparameters were tuned using GridSearchCV.
   - The final model was trained on a split of the dataset (70% training and 30% testing).

5. **Model Evaluation:**
   - The model was evaluated using the Root Mean Squared Error (RMSE) metric.
   - Feature importance was analyzed to understand which features contributed most to the price prediction.

6. **Prediction and Submission:**
   - The trained model was used to predict the price for the test dataset. 
   - Final predictions were saved in the required CSV format for Kaggle submission.

### Results

The developed model achieved an RMSE score of **67201**, placing it within the **top 10%** of the leaderboard.

### Files

- `Car_Prices.ipynb`: Jupyter Notebook containing the complete code and analysis.
- `submission.csv`: File containing the predictions for the test dataset.

### Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- lightgbm

### Acknowledgements

This project was completed as part of a Kaggle competition. Thanks to Kaggle and the competition organizers for providing the dataset and platform.
