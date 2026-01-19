# Predictive Modeling For Electric Vehicles Cost

The transportation industry is evolving rapidly, with electric vehicles (EVs) emerging as a key solution to reduce carbon emissions and address environmental challenges. We chose to focus our analysis on:

   **How do the cost of EVs compare across Models?**
   
# Dataset used: ​
​
  Electric_Vehicle_Population_Data-3.csv (Data.gov)
       ​
# Jupyter Notebook:
​
  EV_Price_Analysis.ipynb
  ​
# Sample Size:
​
  Electric_Vehicle_Population_Data-3.csv
  ​
    - Rows: 216772, Columns: 17
    ​
    -  Rows: 3307, Columns: 13 (After cleaning)
    
# Columns used in efficiency analysis:​

  - Target Variable: Base MSRP(Price)
    ​
  - Predictors: Model year, Make, Model, Electric range, Electric vehicle type
    ​
  - Car ID, Brand, Year, Engine Size, Fuel Type, Transmission, Mileage, Condition, Price​​

# Steps:​

  - Dropped Rows with NaN Values
  ​
  - Dropped any duplicates with the dataset
  ​
  - Dropped any missing data
  ​
  - Dropp irrelevant columns(eg: VIN, DOL Vehicle ID, Vehicle Location.)
  ​
  - Remove rows where 'Base MSRP' is 0​
​​
# Data Types:
​
  **Numerical:** Model Year, Electric Range, Base MSRP, etc
  ​
  **Categorical:** Make, Model, Electric Vehicle Type, etc.
  
# Technologies and Libraries Used

  - Python
  - Jupyter Notebook (.ipynb)
  - Pandas – Data Manipulation
  - NumPy – Numerical Operations
  - Matplotlib & Seaborn – Data Visualization
  - Plotly – Interactive Visualizations
  - Scikit-learn – Machine Learning Models (e.g., Linear Regression, KMeans)

# Key Findings:

  Exploratory Data Analysis (EDA) to understand patterns and relationships in the data
  ​
  - Base MSRP ranges from $31,950 to $845,000, with a median of $59,900.
    ​
  - The majority of prices are concentrated between $30,000 and $80,000.
    ​
  - There are a few outliers with prices exceeding $300,000.
    ​
  - There is a positive trend where vehicles with higher electric ranges tend to have higher base prices.
    ​
  - Clear distinctions between Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) are visible.
    
  - BEVs dominate the dataset, followed by PHEVs.
    ​
  - Most EVs have ranges under 200 miles, with a peak around 100 miles.

# Conclusion:

  - Linear Regression performs very poorly with extremely high MSE, MAE, and a negative R². It’s clearly not a suitable model for this problem.​

  - Random Forest has the best overall performance:​

  - MSE is the lowest, indicating that it has the smallest error.​

  - MAE is also the smallest, showing that the individual predictions are more accurate.​
  
  - R² is the highest, meaning it explains more of the variance in the EV price.​

  - Gradient Boosting has a higher MSE, MAE, and lower R² compared to Random Forest, which suggests it performs worse in this case.​
​​​​​
