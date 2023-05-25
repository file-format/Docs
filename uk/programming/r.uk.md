{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "файл", "розширення", "формат файлу", "бібліотеки R", "Посібник з програмування", "r приклад", "код R", "бібліотеки R", "Microsoft R" , "R code", "R language", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - файл мови програмування",
  "description":"Дізнайтеся про формат файлу R та API, які можуть створювати та відкривати файли R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Що таке файл R?

Файл із розширенням .r належить до мови програмування R. Ця мова призначена для статистичних обчислень і є популярною серед спільноти статистиків. Аналіз даних і розробка статистичного програмного забезпечення є двома основними категоріями, які виконуються цією мовою в галузі аналізу даних. Ще одна перевага використання цієї мови та програмного забезпечення полягає в тому, що він надає можливість створення статичних графіків, які допомагають створювати якісні графіки. Деякі додаткові пакети використовуються для динамічної та інтерактивної графіки.

Програмне забезпечення цієї мови містить загальну публічну ліцензію, тому його доступ є безкоштовним. Код R зазвичай пишеться на мовах високого рівня, таких як [C](/uk/programming/c/), а також на самому R. Програмне забезпечення передбачає інтерфейс командного рядка разом із наявністю інтерфейсів сторонніх розробників, таких як графічний інтерфейс користувача RStudio та Jupyter (інтерфейс ноутбука). У реалізації бібліотек R використовуються статистичні методи. Це також включає лінійне та нелінійне моделювання.


## Коротка історія ##

Ця мова є реалізацією семантики лексичного визначення поряд із мовою S. У 1976 році в Bell Labs Джон Чемберс розробив мову S. Навіть немає змін у більшій частині коду S-PLUS, коли він використовується мовою R. У 1995 році Мартін Мейхлер і його товариші створили мову R разом із вільним програмним забезпеченням під загальною публічною ліцензією.

Офіційне оголошення Comprehensive R Archive Network було зроблено 23 квітня 1997 року. У 2000 році була офіційно випущена версія 1.0, яка була першою стабільною бета-версією. Його перший випуск відбувся в 1995 році, тоді як CRAN (комплексна мережа архівів R) випускалася в наступні роки.

У 1997 році була сформована основна команда для подальшого розвитку мови після перших випусків. У наступні роки було випущено багато оновлень і модифікованих версій, які включали нові функції відповідно до сучасних операційних систем і технологій. Остання модифікація була представлена в травні 2021 року.


## Технічна специфікація ##

R є мовою інтерпретації, і для доступу до цієї мови потрібен інтерпретатор командного рядка. Обчислення, такі як сума, вводяться в команду promo, а результати відображаються після інтерпретації. Дані та код представлені через S-вирази. Інша специфікація цієї мови полягає в тому, що вона може працювати як інструментарій, який забезпечує можливість обчислення загальної матриці.

Для запуску та редагування коду R використовуються різні програми. Інтегровані середовища розробки, такі як Rattle GUI, RKWard, також доступні для запуску коду мови програмування R. Інше програмне забезпечення Microsoft, відоме як Microsoft R open, також доступне з сумісністю з дистрибутивом R для складних обчислень, таких як багатопотокові обчислення. R є однією з п’яти вибраних мов програмування в усьому світі, які складають API Apache Spark.

Мова R підтримує процедурне програмування разом із функціями. Однак, зокрема, для деяких функцій він підтримує ООП (об’єктно-орієнтоване програмування) разом із загальними функціями. Значення використовуються для передачі аргументів, якщо функції та їх оцінка відбуваються під час їх використання, що означає, що вони не оцінюються під час виклику функцій.

## Приклад формату файлу R ##

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

### Функція ###

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

### Моделювання даних

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

## Посилання ##

* [R - від Вікіпедії](https://en.wikipedia.org/wiki/R_(programming_language))



