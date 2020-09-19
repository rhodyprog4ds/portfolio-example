---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.2'
      jupytext_version: 1.6.0
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

```python
import seaborn as sns
import matplotlib.pylab as plt
import pandas as pd
```

# Dataset 1


Load the data to a notebook as a `DataFrame` from url.

```python
iris_df = pd.read_csv('https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data')

```

Explore the dataset in a notebook enough to describe its structure
  - shape
  - columns
  - variable types

```python
iris_df.shape
```

```python
iris_df.columns
```

```python
iris_df.dtypes
```

This dataset doesn't have headings.


Display overall summary statistics

```python
iris_df.describe()
```

Display overall summary statistics grouped by a categorical variable

```python
iris_df.groupby('Iris-setosa').describe()
```

For two continuous variables make a scatter plot and color the points by a categorical variable

```python
sns.lmplot('5.1', '3.5',data=iris_df,hue = 'Iris-setosa',fit_reg=False)
```

Pose one question for this dataset that can be answered with summary statistics, compute a statistic and plot that help answer that exploratory question.

```python

```

```python

```

# Data Set 2

```python
tips_df = sns.load_dataset("tips")
```

```python
tips_df.shape
```

```python
tips_df.columns
```

```python
tips_df.dtypes
```

Display two individual summary statistics for one variable

```python
tips_df['total_bill'].mean()
```

```python
tips_df['total_bill'].max()
```

Group the data by two categorical variables and display a table of one summary statistic

```python
tips_df.groupby(['time','sex'])['tip'].mean().unstack()
```

Use a `FacetGrid` to make a plot that shows something informative about this data, using both categorical variables and at least one numerical value. Describe what this tells you about the data. 

```python
g = sns.FacetGrid(tips_df, col="time",  row="sex")
g.map(sns.scatterplot, "total_bill", "tip")
```

```python

```
