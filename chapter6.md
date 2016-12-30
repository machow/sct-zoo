---
title       : Backend pickle error
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:2 key:8d41eae9b6
## <<<New Exercise>>>



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}
import pandas as pd

class C: pass
```

*** =sample_code
```{python}
c = C()
c.a = 1
```

*** =solution
```{python}
c = C()
c.a = 1
```

*** =sct
```{python}
import pandas as pd

def my_converter(x):
    return pd.DataFrame({'a': [x.a]})

set_converter('__main__.C', my_converter)

test_object('c')
```
