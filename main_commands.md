# Parallel Code Between R and Python

### Text-Editing

creating a sequential list of strings

*R*
```{R}
paste0("X", seq(1,5))
```
*Py*
```{python}
["X%d" % i for i in range(1,6)]
map('X{}'.format, range(1, 6))
```

collapsing a list of strings

*R*
```{R}
paste0("X", seq(1,5), collapse = " + ")
```
*Py*
```{python}
" + ".join(["X%d" % i for i in range(1,6)])
```
