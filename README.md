# breast-cancer-prediction-csv-file

This code focuses on comparing three machine learning models — Logistic Regression, Decision Tree, and K-Nearest Neighbors (KNN) — on a breast cancer dataset. Here’s how it works:

1. **Importing Libraries**: Essential libraries like pandas for data manipulation, scikit-learn for machine learning models and evaluation metrics, and seaborn for visualization are imported. This ensures the necessary tools for building and evaluating the models are available.

2. **Data Preprocessing**: The breast cancer dataset is loaded, and the 'id' column is dropped since it doesn’t contribute to prediction. The 'diagnosis' column, which contains categorical values ('M' for malignant and 'B' for benign), is encoded as binary (1 for malignant, 0 for benign).

3. **Feature and Target Separation**: The dataset is split into features (X) and the target label (y). The features consist of all columns except for the 'diagnosis' column, while the target (y) is the diagnosis column.

4. **Data Splitting and Scaling**: The data is divided into training and testing sets (80% train, 20% test) using `train_test_split`. A `StandardScaler` is applied to normalize the data, ensuring that all features contribute equally to the model.

5. **Evaluation Function**: A function `train_evaluate_model` is defined, which takes a machine learning model, trains it on the training data, makes predictions on the test data, and evaluates the model using several metrics: accuracy, F1-score, precision, recall, and balanced accuracy. The results are stored in a DataFrame for comparison.

6. **Logistic Regression Model**: A logistic regression model is created and trained. The model’s performance is evaluated using the evaluation function, and the results are saved. A visual table with color gradients is generated to highlight the performance based on F1-score.

7. **Decision Tree Model**: A decision tree classifier is trained in the same manner, and its results are compared to the logistic regression results. The DataFrame is updated to include this new model's metrics.

8. **K-Nearest Neighbors (KNN) Model**: A KNN model is trained with 12 neighbors, evaluated, and its results are appended to the previous models' results. The final table is again sorted by F1-score and visualized.
