{
  "date": "2021-09-06",
  "keywords": [
"R",
"failu",
"pagarinājumu",
"faila formātā",
"bibliotēkas R",
"Programmēšanas rokasgrāmata",
"r piemērs",
"kods R",
"bibliotēkas R",
"Microsoft R",
"R kods",
"R valoda",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - programmēšanas valodas fails",
  "description": "Uzziniet par R faila formātu un API, kas var izveidot un atvērt R failus.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--lvr"
}
},
  "lastmod": "2021-09-06"
}

## Kas ir R fails?

Fails ar paplašinājumu .r pieder programmēšanas valodai R. Šī valoda ir paredzēta statistikas skaitļošanai un ir populāra statistiķu aprindās. Datu analīze un statistikas programmatūras izstrāde ir divas galvenās kategorijas, ko šī valoda veic datu ieguves jomā. Vēl viena šīs valodas un programmatūras izmantošanas priekšrocība ir tā, ka tā nodrošina statisku grafiku iespēju, kas ir noderīgas kvalitatīvu grafiku veidošanā. Dažas papildu pakotnes tiek izmantotas dinamiskai un interaktīvai grafikai.

Šīs valodas programmatūra satur vispārējo publisko licenci, tāpēc tās pieejamība ir bezmaksas. R kods parasti tiek rakstīts augsta līmeņa valodās, piemēram, [C](/programming/c/), kā arī pats R. Programmatūra ietver komandrindas interfeisu, kā arī trešo pušu saskarņu pieejamību, piemēram, RStudio un Jupyter grafiskās lietotāja saskarnes (piezīmjdatora saskarne). Ir statistikas metodes, ko izmanto R bibliotēku ieviešanā. Tas ietver arī modelēšanu, piemēram, lineāro un nelineāro.


## Īsa vēsture ##

Šī valoda ir leksiskās tvēruma semantikas īstenošana kopā ar S valodu. 1976. gadā uzņēmumā Bell Labs Džons Čemberss izstrādāja S valodu. Pat liela daļa S-PLUS koda netiek mainīta, ja to lieto R valodā. 1995. gadā Martins Maechler un viņa pavadoņi izveidoja R valodu kopā ar bezmaksas programmatūru saskaņā ar vispārējo publisko licenci.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. 2000. gadā oficiāli tika izlaista versija 1.0, kas bija pirmā stabilā beta versija. Tā pirmā izlaišana notika 1995. gadā, savukārt CRAN (visaptverošais R arhīvu tīkls) tika izlaists vēlākos gados. 

1997. gadā tika izveidota pamata komanda valodas tālākai attīstībai pēc pirmajiem izlaidumiem. Vēlākajos gados tika izlaisti daudzi atjauninājumi un modificētas versijas, kas ietvēra jaunas funkcijas atbilstoši mūsdienu operētājsistēmām un tehnoloģijām. Nesenā modifikācija tika ieviesta 2021. gada maijā.


## Tehniskā specifikācija Nr.

R ir tulkošanas valoda, un, lai piekļūtu šai valodai, ir nepieciešams komandrindas tulks. Aprēķini, piemēram, summa, tiek ierakstīti komandas reklāmā, un rezultāti tiek parādīti pēc interpretācijas. Dati un kods tiek attēloti ar S-izteiksmēm. Vēl viena šīs valodas specifikācija ir tāda, ka to var izmantot kā rīku komplektu, kas nodrošina vispārīgas matricas aprēķināšanas iespējas.

R koda palaišanai un rediģēšanai tiek izmantotas dažādas lietojumprogrammas. Ir pieejamas arī integrētas izstrādes vides, piemēram, Rattle GUI, RKWard, lai palaistu R programmēšanas valodas kodu. Ir pieejama arī cita Microsoft programmatūra, kas pazīstama kā Microsoft R open ar saderību ar R izplatīšanu sarežģītiem aprēķiniem, piemēram, daudzpavedienu aprēķiniem. R ir viena no piecām izvēlētajām programmēšanas valodām visā pasaulē, kas ietver Apache Spark API.

R valoda atbalsta procesuālo programmēšanu kopā ar funkcijām. Tomēr īpaši dažām funkcijām tā atbalsta OOP (objektorientētā programmēšana) kopā ar vispārīgajām funkcijām. Vērtības tiek izmantotas, lai nodotu argumentus, ja funkcijas un to novērtēšana notiek, kad tās tiek izmantotas, kas nozīmē, ka tās netiek novērtētas, kad funkcijas tiek izsauktas.

## R faila formāta piemērs ##

### Sintakse ###

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

### Datu modelēšana

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

## Atsauce Nr.

* [R — Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))




