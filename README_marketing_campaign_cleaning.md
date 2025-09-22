# Data Cleaning Summary - marketing_campaign.csv

- Original shape: (2240, 29)
- Shape after cleaning: (2240, 30)
- Removed exact duplicate rows: 0
- Duplicate rows removed after transforms: 0
- Columns dropped due to >80% missing: []

## Top missing values BEFORE cleaning

- Income: 24

## Missing values AFTER cleaning

- id: 0
- year_birth: 0
- response: 0
- z_revenue: 0
- z_costcontact: 0
- complain: 0
- acceptedcmp2: 0
- acceptedcmp1: 0
- acceptedcmp5: 0
- acceptedcmp4: 0

## Key transforms applied

- Standardized column names to snake_case.
- Parsed `dt_customer` to datetime (if present).
- Created `age` column = 2025 - year_of_birth (if birth-year column found).
- Treated non-positive `income` as missing and filled with median, then clipped outliers by IQR.
- Standardized `education` and `marital_status` text values.
- Converted float columns that represent integer counts to integer dtype where appropriate.
- Dropped columns with >80% missing values (if any).
- Removed duplicate rows.
