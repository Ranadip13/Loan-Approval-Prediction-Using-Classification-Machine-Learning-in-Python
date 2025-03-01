# Loan Approval Prediction Using Classification Machine Learning in Python
The objective of this project is to predict whether a loan would be a risk to the bank or not. When a customer applies for a loan, bank executives must decide whether to approve or reject the application. This decision is based on verifying the customer's background, analyzing the provided information, and identifying whether the customer will repay the loan or default. Since banks process many loan applications every day, a predictive model can help executives make quicker and better decisions.

In this project, a step-by-step approach to creating a Machine Learning predictive model for such scenarios was discussed. This flow can be used as a template to solve any supervised classification ML problem.
The flow of the case study is as below:
- Reading the data in python
- Defining the problem statement
- Identifying the Target variable
- Looking at the distribution of Target variable
- Basic Data exploration
- Visual Exploratory Data Analysis for data distribution (Histogram and Barcharts)
- Feature Selection based on data distribution
- Outlier treatment
- Missing Values treatment
- Visual correlation analysis
- Statistical correlation analysis (Feature Selection)
- Selecting final predictors for ML
- Converting data to numeric for ML
- Splitting the data into Training and Testing sample
- Standardization / Normalization of data (if required)
- Sampling and K-fold cross validation
- Trying multiple classification algorithms
- Selecting the best Model
- Deploying the best model in production

#### Data description: The business meaning of each column in the data is as below
- Loan_ID: Unique identifier for each loan application
- Gender: Applicant's gender (Male/Female)
- Married: Applicant's marital status (Yes/No)
- Dependents: Number of dependents the applicant has
- Education: Education level of the applicant (Graduate/Not Graduate)
- Self_Employed: Whether the applicant is self-employed (Yes/No)
- ApplicantIncome: Applicant's monthly income
- CoapplicantIncome: Income of the co-applicant (if any)
- LoanAmount: Loan amount requested by the applicant
- Loan_Amount_Term: Duration of the loan in months
- Credit_History: Whether the applicant has a credit history (1: Yes, 0: No)
- Property_Area: The area where the property is located (Urban/Semi-Urban/Rural)
- Loan_Status: Whether the loan was approved or not (Y/N)

Following the above steps, various classification machine learning algorithms were tried, including Logistic Regression, Decision Trees, Random Forest, AdaBoost, KNN, Support Vector Machines (SVM), and Naive Bayes, and their average accuracies were calculated. In this case, multiple algorithms produced similar average accuracy. Therefore, any one of them could be chosen. Adaboost is chosen as the final model due to its speed and effective use of predictors, as observed in its variable importance chart. It ensures that no single predictor dominates the decision, which is beneficial.

To deploy the model, the following steps are followed:
1.	Train the model using 100% of the available data.
2.	Save the model as a serialized file for storage and future use.
3.	Develop a Python function that integrates with front-end applications to take inputs and return predictions.
