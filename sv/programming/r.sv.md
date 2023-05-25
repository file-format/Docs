{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "fil", "tillägg", "filformat", "bibliotek av R", "Programmeringsguide", "r exempel", "kod för R", "bibliotek av R", "Microsoft R" , "R-kod", "R-språk", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Programmeringsspråkfil",
  "description":"Läs mer om R-filformat och API:er som kan skapa och öppna R-filer.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Vad är en R-fil?

En fil med filändelsen .r tillhör programmeringsspråket R. Detta språk är specificerat för statistisk beräkning och är populärt bland statistiker. Dataanalys och utveckling av statistisk programvara är två huvudkategorier som utförs av detta språk inom datautvinningsområdet. En annan fördel med att använda detta språk och programvara är att det ger möjlighet till statiska grafer som är användbara vid framställning av kvalitetsgrafer. Vissa ytterligare paket används för dynamisk och interaktiv grafik.

Programvaran för detta språk innehåller en allmän offentlig licens så att dess tillgänglighet är gratis. Koden för R är vanligtvis skriven på högnivåspråk som [C](/sv/programmering/c/) och R självt också. Mjukvaran innefattar ett kommandoradsgränssnitt tillsammans med tillgången till tredjepartsgränssnitt som grafiska användargränssnitt för RStudio och Jupyter (notebook-gränssnitt). Det finns statistiska tekniker som används i implementeringen av bibliotek av R. Det inkluderar också modellering som linjär och olinjär.


## Kortfattad bakgrund ##

Detta språk är en implementering av Semantics of lexical scoping tillsammans med S-språket. 1976 vid Bell Labs utvecklade John Chambers S-språket. Även det finns ingen ändring i mycket av koden för S-PLUS när den används i R-språk. 1995 gjorde Martin Maechler och hans följeslagare R-språket tillsammans med den fria programvaran under General Public-licensen.

Det officiella tillkännagivandet av Comprehensive R Archive Network gjordes den 23 april 1997. År 2000 släpptes version 1.0, som var den första stabila betaversionen, officiellt. Dess första release ägde rum 1995, medan CRAN (comprehensive R archive network) släpptes under senare år.

Ett kärnteam bildades 1997 för vidareutveckling av språket efter de första utgivningarna. Många uppdateringar och modifierade versioner släpptes under de senare åren och innebar nya funktioner enligt moderna operativsystem och teknik. Den senaste ändringen infördes i maj 2021.


## Teknisk specifikation ##

R är ett tolkspråk och en kommandoradstolk krävs för att få åtkomst till detta språk. Beräkningarna som summa skrivs in i kommandot promo och resultaten visas efter tolkning. Data och kod representeras genom S-uttryck. En annan specifikation för detta språk är att det kan användas som en verktygslåda som ger möjlighet till allmän matrisberäkning.

Olika applikationer används för att köra och redigera R-koden. Integrerade utvecklingsmiljöer som Rattle GUI, RKWard är också tillgängliga för att köra koden för programmeringsspråket R. En annan programvara från Microsoft känd som Microsoft R open är också tillgänglig med kompatibilitet med R-distribution för komplexa beräkningar som flertrådade beräkningar. R är ett av de fem utvalda programmeringsspråken runt om i världen som utgör Apache Spark API.

R-språket stöder procedurprogrammering tillsammans med funktionerna. Men särskilt för vissa funktioner stöder den OOP (objektorienterad programmering) tillsammans med de generiska funktionerna. Värden används för att skicka argument om funktioner och deras utvärdering sker när de används, vilket innebär att de inte utvärderas när funktioner anropas.

## R filformat exempel ##

### Syntax ###

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

## Referens ##

* [R - av Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



