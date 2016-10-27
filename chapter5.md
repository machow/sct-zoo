---
title       : Github issues

--- type:NormalExercise lang:python xp: skills: key:9d98ff1534
## tw #71 test_function


*** =instructions

*** =hint

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}

```

*** =solution
```{r}
# Load the tidyr package
library(tidyr)

# Gather the six mu/nu/di/hr/co/ec columns
votes_joined %>%
  gather(topic, has_topic, me:ec)

# Perform gather again, then filter
votes_gathered <- votes_joined %>%
  gather(topic, has_topic, me:ec) %>%
  filter(has_topic == 1)
```

*** =sct
```{r}
test_function("gather", args = c("data", "key", "value"))
```
description : Insert the chapter description here