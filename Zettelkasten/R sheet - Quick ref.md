# Pure R
create a vector of numeric values with 10k spaces
```R
vec <- numeric(10000)
```

create custom function
```R
my_func <- function(param1, param2) {
  ...
  return(...)
}
my_func(1, 2)
```

size of an object in memory
```R
format(object.size(cv.df), units="auto")
```

print some var with a text - python `print(f"{}")`
```R
# paste
paste0("var:", var) # DOES NOT add a space 'var:0'
paste("var:", var) # ADD a space 'var: 0'

# glue
library(glue)
glue("var: {var}")
```

rep can be used to create massive vector
```R
numVector <- rep(c(1, 2, 3), times = 5) # 15 elems
numVector <- rep(c(1, 2, 3), length.out = 5) # 5 elems
```

sampling in a vector
```R
sample(c("M", "F", "?"), 20, replace=T)
```
# DF
First steps with a df
```R
names(df) # col names
dim(df) # dimensions
struct(df) # types of cols
View(df) # open the whole df
head(df) # just the head
tail(df) # just the tail
sum(is.na(df)) # count NAs
colSums(is.na(df)) # count NAs on the cols
summary(df) # summary - can receive cols
```

getting *variance, df and five_num* of each col:
```R
sapply(df,var)
sapply(df,sd)
sapply(df,fivenum)
```

if df has *index*
```R
row.names(df) # all the index nam
```

How to *remove a column* of a dataset
```R
df = subset(df, select = -c(name_col))
```

*replace all instances of a word* in your dataset for something else
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
# or multi column tableggtitle
table(df$cat_1, df$cat_2)
# addmargins to put on the the sum of each category
addmargins(table(df$cat_1, df$cat_2))
# or with the proportions
prop.table(table(df$cat_1, df$cat_2))

```

getting num of rows and cols isolated
```R
nrow(df)
ncol(df)
```

`NA` is different than `NAN`

*counting NAs* (`== NA` does not work ):

```R
# all the dataset 
sum(is.na(df))
# per column
colSums(is.na(df))
```

Get the *structure* of a dataframe
```R
# str stands for STRUCTURE
srt(df)
```

Quite often is handy to *change categorical variables in factors*:
```R
df$cat_var <- as.factor(df$cat_var)
```

Martin like to put *density functions over histograms*
```R
hist(df$col_a, prob=T)
lines(density(df$col_a), col="red")
```

Filtering the DF based in some querry
```R
subset(df, col_a == "condition")
```

setting seed
```R
set.seed(42)
```

cbind *combine vectors to create dataframe*, and *rbind new rows*
```R
df <- as.data.frame(cbind(vec1, vec2))
# can be used with dfs as well
df <- cbind(df0, vec2)
# adding rows
new_row = c(1, "a", ...)
df <- rbind(df, new_row)
```

*correlation* with spearman
```R
round(cor(df, method = "spearman"), 3)
```

removing NA
```R
df_without_nas <- df[complete.cases(df),]
```

get a quantile of a column regardless the distribution
```R
quantile(df$col, c(0.025, 0.975))
```

plot a table with the expected frequencies of two categories
```R
table(df$cat_1, df$cat_2)
```

# GGPLOT

```R
ggplot(data=df, aes(x=col1, y=col2)) + 
	geom_*()

# the input can be ordered with reorder
ggplot(data=df, aes(x=reorder(col_to_use_on_graph, col_to_use_to_order),
					y=col))
# or in the desc way add a minus(-)
ggplot(data=df, aes(x=reorder(col_to_use_on_graph, -col_to_use_to_order),
					y=col))
# you can a colour on the global aes to be accessed to any geom
ggplot(data=df, aes(x=col1, y=col2, colour=col3)) 

# to change ylim
+ ylim(y0, y1)

# to add a title
+ ggtitle("My title", subtitle="some subtitle")

# to add label to x or y
+ xlab("my x label") + ylab("my y label")

# change the scale y (1)
+ scale_y_continuous(trans = "log10")

# to add smooth function
+ stat_smooth(span=)

# flip to horizontal
+ coord_flip()

# rotate the x ticks
+ theme(axis.text.x = element_text(angle=90))

# if there is a colour as third dimension we can change the gradient
+ scale_colour_gradient(low = "blue", high = "red") 

# other background themes
+ theme_bw()
+ theme_minimal()
+ theme_classic()
+ theme_linedraw()

# to save a png
ggsave("filename.png") # after the plot
```
http://www.sthda.com/english/wiki/ggplot2-line-plot-quick-start-guide-r-software-and-data-visualization#create-line-plots-with-points
[ggplot theme](https://ggplot2.tidyverse.org/reference/ggtheme.html)

geom_*
```R
# scatter points with different shapes
geom_point(col="color", shape=3, size=2)
# scatter points with another column used as a 3rd dim
geom_point(aes(color=column_name))

# line will connect the datapoints on a scatter plot
geom_line()
# abline: (check also hline and vline) (2)
geom_abline(intercept= , slope= , linetype="dashed")

# create a linear model to fit the points
geom_smooth(method="lm")
geom_smooth(method="lm", se=T) # add 1 SE of error

# create a boxplots - for this one aes on ggplot can have only y
geom_boxplot(notch=T) # notch represents the CI 95%, wider=uncertain, narrow=nice

# bars 
geom_bar() # count the number (stat="count")
geom_count() # the number as it is (stat="identity")

# histrogram - each bin has the count
geom_histogram(binwidth=3, # size of the bin
			   colour="black", fill="grey")
	# adding a function to overlay the histogram
	+ geom_density(aes(y=after_stat(count)), alpha=.2, fill="blue")


# histrogram that is a probability density function - (each bin has a probability instead of the count):
geom_histogram(aes(y=after_stat(density)))
# aes because we are changing the scale
	# and add to the histogram the density function:
	+ geom_density(alpha=.2, fill="blue")

# geom_ribbon can be used to paint area under the curve
# check lab - week 2 - QDA Indep Practice to understand
# https://github.com/BAlmeidaS/brunel/blob/main/QDA/week-2/independent-practice/lab2-independent-practice-a-solution%202.Rmd
```

(1) - [scale functions](https://bookdown.dongzhuoer.com/hadley/ggplot2-book/scale-transformation)
(2) - [line functions](http://www.sthda.com/english/wiki/ggplot2-line-plot-quick-start-guide-r-software-and-data-visualization#create-line-plots-with-points)

# Validate (pkg)
Week 5 modern data
```R
# create a validator
rules <- validator(name_of_val = <some condition>,
				   okColB = is.ellement(colb, c("A", "B")),
				   NonNegColC = colC >= 0,
				   GreaterColD = colD >= ColC,
				   ...
				   )
# apply the rules
qual.check <- confront(df, rules)
summary(qual.check)
plot(qual.check)

# new rules can be added
new_rule <- validator(...)
rules <- rules + new_rule
```


# Dplyr (pkg)
Function to change the df - Week 5 modern data
```R
# arrange -> Sort
arrange(df, col_a)
arrange(df, -col_a) #reverse order

# filter -> "query"
filter(df, col_a == 7)

# mutate -> change or add new cols
mutate(df, new_col = col_a + col_b)

# rename -> rename a col
rename(df, col_a = new_name_for_col_a)

# sample_n -> random get some values
sample_n(df, 3)

# select -> get some only cols
select(df, c(col_b, col_c))
```

# Hmisc (pkg)
replace NA values on dfs
```R
df$col <- impute(df$col, median)
```

# libraries
```R
library(ggplot2)
library(dplyr)
library(glue)
library(RColorBrewer)
```
[color names of RColorBrewer](https://r-graph-gallery.com/42-colors-names.html)

```R
library(tidyverse)
library(tm)

library(validate)
library(Hmisc)

library(wordcloud)
library(wordcloud2)
```
