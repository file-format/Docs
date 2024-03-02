{
  "date": "2021-09-06",
  "keywords": [
"R",
"tiedosto",
"laajennus",
"tiedosto muoto",
"R:n kirjastot",
"Ohjelmointiopas",
"r esimerkki",
"koodi R",
"R:n kirjastot",
"Microsoft R",
"R-koodi",
"R kieli",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - Ohjelmointikielitiedosto",
  "description": "Opi R-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata R-tiedostoja.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fir"
}
},
  "lastmod": "2021-09-06"
}

## Mikä on R-tiedosto?

Tiedosto, jonka tunniste on .r, kuuluu ohjelmointikieleen R. Tämä kieli on tarkoitettu tilastolaskemiseen ja on suosittu tilastotieteilijöiden keskuudessa. Tietojen analysointi ja tilastoohjelmistojen kehittäminen ovat tämän kielen kaksi pääluokkaa tiedon louhinnan alalla. Toinen tämän kielen ja ohjelmiston käytön etu on, että se tarjoaa staattisten kuvaajien mahdollisuuden, jotka ovat hyödyllisiä laadukkaiden kaavioiden tuotannossa. Joitakin lisäpaketteja käytetään dynaamiseen ja interaktiiviseen grafiikkaan.

Tämän kielen ohjelmisto sisältää yleisen julkisen lisenssin, joten sen saatavuus on ilmainen. R:n koodi kirjoitetaan yleensä korkean tason kielillä, kuten {{HYPERLINKKI}} ja myös itse R. Ohjelmisto sisältää komentorivikäyttöliittymän sekä kolmansien osapuolien käyttöliittymien, kuten RStudion ja Jupyterin graafisten käyttöliittymien (kannettavan tietokoneen käyttöliittymä), saatavuuden. R:n kirjastojen toteutuksessa käytetään tilastollisia tekniikoita. Se sisältää myös mallinnuksen, kuten lineaarisen ja epälineaarisen.


## Lyhyt historia ##

Tämä kieli on leksikaalisen laajuuden semantiikan toteutus yhdessä S-kielen kanssa. Vuonna 1976 Bell Labsissa John Chambers kehitti S-kielen. Edes S-PLUS:n koodin suuressa osassa ei ole muutosta, kun sitä käytetään R-kielellä. Vuonna 1995 Martin Maechler ja hänen toverinsa loivat R-kielen sekä ilmaisen ohjelmiston yleisen julkisen lisenssin alaisena.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. Vuonna 2000 versio 1. 0, joka oli ensimmäinen vakaa beta, julkaistiin virallisesti. Sen ensimmäinen julkaisu tapahtui vuonna 1995, kun taas CRAN (comprehensive R archive network) julkaistiin myöhempinä vuosina. 

Vuonna 1997 perustettiin ydintiimi kielen jatkokehitystä varten ensimmäisten julkaisujen jälkeen. Monia päivityksiä ja muokattuja versioita julkaistiin myöhempinä vuosina, ja ne sisälsivät uusia ominaisuuksia nykyaikaisten käyttöjärjestelmien ja tekniikan mukaisesti. Tuore muutos otettiin käyttöön toukokuussa 2021.


## Tekniset tiedot ##

R on tulkkauskieli, ja tämän kielen käyttämiseen tarvitaan komentorivitulkki. Laskelmat, kuten summa, kirjoitetaan komentopromoon ja tulokset näytetään tulkinnan jälkeen. Data ja koodi esitetään S-lausekkeiden avulla. Toinen tämän kielen spesifikaatio on, että sitä voidaan käyttää työkalupakkina, joka tarjoaa mahdollisuuden yleiseen matriisilaskentaan.

R-koodin suorittamiseen ja muokkaamiseen käytetään erilaisia sovelluksia. Integroidut kehitysympäristöt, kuten Rattle GUI, RKWard, ovat myös saatavilla R-ohjelmointikielen koodin suorittamiseen. Toinen Microsoftin ohjelmisto, joka tunnetaan nimellä Microsoft R open, on myös saatavilla R-jakelun kanssa yhteensopivaksi monimutkaisiin laskelmiin, kuten monisäikeisiin laskelmiin. R on yksi viidestä valitusta ohjelmointikielestä ympäri maailmaa, jotka sisältävät Apache Spark API:n.

R-kieli tukee menettelyohjelmointia toimintojen ohella. Erityisesti joidenkin toimintojen osalta se tukee kuitenkin OOP:ta (olio-ohjelmointia) yleisten toimintojen ohella. Arvoja käytetään argumenttien välittämiseen, jos funktioita ja niiden arviointi tapahtuu, kun niitä käytetään, mikä tarkoittaa, että niitä ei arvioida, kun funktioita kutsutaan.

## R-tiedostomuodon esimerkki ##

### Syntaksi ###

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

### Toiminto ###

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

### Tietomallinnus

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

## Viite ##

* [R - by Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))
