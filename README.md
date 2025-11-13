1. Load Dataset

Used pandas.read_csv() to load the raw CSV file into a DataFrame.

2. Clean Column Names

Converted all column names to a consistent format:

lowercase

no spaces

underscores instead of spaces

This improves readability and makes coding easier.

3. Convert Date Column

Transformed dt_customer from string to proper datetime using:

pd.to_datetime()


This enables date-based analysis in the future.

4. Handle Missing Values

Even though the dataset contained no missing values, the cleaning script includes:

median fill for numeric columns

mode fill for categorical columns

This ensures the script is robust and reusable.

5. Create Age + Remove Invalid Ages

Created a new column:

age = 2024 - year_birth


Filtered out records with unrealistic ages (only kept 18–100).

6. Drop Duplicates

Removed all duplicate rows to ensure clean, unique data.

7. Convert Datatypes

Converted:

education and marital_status → categorical

all numeric-like columns → numeric types

dt_customer → datetime

This ensures accurate analysis and modeling.

8. Save Cleaned Dataset

Exported the cleaned DataFrame as:

cleaned_customer_personality_analysis.csv
