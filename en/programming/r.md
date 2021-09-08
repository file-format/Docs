{
  "date" : "2021-09-06", 
  "keywords" : [ "R", "file", "extension", "file format", "libraries of R", "Programming Guide", "r example", "code of R", "libraries of R", "Microsoft R", "R code", "R language", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "R - Programming Language File",
  "description":"Learn about R file format and APIs that can create and open R files.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-09-06"
}

## What is an R file?

A file with extension .r belongs to the programming language R. This language is specified for statistical computing and is popular among the community of statisticians. Data analysis and development of statistical software are two main categories performed by this language in the field of data mining. Another advantage of using this language and software is that it provides the facility of static graphs which are helpful in the production of quality graphs. Some additional packages are used for the dynamic and interactive graphics.

The software of this language contains a General Public License so its availability is free. The code of R is usually written in high-level languages such as [C](/programming/c/) and R itself also. The software involves a command-line interface along with the availability of third-party interfaces such as graphical user interfaces of RStudio and Jupyter (notebook interface). There are statistical techniques used in the implementation of libraries of R. It also includes modeling like linear and nonlinear.


## Brief History ##

This language is an implementation of  Semantics of lexical scoping along with the S language. In 1976 at Bell Labs, John Chambers developed the S language. Even there is not an alteration in much of the code of S-PLUS when being used in R language. In 1995, Martin Maechler and his companions made the R language along with the free software under the General public license. 

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. In 2000 the version 1. 0, which was the first stable beta, was officially released. Its first release took place in 1995, while the CRAN (comprehensive R archive network) was being released in later years. 

A core team was formed in 1997 for the further development of the language after the first releases. Many updates and modified versions were being released in the later years and involved new features according to modern operating systems and technology. The recent modification was introduced in May of 2021.


## Technichal Specification ##

R is an interpreting language and a command-line interpreter is required to access this language. The calculations like sum are typed in the command promo and the results are shown after interpretation. Data and code are represented through S-expressions. Another specification of this language is that it can be operated as a toolbox that provides the facility of general matrix calculation.

Various applications are used to run and edit the R code. Integrated development environments such as Rattle GUI, RKWard are also available to run the code of the R programming language. Another software by Microsoft known as Microsoft R open is also available with compatibility with R distribution for complex computations such as multithreaded computations. R is one of the five selected programming languages around the world which comprise Apache Spark API.

R language supports procedural programming along with the functions. However, for some functions particularly, it supports OOP (object-oriented programming) along with the generic functions. Values are used to pass arguments if functions and their evaluation takes place when they are used, which means they are not evaluated when functions are being called.

## R File Format Example ##

### Syntax ###

```{r}
> x <- 1:6 # Create a numeric vector in the current environment
> y <- x^2 # Create vector based on the values in x.
> print(y) # Print the vector’s contents.
[1]  1  4  9 16 25 36

> z <- x + y # Create a new vector that is the sum of x and y
> z # return the contents of z to the current environment.
[1]  2  6 12 20 30 42

> z_matrix <- matrix(z, nrow=3) # Create a new matrix that turns the vector z into a 3x2 matrix object
> z_matrix 
     [,1] [,2]
[1,]    2   20
[2,]    6   30
[3,]   12   42

> 2*t(z_matrix)-2 # Transpose the matrix, multiply every element by 2, subtract 2 from each element in the matrix, and return the results to the terminal.
     [,1] [,2] [,3]
[1,]    2   10   22
[2,]   38   58   82

> new_df <- data.frame(t(z_matrix), row.names=c('A','B')) # Create a new data.frame object that contains the data from a transposed z_matrix, with row names 'A' and 'B'
> names(new_df) <- c('X','Y','Z') # set the column names of new_df as X, Y, and Z.
> print(new_df)  #print the current results.
   X  Y  Z
A  2  6 12
B 20 30 42

> new_df$Z #output the Z column
[1] 12 42

> new_df$Z==new_df['Z'] && new_df[3]==new_df$Z # the data.frame column Z can be accessed using $Z, ['Z'], or [3] syntax, and the values are the same. 
[1] TRUE

> attributes(new_df) #print attributes information about the new_df object
$names
[1] "X" "Y" "Z"

$row.names
[1] "A" "B"

$class
[1] "data.frame"

> attributes(new_df)$row.names <- c('one','two') ## access and then change the row.names attribute; can also be done using rownames()
> new_df
     X  Y  Z
one  2  6 12
two 20 30 42
```

### Function ###

```{r}
# Declare function “f” with parameters “x”, “y“
# that returns a linear combination of x and y.
f <- function(x, y) {
  z <- 3 * x + 4 * y
  return(z) ## the return() function is optional here
}
```

```{r}
> f(1, 2)
[1] 11

> f(c(1,2,3), c(5,3,4))
[1] 23 18 25

> f(1:3, 4)
[1] 19 22 25
```

### Data Modeling

```{r}
> x <- 1:6 # Create x and y values
> y <- x^2  
> model <- lm(y ~ x)  # Linear regression model y = A + B * x.
> summary(model)  # Display an in-depth summary of the model.

Call:
lm(formula = y ~ x)

Residuals:
      1       2       3       4       5       6
 3.3333 -0.6667 -2.6667 -2.6667 -0.6667  3.3333

Coefficients:
            Estimate Std. Error t value Pr(>|t|)   
(Intercept)  -9.3333     2.8441  -3.282 0.030453 * 
x             7.0000     0.7303   9.585 0.000662 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 3.055 on 4 degrees of freedom
Multiple R-squared:  0.9583, Adjusted R-squared:  0.9478
F-statistic: 91.88 on 1 and 4 DF,  p-value: 0.000662

> par(mfrow = c(2, 2))  # Create a 2 by 2 layout for figures.
> plot(model)  # Output diagnostic plots of the model.
```

## Reference ##

* [R - by Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))


