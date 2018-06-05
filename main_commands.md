# Parallel Code Between R and Python

### Changing Shape of DF

gather (i.e. make long)
```
# R #
gather(df, metric, val, -keep1:-keep3, val1:val4)

# Py #

```

### Munging Data

grouping by column, applying function, (and keeping column!)
```
# R #
df %>% group_by(grp_col) %>%
# one of the 3 below
  mutate() # per row functions %>%
  do() # per group functions %>%
  summarize() # summarize each group into 1 row

# Py #
dfg = df.groupby(grp_col)
dfg.apply() # per group functions
dfg.mean
```

### Text-Editing

creating a sequential list of strings
```
#R#
paste0("X", seq(1,5))

#Py#
["X%d" % i for i in range(1,6)]
map('X{}'.format, range(1, 6))
```

collapsing a list of strings
```
#R#
paste0("X", seq(1,5), collapse = " + ")

#Py#
" + ".join(["X%d" % i for i in range(1,6)])
```

### Useful External Similar Exercises

[dplyr <-> pandas][http://pandas.pydata.org/pandas-docs/stable/comparison_with_r.html]
[R to Python wrangling][https://gist.github.com/conormm/fd8b1980c28dd21cfaf6975c86c74d07]
[summary of 3 piping options in pandas][http://fastml.com/piping-in-r-and-in-pandas/]
[use of dfply package to pipe][https://towardsdatascience.com/dplyr-style-data-manipulation-with-pipes-in-python-380dcb137000]
[use of pandas-ply package to pipe][https://pythonhosted.org/pandas-ply/]

Plotting Package Comparison and Discussion

[ggplot approximations in python][https://dsaber.com/2016/10/02/a-dramatic-tour-through-pythons-data-visualization-landscape-including-ggplot-and-altair/]
