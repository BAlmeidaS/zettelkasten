How to remove a column of a dataset
```R
df = subset(df, select = -c(name_col))
```

replace all instances of a word in your dataset for something else
```R
df[df=="old string"] <- "new string"
```

replace all instances in of a column to something else
```R
df$col[df$col=="old string"] <- "new string"
```

get all the *number of the occurrences* of a categorical column - `table`
```R
table(df$cat_col)
```

`NA` is different than `NAN`

counting NAs:
```R
# all the dataset
sum(is.na(df))
# per column
colSums(is.na(df))
```

Get the structure of a dataframe
```R
# str stands for STRUCTURE
srt(df)
```

Quite often is handy to change categorical variables in factors:
```R
df$cat_var <- as.factor(df$cat_var)
```

use `summary` to *get info*
```R
summary(df)
summary(df$col)
```

Martin like to put *density functions over histograms*
```R

```
