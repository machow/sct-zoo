---
title       : Spec work
description : Insert the chapter description here


--- type:NormalExercise lang:python xp:100 skills:2 key:9bf2dd5ff3
## Test Highlighting 


*** =instructions

Note that in pythonwhat it marks the starting line, col, and ending line, col

*** =hint

*** =pre_exercise_code
```{python}

from urllib.request import urlretrieve; urlretrieve('http://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/moby_opens.txt', 'moby_dick.txt')

```

*** =solution
```{python}

# # Read & print the first 3 lines
with open('moby_dick.txt') as file:
    print(file.readline())
    print(file.readline())
    print(file.readline())

# # The rows that you wish to print
I = [0,1,3,5,6,7,8,9]

# # Print out these rows
with open('moby_dick.txt') as file:
    for i, row in enumerate(file):
        if i in I:
            print(row)

```

*** =sample_code
```{python}

# # Read & print the first 3 lines
with open('moby_dick.txt') as file, open('moby_dick.txt'):
    print(file.readline())
    print(file.readline())
    print('test')

# # The rows that you wish to print
I = [0,1,3,5,6,7,8,9]

# # Print out these rows
with open('moby_dick.txt') as not_file:
    for i, row in enumerate(not_file):
        if i in I:
            print(row)
            
```

*** =sct
```{python}
test_with(1, context_vals=True)
success_msg("Nice work!")
```