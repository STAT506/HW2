# HW2

### Q1.  

#### a. (6 pts - 1/2 page or so)
Summarize the key points from the talk (on January 27).

#### b. (4 pts - 1/4 page or so)
What are you still confused about?

### Q2. (4 points)

Write out the three different models (feel free to use the Housing Dataset for context). For each model summarize how the slope and intercept of the model can be interpreted. Partial R code is provided for first two models, more on the third later...

```
library(readr)
housing_sales <-read_csv('http://math.montana.edu/ahoegh/teaching/stat408/datasets/HousingSales.csv')
```

1. Separate models for each zipcode

```
zip_vec <- housing_sales$Zip_Code

zip1 <- housing_sales %>% filter(Zip_Code == zip_vec[1])

lm_zip1 <- lm(Closing_Price ~ Living_Sq_Ft, data = zip1)
summary(lm_zip1)
```


2. Same model for each zipcode

```
lm_all <- lm(Closing_Price ~ Living_Sq_Ft, data = housing_sales)
summary(lm_all)
```


3. Hierarchical model with different slopes and intercepts.

### Q3.
Continue working on project 1. Make sure to read the [project overview](https://stat506.github.io/Project1/) and download the [Project 1 Repo](https://classroom.github.com/a/_nJaCFrq).
