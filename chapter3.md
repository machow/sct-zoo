---
title       : Insert the chapter title here

--- type:NormalExercise lang:python xp: skills: key:ed1f7681ab
## test_object using accessor

Note that `test_object_accessed` works as expected, but `test_object` causes an error

*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
class X:
    a = 1
    
X.a
```

*** =solution
```{python}
class X:
    a = 1
    
X.a
```

*** =sct
```{python}
test_object_accessed('X.a')
test_object('X.a')
```

--- type:NormalExercise lang:python xp: skills: key:75c443b691
## <<<TITLE>>> 


*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code

```{python}
for ii in range(2): ii + 1
```

*** =solution

```{python}
for ii in range(2): ii
```

*** =sct

```{python}
test_for_loop(body=test_expression_result(incorrect_msg='wrong'))
```

description : Insert the chapter description here