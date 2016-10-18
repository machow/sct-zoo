---
title       : Lambdaless

--- type:NormalExercise lang:python xp: skills: key:7ae8ce7d91
## <<<TITLE>>> 


*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
dice = 2
if dice <= 2:
    print('too low')

```

*** =solution
```{python}
dice = 2
if dice <= 2:
    print('too low')
```

*** =sct
```{python}
# use list comprehension of sub tests
msg = "In the condition of your `if` part, make sure you use `dice <= 2`."
test_if_else(1, 
             test = lambda msg=msg: [test_expression_result({"dice": i}, incorrect_msg = msg) for i in range(1,7)], 
             expand_message = False)
             
```
description : Insert the chapter description here
