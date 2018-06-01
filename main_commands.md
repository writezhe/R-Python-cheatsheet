# Parallel Code Between R and Python

## Text-Editing

```{r}
paste("X", seq(1,5))
```
```{python}
["X%d" % i for i in range(1,6)]
map('X{}'.format, range(1, 6))
```
