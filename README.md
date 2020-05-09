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
