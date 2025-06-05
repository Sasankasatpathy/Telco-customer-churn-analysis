 1. Environment Setup (Cells 0–2)
      -Purpose: Install required libraries (pandas, numpy, matplotlib, seaborn, scikit-learn) and mount Google Drive to access the dataset.
      -Summary: Prepares the notebook to read data and perform analysis.

 2. Data Loading & Preview (Cells 3–4)
      -Code: Loads the dataset costumer churn.csv.csv using pandas and displays the first 10 rows.
      -Summary: Confirms the dataset is correctly read into a DataFrame (df) and gives a preview of the data structure.

 3. Data Cleaning (Cells 5–7)
     Tasks:
      -Replaces empty strings in TotalCharges with "0".
      -Converts TotalCharges from object to float.
      -Checks for null values using isnull().sum().sum().
      -Summary: Ensures numerical fields are in the correct format and that the data is clean (no nulls).

 4. Data Inspection (Cells 8–9)
      -Code: Uses df.describe() for statistics and df.duplicated().sum() to check for duplicate rows.
      -Summary: Confirms dataset quality by checking distributions and duplicates.

 5. Data Preprocessing (Cells 10–13)
      -Checked for duplicate customer IDs.
      -Transformed SeniorCitizen from numeric (0/1) to categorical ("yes"/"no") for better readability.
      -Previewed updated dataset.

 6. Churn Distribution Analysis (Cells 14–16)
      -Countplot of Churn shows the number of customers who stayed vs. left.
      -Pie Chart reveals that ~26.54% of customers have churned.

 7. Demographic Analysis (Cells 17–20)
      -Gender vs. Churn: No strong difference in churn by gender.
      -SeniorCitizen vs. Churn:
      -Countplot and stacked bar chart indicate higher churn among senior citizens.

 8. Tenure Impact (Cells 21–22)
      -Histogram of Tenure by Churn shows that:
      -Customers with low tenure (1–2 months) are more likely to churn.
      -Long-tenured customers tend to stay.

 9. Contract Type Analysis (Cells 23–24)
      -Customers on month-to-month contracts are significantly more likely to churn than those on yearly plans.

 10. Payment Method Insights (Cells 27–28)
       -Churn is higher among those paying via Electronic Check compared to credit card, mailed check, or bank transfer.

 11. Categorical Feature Preparation (Cell 26)
       -Lists categorical features like:
       -'PhoneService', 'InternetService', 'StreamingTV', etc.
       -Likely setup for batch visualization (e.g., subplots of countplots).

