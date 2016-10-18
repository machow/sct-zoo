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

```

*** =solution

```{python}
a = 1
```

*** =sct

```{python}
test_object('a')
```

description : Insert the chapter description here