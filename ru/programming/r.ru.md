{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "файл", "расширение", "формат файла", "библиотеки R", "Руководство по программированию", "пример r", "код R", "библиотеки R", "Microsoft R" , "Код R", "Язык R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R — файл языка программирования",
  "description":"Узнайте о формате файлов R и API-интерфейсах, которые могут создавать и открывать файлы R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## .R вариант №

Файл с расширением .r принадлежит языку программирования R. Этот язык предназначен для статистических вычислений и популярен в сообществе статистиков. Анализ данных и разработка статистического программного обеспечения - две основные категории, выполняемые этим языком в области интеллектуального анализа данных. Еще одно преимущество использования этого языка и программного обеспечения заключается в том, что они предоставляют возможность построения статических графиков, которые помогают создавать качественные графики. Некоторые дополнительные пакеты используются для динамической и интерактивной графики.

Программное обеспечение этого языка содержит Стандартную общественную лицензию, поэтому его доступность бесплатна. Код R обычно пишется на языках высокого уровня, таких как [C](/ru/programming/c/), а также сам R. Программное обеспечение включает в себя интерфейс командной строки, а также наличие сторонних интерфейсов, таких как графические пользовательские интерфейсы RStudio и Jupyter (интерфейс ноутбука). Существуют статистические методы, используемые при реализации библиотек R. Сюда также входит моделирование, как линейное, так и нелинейное.


## Краткая история ##

Этот язык является реализацией семантики лексической области видимости наряду с языком S. В 1976 году в Bell Labs Джон Чемберс разработал язык S. Даже большая часть кода S-PLUS не меняется при использовании на языке R. В 1995 году Мартин Махлер и его товарищи создали язык R вместе со свободным программным обеспечением под Общедоступной лицензией.

Официальное объявление о создании сети Comprehensive R Archive Network было сделано 23 апреля 1997 года. В 2000 году была официально выпущена версия 1.0, ставшая первой стабильной бета-версией. Его первый выпуск состоялся в 1995 году, а в последующие годы была выпущена CRAN (комплексная сеть архивов R).

Основная команда была сформирована в 1997 году для дальнейшего развития языка после первых выпусков. В последующие годы было выпущено множество обновлений и модифицированных версий, которые включали новые функции в соответствии с современными операционными системами и технологиями. Последняя модификация была представлена в мае 2021 года.


## Техническая спецификация ##

R является интерпретирующим языком, и для доступа к этому языку требуется интерпретатор командной строки. Вычисления типа sum вводятся в команду promo, а результаты отображаются после интерпретации. Данные и код представлены через S-выражения. Другая особенность этого языка заключается в том, что его можно использовать как набор инструментов, обеспечивающий возможность вычисления общих матриц.

Для запуска и редактирования кода R используются различные приложения. Интегрированные среды разработки, такие как Rattle GUI, RKWard, также доступны для запуска кода языка программирования R. Другое программное обеспечение Microsoft, известное как Microsoft R open, также доступно с совместимостью с дистрибутивом R для сложных вычислений, таких как многопоточные вычисления. R — один из пяти избранных языков программирования по всему миру, которые составляют Apache Spark API.

Язык R поддерживает процедурное программирование наряду с функциями. Однако, в частности, для некоторых функций он поддерживает ООП (объектно-ориентированное программирование) наряду с общими функциями. Значения используются для передачи аргументов, если функции и их оценка происходят при их использовании, что означает, что они не оцениваются при вызове функций.

## Пример формата файла R ##

### Синтаксис ###

```
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

### Функция ###

```
# Declare function “f” with parameters “x”, “y“
# that returns a linear combination of x and y.
f <- function(x, y) {
  z <- 3 * x + 4 * y
  return(z) ## the return() function is optional here
}
```

```
> f(1, 2)
[1] 11

> f(c(1,2,3), c(5,3,4))
[1] 23 18 25

> f(1:3, 4)
[1] 19 22 25
```

### Моделирование данных

```
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

## Ссылка ##

* [R - по Википедии](https://en.wikipedia.org/wiki/R_(programming_language))



