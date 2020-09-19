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
import pandas as pd
```

```python
d1 = {'url': 'https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data',
      'name':'iris',
      'load_func': lambda path: pd.read_csv(path)}
d2 = {'url': 'https://raw.githubusercontent.com/brownsarahm/python-socialsci-files/master/data/SAFI.json',
     'name':'safi',
     'load_func': lambda path: pd.read_json(path)}
d3 = {'url':'https://rhodyprog4ds.github.io/BrownFall20/syllabus/grading.html',
     'name': 'min_acheivements',
     'load_func': lambda path: pd.read_html(path)[0]}

dataset_list = [d1,d2,d3]
```

```python
# test the dicts
d1['load_func'](d1['url'])
```

```python
# test spitting
d1['url'].split('/')[-1]
```

```python
data_info = []
column_names = ['name','source','num_rows', 'num_columns','source_file_name']

for dataset in dataset_list:
    df = dataset['load_func'](dataset['url'])
    source_file_name = dataset['url'].split('/')[-1]
    num_rows, num_cols = df.shape
    data_info.append([dataset['name'],dataset['url'],num_rows,
                      num_cols,source_file_name])
    
summary_df = pd.DataFrame(data_info,columns=column_names)
summary_df
```

```python
summary_df.to_csv('dataset_summary.csv')
```

# Exploring Safi

```python
d2
```

Load it into a data frame

```python
safi_df = d2['load_func'](d2['url'])
```

Show the last 7 rows

```python
safi_df.tail()
```

## Two ways to pick out the non numerical columns

```python
non_num_cols = safi_df.columns[safi_df.dtypes =='object']
non_num_cols
```

```python
nn_cols = [col for col in safi_df.columns if safi_df[col].dtypes =='object']
nn_cols
```

```python
list(non_num_cols) == nn_cols
```

Sentences about the format of the data


## Exploring Iris

```python
d1
```

```python
iris_df = d1['load_func'](d1['url'])
```

```python
iris_df.head(3)
```

```python
iris_df.dtypes
```

All of these look like the datatype I expected


## Exploring Minimum achievments

```python
d3
```

```python
min_acheivements_df = d3['load_func'](d3['url'])
```

```python
min_acheivements_df.columns
```

```python
min_acheivements_df[[('Level 3', 'Unnamed: 1_level_1'),
            ('Level 2', 'Unnamed: 2_level_1'),
                     ('Level 1', 'Unnamed: 3_level_1')]]
```

```python
min_acheivements_df[[('Level 3', 'Unnamed: 1_level_1'),
            ('Level 2', 'Unnamed: 2_level_1'),
                     ('Level 1', 'Unnamed: 3_level_1')]].loc[:10:2]
```

## Scratch

```python
[type(d) for d in d1.items()]
```

```python
opt1 = [char for char in 'abcde']
opt2 = {char:i for i, char in enumerate('abcde')}
opt3 = ('a','b','c','d','e')
opt4 =  'a b c d e'.split(' ')
```

```python
options = [opt1, opt2, opt3, opt4]

for i,op in enumerate(options):
    print(i+1,': ',op)
```

```python
options[[type(op)==dict for op in options]]
```

```python

```
