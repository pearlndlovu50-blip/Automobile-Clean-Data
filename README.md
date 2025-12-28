
## Key Cleaning Steps (From Notebook)

1. **Load & Inspect**
import pandas as pd
df = pd.read_csv('Automobile_data.csv')
df.shape # (61, 10)
df.info() # 3 missing prices
2. **Handle Missing Prices**
df['price'] = pd.to_numeric(df['price'], errors='coerce')
price_mean = df['price'].mean() # 15387.0
df['price'] = df['price'].fillna(price_mean)

3. **Data Quality Checks**
- No duplicates: `df.duplicated().sum()` → 0
- Price range: $5,151 - $45,400
- Stats: mean wheel-base 98.48", avg horsepower 107.85

## 📁 Files Included
- `Automobile_data.csv` - Raw messy data
- `data_cleaning.ipynb` - Full Jupyter walkthrough
- `automobile_cleaned.csv` - Final production-ready dataset

## 💼 Skills Demonstrated
Pandas - Data Cleaning - Missing Value Imputation -
Data Inspection - Jupyter Notebooks - Descriptive Stats
