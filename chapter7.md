---
title       : Bokeh sct import errors
description : Insert the chapter description here



--- type:NormalExercise lang:python xp:100 skills:2 key:0928693546
## <<<New Exercise>>>



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}
import pandas as pd
from bokeh.models import ColumnDataSource

source = ColumnDataSource(data={
    'x'       : [1,2,3],
    'y'       : [1,2,3]
})

```

*** =sample_code
```{python}
```

*** =solution
```{python}
```

*** =sct
```{python}
# COMMENT LINE BELOW TO REMOVE ERROR
import pandas as pd

def my_converter2(source):
    return True
set_converter(key = "bokeh.models.sources.ColumnDataSource", fundef = my_converter2)

test_object('source')

```

--- type:NormalExercise lang:python xp:100 skills:2 key:01cbdf3f04
## <<<New Exercise>>>



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}
class C: pass

c = C()
c.a = 1

#import pandas as pd

```

*** =sample_code
```{python}

```

*** =solution
```{python}

```

*** =sct
```{python}
# COMMENT LINE BELOW TO REMOVE ERROR
import pandas

set_converter('__main__.C', lambda x: True)
test_object('c')
```