# Ames Housing Data Analysis
## Project Overview
This project was completed as part of my summer internship, focusing on Exploratory Data Analysis (EDA) of the Ames Housing dataset. The goal of the project was to get to know the data, perform data quality checks, and conduct an initial exploratory analysis to prepare for building statistical models, particularly linear regression models to predict housing prices.

## Dataset
The dataset used for this analysis is the Ames Housing dataset, which contains various features related to residential homes in Ames, Iowa. The primary objective is to predict the sale price of homes based on these features.

## Project Structure
data/: Directory containing the dataset.
notebooks/: Jupyter notebooks used for the analysis.A
scripts/: Python scripts for data preprocessing and visualization.
results/: Directory containing the generated plots and analysis results.
README.md: This readme file.
## Project Structure

This project follows a standard directory structure to organize the code, data, and documentation.

### Directory Structure
  ```
Week1_EDA/
│
├── data/
│ ├── Ames_Housing_Data.xlsx
│
├── notebooks/ Jupyter notebooks used for the analysis.
│ ├── Sampling.ipynb (Choosing the Population of interest by removing the unwanted data, (eg: commercial real estate data).)
│ └── Cleaning.ipynb (Selected the best 20 variable to perform cleaning like handling missing value, etc)
│
├── README.md: This readme file.
```

## Steps Performed

### 1. Data Survey

**Objective:** Understand the data and its structure.

**Actions:**
- Loaded the dataset.
- Displayed basic information about the dataset.
- Displayed statistical summary of the dataset.

### 2. Data Quality Check

**Objective:** Ensure the data is clean and ready for analysis.

**Actions:**
- Checked for missing values.
- Imputed missing values for Alley and MasVnrType, etc.
- Replaced missing values in LotFrontage using the formula sqrt(LotArea/2.3).

### 3. Initial Exploratory Data Analysis

**Objective:** Explore the data to understand distributions and relationships.

**Actions:**
- Created scatter plots for numerical features against SalePrice.
- Created box plots for categorical variables against SalePrice.
- Visualized the frequency of categorical variables using bar graphs.
- Generated a correlation heatmap.

### 4. Data Preparation for Modeling

**Objective:** Prepare the data specifically for linear regression modeling.

**Actions:**
- Excluded non-residential real estate based on zoning.
- Dropped rows where SalePrice > 500000 and LotFrontage < 220.
- Excluded non-normal sale conditions.
- Excluded non-typical home functionality.
- Ensured only single-family homes were included.

### 5. Log Transformation

**Objective:** Analyze the effect of log transformation on SalePrice.

**Actions:**
- Added a new column LogSalePrice.
- Plotted a histogram for LogSalePrice.
- Calculated the correlation between LotFrontage and LogSalePrice.

### 6. Outlier Treatment

**Objective:** Handle outliers in the dataset.

**Actions:**
- Removed rows outside 3 standard deviations of SalePrice.
- Reset the index after deleting rows.

### 7. Linear Regression Analysis

**Objective:** Perform linear regression for each numerical feature against SalePrice.

**Actions:**
- Fitted linear regression models for each numerical feature.
- Created scatter plots with regression lines.

## How to Use

### Prerequisites

Before you begin, ensure you have met the following requirements:
- Python 3.x installed on your machine.
- The following Python libraries installed:
  - pandas
  - numpy
  - seaborn
  - matplotlib
  - scikit-learn
  - scipy

### Installation

1. Clone the repository to your local machine:
   ```sh
   git clone https://github.com/Krishnansh03/Week1_EDA.git

2. Navigate to the project directory:
   ```sh
   cd Week1_EDA
3. Install the required libraries:
   ```sh
   pip install -r requirements.txt

## Conclusion
This project provided a comprehensive understanding of the Ames Housing dataset through EDA. The insights gained will be instrumental in building and refining predictive models for housing prices.

## Acknowledgments
Thank you to my internship supervisor and mentors for their guidance.
The dataset was sourced from the [Ames Housing Dataset](https://www.kaggle.com/datasets/marcopale/housing).
