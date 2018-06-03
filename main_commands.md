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
