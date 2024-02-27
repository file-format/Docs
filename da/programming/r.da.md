{
  "date": "2021-09-06",
  "keywords": [
"R",
"fil",
"udvidelse",
"filformat",
"biblioteker af R",
"Programmeringsvejledning",
"r eksempel",
"kode for R",
"biblioteker af R",
"Microsoft R",
"R-kode",
"R sprog",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - Programmeringssprogsfil",
  "description": "Lær om R-filformat og API'er, der kan oprette og åbne R-filer.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--dar"
}
},
  "lastmod": "2021-09-06"
}

## Hvad er en R-fil?

En fil med endelsen .r tilhører programmeringssproget R. Dette sprog er specificeret til statistisk databehandling og er populært blandt statistikere. Dataanalyse og udvikling af statistisk software er to hovedkategorier udført af dette sprog inden for data mining. En anden fordel ved at bruge dette sprog og software er, at det giver mulighed for statiske grafer, som er nyttige i produktionen af kvalitetsgrafer. Nogle ekstra pakker bruges til den dynamiske og interaktive grafik.

Softwaren på dette sprog indeholder en General Public License, så tilgængeligheden er gratis. Koden til R er normalt skrevet på højt niveau sprog såsom [C](/programming/c/) og R selv også. Softwaren involverer en kommandolinjegrænseflade sammen med tilgængeligheden af tredjepartsgrænseflader såsom grafiske brugergrænseflader i RStudio og Jupyter (notebook-grænseflade). Der er statistiske teknikker, der bruges i implementeringen af biblioteker af R. Det omfatter også modellering som lineær og ikke-lineær.


## Kort historie ##

Dette sprog er en implementering af Semantics of lexical scoping sammen med S-sproget. I 1976 på Bell Labs udviklede John Chambers S-sproget. Selv er der ikke en ændring i meget af koden til S-PLUS, når den bruges i R-sprog. I 1995 lavede Martin Maechler og hans ledsagere R-sproget sammen med den gratis software under General public-licensen.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. I 2000 blev version 1.0, som var den første stabile beta, officielt udgivet. Dens første udgivelse fandt sted i 1995, mens CRAN (comprehensive R archive network) blev udgivet i senere år. 

Et kerneteam blev dannet i 1997 til videreudvikling af sproget efter de første udgivelser. Mange opdateringer og ændrede versioner blev frigivet i de senere år og involverede nye funktioner i henhold til moderne operativsystemer og teknologi. Den seneste ændring blev introduceret i maj 2021.


## Teknisk specifikation ##

R er et tolkesprog, og der kræves en kommandolinjetolk for at få adgang til dette sprog. Beregningerne som sum er indtastet i kommandoen promo og resultaterne vises efter fortolkning. Data og kode er repræsenteret gennem S-udtryk. En anden specifikation af dette sprog er, at det kan betjenes som en værktøjskasse, der giver mulighed for generel matrixberegning.

Forskellige applikationer bruges til at køre og redigere R-koden. Integrerede udviklingsmiljøer såsom Rattle GUI, RKWard er også tilgængelige til at køre koden til R-programmeringssproget. En anden software fra Microsoft kendt som Microsoft R open er også tilgængelig med kompatibilitet med R-distribution til komplekse beregninger såsom multitrådede beregninger. R er et af de fem udvalgte programmeringssprog rundt om i verden, som omfatter Apache Spark API.

R-sproget understøtter proceduremæssig programmering sammen med funktionerne. Men især for nogle funktioner understøtter den OOP (objektorienteret programmering) sammen med de generiske funktioner. Værdier bruges til at sende argumenter, hvis funktioner og deres evaluering finder sted, når de bruges, hvilket betyder, at de ikke evalueres, når funktioner kaldes.

## R filformat eksempel ##

### Syntaks ###

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

### Funktion ###

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

### Datamodellering

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

## Reference ##

* [R - af Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))




