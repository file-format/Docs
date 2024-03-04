{
  "date": "2021-09-06",
  "keywords": [
"R",
"failą",
"pratęsimas",
"Dokumento formatas",
"bibliotekos R",
"Programavimo vadovas",
"r pavyzdys",
"kodas R",
"bibliotekos R",
"Microsoft R",
"R kodas",
"R kalba",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R – programavimo kalbos failas",
  "description": "Sužinokite apie R failo formatą ir API, kurios gali kurti ir atidaryti R failus.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--ltr"
}
},
  "lastmod": "2021-09-06"
}

## Kas yra R failas?

Failas su plėtiniu .r priklauso programavimo kalbai R. Ši kalba skirta statistiniam skaičiavimui ir yra populiari tarp statistikų bendruomenės. Duomenų analizė ir statistinės programinės įrangos kūrimas yra dvi pagrindinės kategorijos, kurias ši kalba atlieka duomenų gavybos srityje. Kitas šios kalbos ir programinės įrangos naudojimo privalumas yra tai, kad ji suteikia galimybę kurti statinius grafikus, kurie yra naudingi kuriant kokybiškus grafikus. Kai kurie papildomi paketai naudojami dinaminei ir interaktyviai grafikai.

Šios kalbos programinė įranga turi bendrąją viešąją licenciją, todėl jos prieinamumas yra nemokamas. R kodas paprastai rašomas aukšto lygio kalbomis, tokiomis kaip [C](/programming/c/), taip pat pats R. Programinė įranga apima komandinės eilutės sąsają ir trečiųjų šalių sąsajas, pvz., RStudio ir Jupyter grafines vartotojo sąsajas (nešiojamojo kompiuterio sąsaja). Yra statistinių metodų, naudojamų diegiant R bibliotekas. Tai taip pat apima linijinį ir netiesinį modeliavimą.


## Trumpa istorija ##

Ši kalba yra leksinės apimties semantikos įgyvendinimas kartu su S kalba. 1976 m. Bell Labs Johnas Chambersas sukūrė S kalbą. Netgi didelė dalis S-PLUS kodo nesikeičia, kai naudojamas R kalba. 1995 m. Martinas Maechleris ir jo bendražygiai sukūrė R kalbą kartu su nemokama programine įranga pagal bendrąją viešąją licenciją.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. 2000 m. buvo oficialiai išleista 1.0 versija, kuri buvo pirmoji stabili beta versija. Pirmasis jo išleidimas įvyko 1995 m., o CRAN (išsamus R archyvų tinklas) buvo išleistas vėlesniais metais. 

1997 m. buvo suformuota pagrindinė komanda, skirta toliau plėtoti kalbą po pirmųjų leidimų. Daug atnaujinimų ir modifikuotų versijų buvo išleista vėlesniais metais ir įtraukė naujas funkcijas pagal šiuolaikines operacines sistemas ir technologijas. Naujausias pakeitimas buvo pristatytas 2021 m. gegužės mėn.


## Techninė specifikacija Nr.

R yra vertimo kalba, o norint pasiekti šią kalbą reikalingas komandų eilutės vertėjas. Skaičiavimai, tokie kaip suma, įvedami į komandų reklamą, o rezultatai rodomi po interpretacijos. Duomenys ir kodas pateikiami naudojant S išraiškas. Kita šios kalbos specifikacija yra ta, kad ji gali būti naudojama kaip įrankių rinkinys, suteikiantis bendrosios matricos skaičiavimo galimybę.

R kodui paleisti ir redaguoti naudojamos įvairios programos. R programavimo kalbos kodui paleisti taip pat yra integruotos kūrimo aplinkos, tokios kaip Rattle GUI, RKWard. Kita Microsoft programinė įranga, žinoma kaip Microsoft R open, taip pat yra suderinama su R paskirstymu sudėtingiems skaičiavimams, pvz., daugiasriegiams skaičiavimams. R yra viena iš penkių pasirinktų programavimo kalbų visame pasaulyje, kurią sudaro Apache Spark API.

R kalba palaiko procedūrinį programavimą kartu su funkcijomis. Tačiau, ypač kai kurioms funkcijoms, ji palaiko OOP (objektinį programavimą) kartu su bendromis funkcijomis. Reikšmės naudojamos perduoti argumentams, jei funkcijos ir jų įvertinimas vyksta, kai jos naudojamos, o tai reiškia, kad jos neįvertinamos, kai iškviečiamos funkcijos.

## R failo formato pavyzdys ##

### Sintaksė ###

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

### Funkcija ###

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

### Duomenų modeliavimas

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

## Nuoroda ##

* [R – pateikė Vikipedija](https://en.wikipedia.org/wiki/R_(programing_language))




