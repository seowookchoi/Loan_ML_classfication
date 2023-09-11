# Loan Eligibility Prediction






### 1. Problem Statement:

Stock Yards Bank & Trust, currently handles loan applications through manual processes. Due to the subjective nature of loan approvals and the influx of applications, making decisions has become challenging. To streamline this, they aim to develop an automated machine learning system to assess various criteria and determine loan approval.

In this project, the goal is to create a classification model to decide if a loan should be granted. We'll consider several factors, such as the applicant's credit rating and previous loan history, to predict their eligibility. Data cleaning will be essential, filling gaps and ensuring the model's reliability. The end result will provide a probability score, indicating either "Loan Approved" or "Loan Denied" based on the model's analysis. Code for the projects is in "SW_pred.ipynb"





### 2. Data Description
- **Loan ID:** Loan ID (uique id)
- **Customer ID:** (non-unique, single customer can have multiple loan records)
- **Loan Status:** Target binary metric, Loan Given/Loan Refused.
- **Term:** Binary, short/long
- **Credit Score:** Credit score 0~800
- **Years in current job:** Ordered
- **Home Ownership:** Categorical, ex) Rent, Own
- **Annual Income:** Annual income in US dollars
- **Monthly Debt:** Monthly Debt in US dollars
- **Years of Credit History:** in years
- **Months since last delinquent:** in months
- **Number of Open Accounts:** Count in positive integer
- **Number of Credit Problems:** Count in positive integer, Zero inflated
- **Current Credit Balance:** in US dollars
- **Maximum Open Credit:** in US dollars
- **Bankruptcies:** Binary, 0/1
- **Tax Liens:** Binary, 0/1

### 3. Data Prep and EDA
As the target variable for the modeling is "Loan Status", we need to examine this feature closely. Since this feature is binary, the modeling problem will be a classification task. The data is not balanced, though it's not severely imbalanced either. In subsequent sections, we will work with the raw imbalanced data and also explore resampling methods to achieve balance.
![Alternative text describing the image](loan_given.png)

Soft impute is used to address missing values. Additionally, outliers were removed and the data was winsorized. For instance, in the credit score feature, some data had four-digit scores instead of the typical three-digit scores. These discrepancies were corrected before modeling. Below is a histogram illustrating the credit score distribution after cleaning. There's a peak at one point, representing the default credit score. Such a distribution is expected.
![Alternative text describing the image](Credit_score_histo_loan.png)

### 4. Modelling and Evaluation

### 5. Results
Open the Command Prompt by pressing Win + R, typing "cmd", and pressing Enter.

Change the directory to the desired location for your project:

`cd C:\path\to\project`

Create a new virtual environment using the Python Launcher:

`py -3.8 -m venv myenv`

Note: Replace myenv with your desired virtual environment name.

Activate the virtual environment:

`myenv\Scripts\activate`

Install the project requirements using pip:

`pip install -r requirements.txt`


For Linux/Mac:

Open a terminal.

Change the directory to the desired location for your project:

`cd /path/to/project`

Create a new virtual environment using the Python Launcher:

`python3.8 -m venv myenv`
Note: Replace myenv with your desired virtual environment name.

Activate the virtual environment:

`source myenv/bin/activate`
Install the project requirements using pip:

`pip install -r requirements.txt`


By specifying the version using py -3.8 or python3.8, you can ensure that the virtual environment is created using Python 3.8.10 specifically, even if you have other Python versions installed.



