{
  "date" : "2021-09-06", 
  "keywords" :["R","文件","扩展","文件格式","R 库","编程指南","r 示例","R 代码","R 库","Microsoft R" , "R 代码", "R 语言", "RStudio"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - 编程语言文件",
  "description":"了解 R 文件格式和可以创建和打开 R 文件的 API。",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## 什么是 .R 文件？

扩展名为 .r 的文件属于编程语言 R。这种语言专门用于统计计算，在统计学家社区中很流行。数据分析和统计软件的开发是该语言在数据挖掘领域执行的两个主要类别。使用这种语言和软件的另一个优点是它提供了静态图的功能，这有助于生成高质量的图。一些附加包用于动态和交互式图形。

这种语言的软件包含一个通用公共许可证，因此它的可用性是免费的。 R 的代码通常是用高级语言编写的，例如 [C](/zh/programming/c/) 和 R 本身。该软件涉及命令行界面以及第三方界面的可用性，例如 RStudio 和 Jupyter 的图形用户界面（笔记本界面）。 R 库的实现中使用了统计技术。它还包括线性和非线性建模。


## 历史简介 ＃＃

这种语言是与 S 语言一起的词法范围语义的实现。 1976 年，John Chambers 在贝尔实验室开发了 S 语言。即使是在 R 语言中使用时，S-PLUS 的大部分代码也没有改变。 1995 年，Martin Maechler 和他的同伴制作了 R 语言以及通用公共许可下的自由软件。

综合 R 档案网络于 1997 年 4 月 23 日正式发布。2000 年，第一个稳定的 beta 版本 1.0 正式发布。它的第一次发布是在 1995 年，而 CRAN（综合 R 存档网络）是在晚年发布的。

1997 年成立了一个核心团队，在第一个版本之后进一步开发该语言。晚年发布了许多更新和修改版本，并根据现代操作系统和技术涉及新功能。最近的修改是在 2021 年 5 月推出的。


## 技术规格##

R 是一种解释语言，需要命令行解释器才能访问该语言。在命令 promo 中输入 sum 之类的计算，结果在解释后显示。数据和代码通过 S 表达式表示。这种语言的另一个规范是它可以作为一个工具箱来操作，提供通用矩阵计算的便利。

各种应用程序用于运行和编辑 R 代码。 Rattle GUI、RKWard 等集成开发环境也可用于运行 R 编程语言的代码。 Microsoft 的另一款名为 Microsoft R open 的软件也可与 R 发行版兼容，用于复杂计算，例如多线程计算。 R 是组成 Apache Spark API 的全球五种选定的编程语言之一。

R 语言与函数一起支持过程式编程。但是，特别是对于某些功能，它支持 OOP（面向对象编程）以及通用功能。如果函数及其评估在使用时发生，则值用于传递参数，这意味着在调用函数时不会评估它们。

## R 文件格式示例 ##

＃＃＃ 句法 ＃＃＃

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

＃＃＃ 功能 ＃＃＃

```{r}
# Declare function “f" with parameters “x", “y“
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

### 数据建模

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

## 参考 ＃＃

* [R - 维基百科](https://en.wikipedia.org/wiki/R_(programming_language))



