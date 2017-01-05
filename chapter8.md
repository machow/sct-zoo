---
title       : Docs
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:2 key:bb6f6112b6
## Expression Call



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}
```

*** =sample_code
```{python}
def my_fun(x, y = 4, z = ('a', 'b'), *args, **kwargs):
    return [x, y, *z, *args]
```

*** =solution
```{python}
def my_fun(x, y = 4, z = ('a', 'b'), *args, **kwargs):
    return [x, y, *z, *args]
```

*** =sct
```{python}
Ex().check_function_def('my_fun').call("f(1, 2, (3,4), 5, kw_arg='ok')")
Ex().check_function_def('my_fun').call([1, 2, (3,4), 5])
```

--- type:NormalExercise lang:python xp:100 skills:2 key:2e8bd19ffc
## Check function - simple sum



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
sum([1,2,3])
```

*** =solution
```{python}
sum([1,2,3])
```

*** =sct
```{python}
Ex().check_function('sum', 0).check_args(0).has_equal_ast()
```

--- type:NormalExercise lang:python xp:100 skills:2 key:0974b37dd1
## Check function complex sum



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
sum([i for i in range(10)])
```

*** =solution
```{python}
sum([i for i in range(10)])
```

*** =sct
```{python}
(Ex().check_function('sum', 0)
    .check_args(0)
    .check_list_comp(0)
    .has_equal_ast()
    )
   ```