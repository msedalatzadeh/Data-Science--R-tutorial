# R - Language of Data Science: a Tutorial

In this repository, a useful, though short, tutorial of R is provided for beginners and those who are interested 
to learn about Data Science.

R is a statistical computing programming language. Creating and analyzing data is R could not be easier. For instant
to create a vector of strings in R you just need write 

```R 
MyVector <- c(1,2,3,4,5)
```

where `c` stands for combine and `<-` is assignment operator.

Data types in R is almost similar to any other programming language. There are 

- numerics (integer, single, double): `1`, `2.32`
- characters: `"HelloWorld"`
- logical: `True`, `False`
- complex: `(-1)^(1/2)`
- raw: contains bytes

Data structures in R is also similar to other programming languages but with extra feature. There are

- Vector: `c(1, 2, 3, 4, 5)`
- Matrix/array: `matrix(c(T, T, F, F, T, F), nrow = 2)` and `array(c( 1:24), c(4, 3, 2))`
- Data frame: `cbind(c(1, 2), c("a", "b"), c(True, False))`
- List: `list(True, c(1, 2), "a")`


## Installation
To install R, please visit [r-project.org](https://www.r-project.org/). You can also install R Studio to assist you in programming and visualizing the data. Download R Studio [here](https://rstudio.com/).


## Load, Summary, Plot on Built-in Data
There are some buit-in datasets in R that you can use to experiment on. To load a dataset use `library()`, to see the head (first row) of dataset use `head()`, to get a summary of stats use `summary()`, to plot the data simply use `plot()`. Run

```R
library(datasets)  # Load built-in datasets
head(iris)         # Show the first six lines of iris data
summary(iris)      # Summary statistics for iris data
plot(iris)         # Plot the dataset
```

The output is 

```cmd
> head(iris)
 Sepal.Length Sepal.Width Petal.Length Petal.Width Species
1          5.1         3.5          1.4         0.2  setosa
2          4.9         3.0          1.4         0.2  setosa
3          4.7         3.2          1.3         0.2  setosa
4          4.6         3.1          1.5         0.2  setosa
5          5.0         3.6          1.4         0.2  setosa
6          5.4         3.9          1.7         0.4  setosa

> summary(iris)
  Sepal.Length    Sepal.Width     Petal.Length    Petal.Width
 Min.   :4.300   Min.   :2.000   Min.   :1.000   Min.   :0.100
 1st Qu.:5.100   1st Qu.:2.800   1st Qu.:1.600   1st Qu.:0.300
 Median :5.800   Median :3.000   Median :4.350   Median :1.300
 Mean   :5.843   Mean   :3.057   Mean   :3.758   Mean   :1.199
 3rd Qu.:6.400   3rd Qu.:3.300   3rd Qu.:5.100   3rd Qu.:1.800
 Max.   :7.900   Max.   :4.400   Max.   :6.900   Max.   :2.500
       Species
 setosa    :50
 versicolor:50
 virginica :50

 > plot(iris) 
 ```

 ![](plots\iris.png)

 To clear a plot, write `dev.off()` and hit enter!

 ## Load Packages
 Use `pacman` for managing add-on packages. To install `pacman`, enter

 ```R
 install.packages("pacman")
 ```

 You can then choose the packages you need and load them as follows

 ```R
 pacman::p_load(pacman, dplyr, GGally, ggplot2, ggthemes, ggvis, httr, lubridate, plotly, rio, rmarkdown, shiny, stringr, tidyr)
  ```

  Make sure to clear all packages and datasets before exit

  ```R
p_unload(all)  # Clears all add-ons
detach("package:datasets", unload = TRUE)  # Clear data-base
```