# walmart_inventory_model

# Step 1: Data Collection

For this assignment, I chose to create a synthetic dataset of 300 records that reflect Walmart's weekly product demand and inventory levels. The features in my dataset are:
•	Product ID
•	Product Category
•	Store Location
•	Week Number
•	Units in Stock
•	Units Sold
•	Promotion (Yes/No)
•	Weather Index (numeric)
•	Forecasted Demand (Target Variable)
This dataset is modeled on real retail inventory patterns, taking inspiration from Walmart's business, and is designed to utilize historical and contextual data to predict future demand.

# Step 2: Data Preprocessing
I cleaned the dataset by:
•	Removing duplicates
•	Filling missing values using mean and mode (for numerical and categorical data respectively)
•	Normalizing numerical features like “Units in Stock” and “Weather Index”
•	Converting categorical variables (like Product Category and Promotion) to numerical format using one-hot encoding
•	Splitting the data into 80% training set and 20% testing set



# Step 3: Model Selection and Model Training 
Since I am trying to predict product demand, I went with a regression model. Specifically, I used Linear Regression, since it's simple, interpretable, and suitable for continuous target prediction (i.e., units expected to be sold). I used scikit-learn to build the Linear Regression model. I trained the model using the training set. The model learned correlations between variables like promotions, stocks, and weather and how they impact the demand for goods.

# Step 4: Model Evaluation
To evaluate the model, I used:
•	Mean Absolute Error (MAE)
•	Root Mean Squared Error (RMSE)
•	R² Score
The first output showed an R² of 0.78, which meant that the model explained 78% of the variance in demand. The error metrics were in a satisfactory range, which meant that the model generalized very well.

# Step 5: Model Optimization
I improved the model performance by:
•	Removing highly correlated features to reduce multicollinearity
•	Tuning the model by switching to Ridge Regression (a regularized form of linear regression)
•	Using GridSearchCV to find the best hyperparameters (alpha value)
This optimization increased the R² score to 0.83 and slightly reduced the error metrics.

# Model Testing
Once optimized, I tested the model again on the test data. The performance was consistent with minimal overfitting. The final model can now predict product demand for upcoming weeks, which can help Walmart plan inventory better and reduce waste or shortages.
![image](https://github.com/user-attachments/assets/731e9366-3763-4d91-beca-1061e825fc89)
