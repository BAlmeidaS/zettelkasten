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

get all the *number of the occurrences (table of frequencies)* of a categorical column - `table`
```R
table(df$cat_1)
# or multi column table
table(df$cat_1, df$cat_2)
# addmargins to put on the the sum of each category
addmargins(table(df$cat_1, df$cat_2))
# or with the proportions
prop.table(table(df$cat_1, df$cat_2))

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
hist(df$col_a, prob=T)
lines(density(df$col_a), col="red")
```

Boxplots
```R
Boxplot(df$numeric, df$numeric_2, ...)
# you can filter a numeric column with a cat (factored) column
Boxplot(df$numeric ~ as.factor(df$categorical))
```

setting seed
```R
set.seed(42)
```

cbind combine vectors to create dataframe, and rbind new rows
```R
df <- as.data.frame(cbind(vec1, vec2))
# can be used with dfs as well
df <- cbind(df0, vec2)
# adding rows
new_row = c(1, "a", ...)
df <- rbind(df, new_row)
```

Head / Tail of a dataset
```R
head(df)
tail(df)
```

### basic about ggplot
```R
ggplot(data=df, aes(x=col, y=col)) + geom_*()

# to change ylim
+ ylim(y0, y1)

# to add a title
+ ggtitle("My title")

# to add label to x or y
+ xlab("my x label") + ylab("my y label")

# change the scale y (1)
+ scale_y_continuous(trans = "log10")

# to add smooth function
+ stat_smooth(span=)

# to save a png
ggsave("filename.png") # after the plot
```

(1) - [scale functions](https://bookdown.dongzhuoer.com/hadley/ggplot2-book/scale-transformation)


## libraries
```R
library(tidyverse)
library(wordcloud)
library(RColorBrewer)
library(wordcloud2)
library(tm)
```

[color names of RColorBrewer](https://r-graph-gallery.com/42-colors-names.html)
