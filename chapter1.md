---
title       : Insert the chapter title here
description : Insert the chapter description here
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

--- type:NormalExercise lang:python xp:100 skills:1 key:b1c43870e7
## Testing for *args call in a function signature


*** =instructions
- No

*** =hint
- No

*** =sample_code
```{python}
# Create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)

# Print the tuples in z1 by unpacking with *
print(*z1)

# Re-create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)

# 'Unzip' the tuples in z1 by unpacking with * and zip(): result1, result2
# WILL PASS
# result1, result2 = zip(*z1)

# WILL FAIL (though produces same result)
z2 = list(z1)
result1, result2 = zip(z2[0], z2[1], z2[2], z2[3], z2[4])

# Check if unpacked tuples are equivalent to original tuples
print(result1 == mutants)
print(result2 == powers)

```

*** =pre_exercise_code
```{python}
# Create a tuple of strings: mutants
mutants = ('charles xavier', 'bobby drake', 'kurt wagner', 'max eisenhardt', 'kitty pride')

# Create a tuple of strings: powers
powers = ('telepathy', 'thermokinesis', 'teleportation', 'magnetokinesis', 'intangibility')

```

*** =solution
```{python}
# Create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)

# Print the tuples in z1 by unpacking with *
print(*z1)

# Re-create a zip object from mutants and powers: z1
z1 = zip(mutants, powers)

# 'Unzip' the tuples in z1 by unpacking with * and zip(): result1, result2
result1, result2 = zip(*z1)

# Check if unpacked tuples are equivalent to original tuples
print(result1 == mutants)
print(result2 == powers)

```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

#test_function('zip', index=3, do_eval=False, incorrect_msg="exact name of *args variable did not match")
test_function_v2('zip', index=3, do_eval=False, incorrect_msg="exact name of *args variable did not match")
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp: skills: key:a669c81599
## Manual Signatures

*** =pre_exercise_code
```{python}
import pandas as pd

# Make DataFrame of iris data
import sklearn.datasets
data = sklearn.datasets.load_iris()
df = pd.DataFrame(data.data, columns=data.feature_names)
df['species'] = data.target
df = df.rename(columns={'petal length (cm)': 'petal_length'})
for i in [0, 1, 2]:
    df.loc[df['species']==i, 'species'] = data.target_names[i]

df = df[['species', 'petal_length']]

# Extract Series that has versicolor petal lengths
versicolor_petal_length = df.loc[df.species=='versicolor',
                                 'petal_length'].values
```

*** =solution
```{python}
# Import plotting modules
import matplotlib.pyplot as plt
import seaborn as sns

# Set default Seaborn style
sns.set()

# Plot histogram of versicolor petal lengths
_ = plt.hist(versicolor_petal_length)

# Show histogram
plt.show()

```

*** =sct
```{python}

test_import("matplotlib.pyplot")

test_import("seaborn")

test_function("seaborn.set")

#sig = sig_from_params(param("x", param.POSITIONAL_OR_KEYWORD))

#test_function_v2("matplotlib.pyplot.hist", params=["x"], not_called_msg="Did you create the histogram using `plt.hist`?", incorrect_msg="Did you pass the correct argument to `plt.hist`?")


#test_object("_", undefined_msg="Did you create the histogram as `_`?", incorrect_msg="Did you pass the correct argument to 'plt.hist'?")

test_function("matplotlib.pyplot.show")

success_msg("Great work!")
```

--- type:NormalExercise lang:python xp: skills: key:2ca71f9e6a
## Nested list comp


*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
matrix = [[col for col in range(5)] for row in range(5)]
```

*** =solution
```{python}
matrix = [[col for col in range(5)] for row in range(5)]
```

*** =sct
```{python}
def inner_list_comp():
    test_list_comp(body = lambda: test_expression_result(context_vals=[2]),
                   comp_iter = lambda: test_function('range'))
test_list_comp(body = inner_list_comp, 
               comp_iter = lambda: test_function('range'))
```
