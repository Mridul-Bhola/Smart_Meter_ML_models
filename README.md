# Smart_Meter_ML_models
We collected data from smart meters installed in homes throughout Bareilly City and applied various machine-learning models to analyze them.

The high-frequency three-minute interval smart meter dataset provides information on urban household electricity consumption patterns from nearly 100 smart meters installed in Mathura and Bareilly districts of Uttar Pradesh, India from May 2019 to October 2021. The data also provides information on the power supply situation (including hours of power supply, voltage, current withdrawn, and other related variables). The data can have various use cases for researchers and practitioners in the power sector domain. For instance, power distribution companies (discoms) can utilize the smart meter data for effective service delivery and demand management

1.) Linear Regression

 First, we meticulously organized the dataset, ensuring that all relevant features were included 
 and properly formatted. We then assigned the features (independent variables) to the 'X'
 variable and the target variable (electricity consumption) to the 'y' variable. Following this, 
 we applied linear regression to the prepared data to model and predict electricity consumption 
 values.

Results:-
Mean Squared Error: 1.6734258269109627e-05

2.) Ridge Regression

After organizing the dataset and assigning the relevant features to the X variable and the target variable (electricity consumption) to the y variable, we initially used linear regression to predict electricity consumption values. However, to enhance the robustness and accuracy of our predictions, we subsequently employed Ridge regression on this dataset. Ridge regression, a form of regularized linear regression, helps in addressing multicollinearity among the predictor variables by imposing a penalty on the size of the coefficients. This penalty term, also known as the L2 regularization term, helps prevent overfitting by shrinking the coefficients and thus improving the model's generalizability to new, unseen data.

Results:-
Mean Squared Error: 1.67342582381245e-05

3.)Lasso Regression

 Following the application of Ridge regression, we further refined our predictive model by 
 employing Lasso regression on the dataset. Lasso regression, which stands for Least Absolute 
 Shrinkage and Selection Operator, adds an L1 regularization term to the linear regression model. 
 This technique not only helps prevent overfitting by shrinking the coefficients but also 
 performs feature selection by driving some coefficients to zero. As a result, Lasso regression 
 enhances model interpretability by identifying and retaining only the most significant features 
 that contribute to predicting electricity consumption, thereby improving the model's performance 
 and robustness.

 Results:-
 Mean Squared Error: 0.0005850677736469955

4.)Support Vector Regression (SVR) 

 After employing Lasso regression, we further experimented with Support Vector Regression (SVR)
 to enhance the predictive accuracy of our model. SVR, an extension of Support Vector Machines
 (SVM) for regression tasks, is particularly effective in handling non-linear relationships by 
 utilizing  kernel functions. By mapping the input features into higher-dimensional space, SVR
 aims to find the optimal hyperplane that minimizes the prediction error within a specified
 margin. This method is beneficial for capturing complex patterns in the electricity consumption 
 data, providing robust predictions and potentially improving the model's performance compared to 
 linear regression techniques.

  Results:-
  Mean Squared Error: 0.0020554292761559424

5.) Random Forest Regression

 After applying Support Vector Regression (SVR), we turned to the Random Forest model to further 
 enhance our predictions. Random Forest, an ensemble learning method, is well-suited for 
 capturing complex interactions between variables by constructing multiple decision trees and 
 aggregating their results. However, due to the large size of our electricity consumption 
 dataset, the computational demands exceeded the capabilities of our CPU. Processing such a vast 
 amount of data with Random Forest on a CPU resulted in significantly prolonged training times 
 and performance bottlenecks, highlighting the need for more powerful computational resources, 
 such as a GPU or distributed computing environment, to effectively handle large-scale datasets.

 To effectively run a dataset after cleaning the data for machine learning tasks, several 
 theoretical considerations and steps need to be followed. Here’s a comprehensive guide:

1.) Handling Missing Data:

  1. Detection: Identify missing values in the dataset using methods like .isnull() or .isna() in 
     Python.
   
  2. Strategies: Decide on how to handle missing data, such as imputation (replacing missing 
     values with statistical measures like mean, median, or mode) or deletion (removing rows or 
     columns with missing data if appropriate).
     
2.) Dealing with Outliers:

  1. Detection: Detect outliers using statistical methods (e.g., Z-score, IQR) or visualization 
     techniques (e.g., box plots, scatter plots).
    
  2. Treatment: Decide whether to remove outliers, transform them, or keep them based on domain 
     knowledge and impact on the analysis.
    
3.) Removing Duplicates:

  1. Identification: Identify and remove duplicate records from the dataset to avoid bias and 
     redundancy.
    
  2. Methods: Use functions like .duplicated() followed by .drop_duplicates() in pandas to 
     eliminate duplicate rows.
     
4.) Standardization and Normalization:

  1. Standardization: Scale numerical features to have a mean of 0 and a standard deviation of 1 
    (Z-score normalization) to handle variables with different scales.
  
  2. Normalization: Transform numerical data to a common range, typically [0, 1] (Min-Max 
     normalization), to ensure consistency across features.
  
5.) Handling Inconsistent Data:
 
  1. Format Standardization: Ensure consistent data formats across columns, such as date formats 
     or categorical variables.
     
  2. Correction: Correct errors in data entry or formatting to maintain data integrity.
     
6.) Feature Engineering:
 
  1. Creating New Features: Derive new features from existing ones to capture additional insights 
     or improve model performance.
     
  2. Feature Selection: Choose relevant features that contribute most to the target variable, 
     using techniques like correlation analysis or feature importance methods.
 
 
 
