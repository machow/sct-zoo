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

test_function('zip', index=3, do_eval=False, incorrect_msg="exact name of *args variable did not match")
success_msg("Great work!")
```
