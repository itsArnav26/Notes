## Table of Contents

## About Pandas

- Pandas is a `Python library` used for `data manipulation` and `analysis`. It provides data structures like `Series` and `DataFrame` that allow users to store, organize, clean, and analyze structured data efficiently.

## Dataframe

- A DataFrame in Pandas is a two-dimensional, labeled data structure used to store and organize data in rows and columns, similar to a table or spreadsheet.

## Creating Dataframe

-use function : `DataFrame`

```py
df = pd.dataFrame([11,22,33])
df
type(df)
```

Output:

```py
	0 # since we have not mentioned column name,so it take as zero
0	11
1	22
2	33
pandas.core.frame.DataFrame
```

```py
df = pd.DataFrame([11,22,33],columns = ['col_name'])
df
```

Output:

```py
col_name
0	11
1	22
2	33

```

## head,tail,rename,info,describe

```py
data = {
    "Name": ["Arnav", "Rahul", "Sneha", "Priya", "Amit", "Neha"],
    "Age": [21, 22, 20, 23, 24, 22],
    "Salary": [30000, 35000, 28000, 40000, 45000, 32000],
    "Gender": ["Male", "Male", "Female", "Female", "Male", "Female"]
}
df = pd.DataFrame(data)
df
```

Output:

```py
Name	Age	Salary	Gender
0	Arnav	21	30000	Male
1	Rahul	22	35000	Male
2	Sneha	20	28000	Female
3	Priya	23	40000	Female
4	Amit	24	45000	Male
5	Neha	22	32000	Female

```

- `head :`
- Give the rows from top
- By default it will give `top 5` rows
- Ex: df.head(1)

```py
Name	Age	Salary	Gender
0	Arnav	21	30000	Male
```

- `tail :`
- Give the rows from Bottom
- By default it will give `bottom 5` rows
- Ex: df.tail()

```py
Name	Age	Salary	Gender
1	Rahul	22	35000	Male
2	Sneha	20	28000	Female
3	Priya	23	40000	Female
4	Amit	24	45000	Male
5	Neha	22	32000	Female
```

- `rename :`
- Use to rename column

```py
df1.renmae(columns = {'Gender':'Sex'})
df1
```

```py
Name	Age	Salary	Gender
1	Rahul	22	35000	Male
2	Sneha	20	28000	Female
3	Priya	23	40000	Female
4	Amit	24	45000	Male
5	Neha	22	32000	Female
```

- Now by default `inplace` is False,that means the changes will not effect in orignal DataFrame
- If it is True:

```py
df1.renmae(columns = {'Gender':'Sex'},inplace = True)
df1
```

Output:

```py
Name	Age	Salary	Sex
0	Arnav	21	30000	Male
1	Rahul	22	35000	Male
2	Sneha	20	28000	Female
3	Priya	23	40000	Female
4	Amit	24	45000	Male
5	Neha	22	32000	Female
```

- `info`
- Will give the summary of DataFrame

```py
df1.info()
```

```py
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 6 entries, 0 to 5
Data columns (total 4 columns):
 #   Column  Non-Null Count  Dtype
---  ------  --------------  -----
 0   Name    6 non-null      object
 1   Age     6 non-null      int64
 2   Salary  6 non-null      int64
 3   Gender  6 non-null      object
dtypes: int64(2), object(2)
memory usage: 324.0+ bytes
```

- `describe`
- used to generate statistical summary of **`numerical columns`** in a DataFrame.

```py
df1.describe()
```

```py
Age	Salary
count	6.000000	6.000000
mean	22.000000	35000.000000
std	1.414214	6449.806199
min	20.000000	28000.000000
25%	21.250000	30500.000000
50%	22.000000	33500.000000
75%	22.750000	38750.000000
max	24.000000	45000.000000
```
