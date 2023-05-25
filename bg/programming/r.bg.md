{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "файл", "разширение", "файлов формат", "библиотеки на R", "Ръководство за програмиране", "r пример", "код на R", "библиотеки на R", "Microsoft R" , "R код", "R език", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Езиков файл за програмиране",
  "description":"Научете за R файловия формат и API, които могат да създават и отварят R файлове.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Какво е R файл?

Файл с разширение .r принадлежи към езика за програмиране R. Този език е определен за статистически изчисления и е популярен сред общността на статистиците. Анализът на данни и разработването на статистически софтуер са две основни категории, извършвани от този език в областта на извличането на данни. Друго предимство на използването на този език и софтуер е, че той предоставя възможността за статични графики, които са полезни при създаването на качествени графики. Някои допълнителни пакети се използват за динамична и интерактивна графика.

Софтуерът на този език съдържа Общ публичен лиценз, така че достъпността му е безплатна. Кодът на R обикновено се пише на езици от високо ниво като [C](/bg/programming/c/) и самия R също. Софтуерът включва интерфейс на командния ред заедно с наличието на интерфейси на трети страни, като например графични потребителски интерфейси на RStudio и Jupyter (интерфейс за преносим компютър). Има статистически техники, използвани при внедряването на библиотеки на R. Той също така включва моделиране като линейно и нелинейно.


## Кратка история ##

Този език е реализация на семантиката на лексикалния обхват заедно с езика S. През 1976 г. в Bell Labs Джон Чембърс разработва езика S. Дори няма промяна в голяма част от кода на S-PLUS, когато се използва в R език. През 1995 г. Martin Maechler и неговите другари създават езика R заедно със свободния софтуер под общия публичен лиценз.

Официалното съобщение за Comprehensive R Archive Network беше направено на 23 април 1997 г. През 2000 г. версия 1. 0, която беше първата стабилна бета версия, беше официално пусната. Първото му издание се състоя през 1995 г., докато CRAN (цялостната R архивна мрежа) беше пуснат в следващите години.

През 1997 г. беше сформиран основен екип за по-нататъшното развитие на езика след първите версии. Много актуализации и модифицирани версии бяха пуснати през следващите години и включваха нови функции според съвременните операционни системи и технологии. Скорошната модификация беше въведена през май 2021 г.


## Техническа спецификация ##

R е интерпретиращ език и за достъп до този език е необходим интерпретатор на команден ред. Изчисленията като sum се въвеждат в командата promo и резултатите се показват след интерпретация. Данните и кодът са представени чрез S-изрази. Друга спецификация на този език е, че той може да се използва като кутия с инструменти, която предоставя възможността за общо матрично изчисление.

Използват се различни приложения за изпълнение и редактиране на R кода. Интегрирани среди за разработка като Rattle GUI, RKWard също са налични за изпълнение на кода на езика за програмиране R. Друг софтуер от Microsoft, известен като Microsoft R open, също е наличен със съвместимост с R дистрибуция за сложни изчисления, като например многонишкови изчисления. R е един от петте избрани езика за програмиране по света, които включват API на Apache Spark.

Езикът R поддържа процедурно програмиране заедно с функциите. Въпреки това, особено за някои функции, той поддържа OOP (обектно-ориентирано програмиране) заедно с общите функции. Стойностите се използват за предаване на аргументи, ако функциите и тяхната оценка се извършва, когато се използват, което означава, че не се оценяват, когато функциите се извикват.

## R пример за файлов формат ##

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

### Моделиране на данни

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

## Референция ##

* [R - от Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



