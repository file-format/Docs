{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "bestand", "extensie", "bestandsindeling", "bibliotheken van R", "Programmeergids", "r voorbeeld", "code van R", "bibliotheken van R", "Microsoft R" , "R-code", "R-taal", "RStudio"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Programmeertaalbestand",
  "description":"Meer informatie over de R-bestandsindeling en API's die R-bestanden kunnen maken en openen.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Wat is een R-bestand?

Een bestand met de extensie .r behoort tot de programmeertaal R. Deze taal is gespecificeerd voor statistische berekeningen en is populair onder de gemeenschap van statistici. Gegevensanalyse en ontwikkeling van statistische software zijn twee hoofdcategorieën die door deze taal worden uitgevoerd op het gebied van datamining. Een ander voordeel van het gebruik van deze taal en software is dat het de mogelijkheid biedt van statische grafieken die nuttig zijn bij de productie van kwaliteitsgrafieken. Voor de dynamische en interactieve graphics worden enkele aanvullende pakketten gebruikt.

De software van deze taal bevat een General Public License, zodat de beschikbaarheid ervan gratis is. De code van R is meestal geschreven in talen op hoog niveau zoals [C](/nl/programmering/c/) en R zelf ook. De software omvat een opdrachtregelinterface en de beschikbaarheid van interfaces van derden, zoals grafische gebruikersinterfaces van RStudio en Jupyter (notebookinterface). Er zijn statistische technieken die worden gebruikt bij de implementatie van bibliotheken van R. Het omvat ook modellering zoals lineair en niet-lineair.


## Korte geschiedenis ##

Deze taal is een implementatie van de semantiek van lexicale scoping samen met de S-taal. In 1976 ontwikkelde John Chambers bij Bell Labs de S-taal. Zelfs is er geen wijziging in veel van de code van S-PLUS wanneer deze in R-taal wordt gebruikt. In 1995 maakten Martin Maechler en zijn metgezellen de R-taal samen met de gratis software onder de algemene openbare licentie.

De officiële aankondiging van het Comprehensive R Archive Network werd gedaan op 23 april 1997. In 2000 werd versie 1. 0, de eerste stabiele bèta, officieel uitgebracht. De eerste release vond plaats in 1995, terwijl het CRAN (comprehensive R archive network) in latere jaren werd uitgebracht.

In 1997 werd een kernteam gevormd voor de verdere ontwikkeling van de taal na de eerste releases. Veel updates en gewijzigde versies werden in de latere jaren uitgebracht en bevatten nieuwe functies volgens moderne besturingssystemen en technologie. De recente wijziging werd in mei 2021 ingevoerd.


## Technische specificatie ##

R is een tolktaal en voor toegang tot deze taal is een opdrachtregeltolk vereist. De berekeningen zoals som worden getypt in het commando promo en de resultaten worden getoond na interpretatie. Gegevens en code worden weergegeven via S-expressies. Een andere specificatie van deze taal is dat deze kan worden gebruikt als een gereedschapskist die de mogelijkheid biedt voor algemene matrixberekening.

Er worden verschillende toepassingen gebruikt om de R-code uit te voeren en te bewerken. Geïntegreerde ontwikkelomgevingen zoals Rattle GUI, RKWard zijn ook beschikbaar om de code van de R-programmeertaal uit te voeren. Een andere software van Microsoft, bekend als Microsoft R open, is ook beschikbaar met compatibiliteit met R-distributie voor complexe berekeningen zoals multithreaded berekeningen. R is een van de vijf geselecteerde programmeertalen over de hele wereld waaruit de Apache Spark API bestaat.

R-taal ondersteunt procedureel programmeren samen met de functies. Vooral voor sommige functies ondersteunt het echter OOP (objectgeoriënteerd programmeren) samen met de generieke functies. Waarden worden gebruikt om argumenten door te geven als functies en hun evaluatie vindt plaats wanneer ze worden gebruikt, wat betekent dat ze niet worden geëvalueerd wanneer functies worden aangeroepen.

## R Voorbeeld bestandsindeling ##

### Syntaxis ###

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

### Functie ###

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

## Referentie ##

* [R - door Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



