# Pandas DataFrame Operations

## Creating a DataFrame
```python
import pandas as pd

data = {'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35]}
df = pd.DataFrame(data)
```

## Viewing Data
```python
df.head()      # First 5 rows
df.tail()      # Last 5 rows
df.info()      # DataFrame info
df.describe()  # Statistical summary
```

## Selecting Data
```python
df['Name']           # Select column
df[['Name', 'Age']]  # Select multiple columns
df.loc[0]            # Select row by label
df.iloc[0]           # Select row by index
```

## Filtering Data
```python
df[df['Age'] > 28]   # Rows where Age > 28
```

## Adding/Removing Columns
```python
df['Salary'] = [50000, 60000, 70000]  # Add column
df.drop('Salary', axis=1, inplace=True)  # Remove column
```

## Sorting Data
```python
df.sort_values('Age', ascending=False)
```

## Grouping Data
```python
df.groupby('Age').mean()
```

## Handling Missing Data
```python
df.dropna()      # Remove rows with missing values
df.fillna(0)     # Replace missing values with 0
```