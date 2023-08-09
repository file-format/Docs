{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "fișier", "extensie", "format fișier", "biblioteci ale lui R", "Ghid de programare", "exemplu r", "codul lui R", "biblioteci ale lui R", "Microsoft R" , "Cod R", "Limba R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Fișier limbaj de programare",
  "description":"Aflați despre formatul de fișier R și despre API-urile care pot crea și deschide fișiere R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Ce este un fișier R?

Un fișier cu extensia .r aparține limbajului de programare R. Acest limbaj este specificat pentru calculul statistic și este popular în rândul comunității statisticienilor. Analiza datelor și dezvoltarea de software statistic sunt două categorii principale realizate de acest limbaj în domeniul minării de date. Un alt avantaj al utilizării acestui limbaj și software este că oferă posibilitatea de a crea grafice statice care sunt utile în producerea de grafice de calitate. Unele pachete suplimentare sunt folosite pentru grafica dinamică și interactivă.

Software-ul acestui limbaj conține o licență publică generală, astfel încât disponibilitatea sa este gratuită. Codul lui R este de obicei scris în limbaje de nivel înalt, cum ar fi [C](/ro/programming/c/) și R însuși, de asemenea. Software-ul implică o interfață de linie de comandă împreună cu disponibilitatea interfețelor terțe, cum ar fi interfețele grafice cu utilizatorul RStudio și Jupyter (interfață pentru notebook). Există tehnici statistice utilizate în implementarea bibliotecilor lui R. Include, de asemenea, modelarea liniară și neliniară.


## Scurt istoric ##

Acest limbaj este o implementare a Semanticii delimitării lexicale împreună cu limbajul S. În 1976, la Bell Labs, John Chambers a dezvoltat limbajul S. Chiar și nu există o modificare în mare parte a codului S-PLUS atunci când este utilizat în limbajul R. În 1995, Martin Maechler și însoțitorii săi au creat limbajul R împreună cu software-ul liber sub licența publică generală.

Anunțul oficial al Rețelei Comprehensive R Archive a fost făcut pe 23 aprilie 1997. În 2000, versiunea 1. 0, care a fost prima beta stabilă, a fost lansată oficial. Prima sa lansare a avut loc în 1995, în timp ce CRAN (comprehensive R archive network) a fost lansat în anii următori.

O echipă de bază a fost formată în 1997 pentru dezvoltarea ulterioară a limbajului după primele lansări. Multe actualizări și versiuni modificate au fost lansate în ultimii ani și au implicat noi funcții conform sistemelor de operare și tehnologiei moderne. Modificarea recentă a fost introdusă în mai 2021.


## Specificatii tehnice ##

R este un limbaj de interpretare și este necesar un interpret de linie de comandă pentru a accesa acest limbaj. Calculele precum suma sunt introduse în promo de comandă, iar rezultatele sunt afișate după interpretare. Datele și codul sunt reprezentate prin expresii S. O altă specificație a acestui limbaj este că poate fi operat ca o cutie de instrumente care oferă facilitatea calculului matriceal general.

Sunt folosite diverse aplicații pentru a rula și edita codul R. Mediile de dezvoltare integrate, cum ar fi Rattle GUI, RKWard sunt, de asemenea, disponibile pentru a rula codul limbajului de programare R. Un alt software de la Microsoft cunoscut sub numele de Microsoft R open este, de asemenea, disponibil cu compatibilitate cu distribuția R pentru calcule complexe, cum ar fi calcule multithreaded. R este unul dintre cele cinci limbaje de programare selectate din întreaga lume care cuprind Apache Spark API.

Limbajul R acceptă programarea procedurală împreună cu funcțiile. Cu toate acestea, în special pentru unele funcții, acceptă OOP (programare orientată pe obiecte) împreună cu funcțiile generice. Valorile sunt folosite pentru a transmite argumente dacă funcțiile și evaluarea lor are loc atunci când sunt utilizate, ceea ce înseamnă că nu sunt evaluate atunci când funcțiile sunt apelate.

## Exemplu de format de fișier R ##

### Sintaxă ###

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

### Funcția ###

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

### Modelarea datelor

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

## Referință ##

* [R - de Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



