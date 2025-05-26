# Supply Chain Dataset Analysis

This report provides a structural and exploratory analysis of the dataset contained in the file `processed_supply_chain.xlsx`.

## Dataset Overview

- **File Name:** `processed_supply_chain.xlsx`
- **Worksheet Name:** `processed_supply_chain`
- **Number of Records:** 99 rows
- **Number of Features:** 27 columns

## Dataset Structure

The dataset contains a mix of categorical and numerical data types:

- **Categorical Columns (10):**
  - Examples: `haircare`, `SKU0`, `Non-binary`, `Carrier B`, `Supplier 3`, `Mumbai`, `Pending`, `Road`, `Route B`, `nan.2`

- **Numerical Columns (17):**
  - Examples: `69.8080055421157`, `55`, `802`, `8661.99679239238`, `58`, `7`, `96`, `4`, `29`, `215`, `29.1`, `46.2798792405083`, `0.226410360849925`, `nan.1`, `187.752075459203`

Note: Several column names appear to be numerical values or placeholder names (e.g., `nan`, `nan.1`, `nan.2`), which may require cleaning or renaming for clarity and usability.

## Key Observations

### Categorical Data

- The column `haircare` includes three distinct product categories. The most frequent category is "skincare".
- The `Non-binary` column includes four unique values, with "Unknown" being the most common.
- Columns such as `Pending`, `Carrier B`, `Road`, and `Route B` include a limited number of distinct values and are suitable for encoding.

### Numerical Data

- The dataset includes features with a wide range of values, suggesting differences in units (e.g., quantity, price, distance).
- Examples:
  - Column `8661.99679239238`: Mean = 5746.90, Max = 9866.47
  - Column `0.226410360849925`: Values range from 0.0186 to 4.9393
  - Column `nan.1`: Appears to contain continuous numerical values, possibly representing cost or time

## Data Quality and Cleaning Recommendations

- Several columns are unnamed or use non-descriptive numeric strings as names. These should be renamed to improve readability and consistency.
- Potential redundancy or duplication may exist among columns. This should be examined during data cleaning.
- Categorical values should be standardized and encoded as needed for machine learning applications.

## Recommendations for Further Analysis

1. **Column Renaming**
   - Replace ambiguous column names with descriptive labels.

2. **Normalization and Scaling**
   - Normalize numerical values to improve model performance and comparability.

3. **Encoding Categorical Features**
   - Apply label encoding or one-hot encoding to prepare the data for modeling.

4. **Feature Engineering**
   - Derive additional features such as:
     - Encoded product categories
     - Supplier performance scores
     - Route reliability indicators

5. **Outlier Detection**
   - Investigate numerical columns with high standard deviations to identify and handle potential outliers.

## Conclusion

The dataset offers a comprehensive view of various aspects of a supply chain process, combining product, supplier, and logistical information. However, improvements are needed in column naming and data standardization before any predictive modeling or operational analytics can be performed effectively.
