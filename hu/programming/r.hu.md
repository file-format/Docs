{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "fájl", "kiterjesztés", "fájlformátum", "R könyvtárai", "Programozási útmutató", "r példa", "R kódja", "R könyvtárai", "Microsoft R" , "R kód", "R nyelv", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - programozási nyelvi fájl",
  "description":"További információ az R fájlformátumról és az R-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Mi az R fájl?

Az .r kiterjesztésű fájl az R programozási nyelvhez tartozik. Ez a nyelv statisztikai számításokhoz van megadva, és népszerű a statisztikusok közösségében. Az adatelemzés és a statisztikai szoftverek fejlesztése két fő kategória, amelyet ez a nyelv végez az adatbányászat területén. A nyelv és a szoftver használatának másik előnye, hogy lehetővé teszi a statikus gráfok készítését, amelyek segítenek minőségi grafikonok készítésében. Néhány további csomag a dinamikus és interaktív grafikához használatos.

Az ezen nyelvű szoftver általános nyilvános licencet tartalmaz, így elérhetősége ingyenes. Az R kódját általában magas szintű nyelveken írják, például [C](/hu/programing/c/) és magát az R-t is. A szoftver magában foglal egy parancssori felületet, valamint harmadik féltől származó interfészek elérhetőségét, például az RStudio és a Jupyter grafikus felhasználói felületeit (notebook felület). Léteznek statisztikai technikák, amelyeket az R könyvtárainak megvalósítására használnak. Ez magában foglalja a lineáris és nemlineáris modellezést is.


## Rövid története ##

Ez a nyelv a lexikális hatókör szemantikájának megvalósítása az S nyelv mellett. 1976-ban a Bell Labsnál John Chambers kifejlesztette az S nyelvet. Még az S-PLUS kódjának nagy részében sem történik változás, ha R nyelven használják. 1995-ben Martin Maechler és társai elkészítették az R nyelvet a szabad szoftverekkel együtt a General Public licenc alatt.

A Comprehensive R Archive Network hivatalos bejelentésére 1997. április 23-án került sor. 2000-ben hivatalosan is megjelent az 1.0 verzió, amely az első stabil béta volt. Első kiadására 1995-ben került sor, míg a CRAN-t (átfogó R archívum hálózat) a későbbi években adták ki.

1997-ben alakult egy törzscsapat a nyelv továbbfejlesztésére az első kiadások után. A későbbi években számos frissítés és módosított verzió jelent meg, amelyek a modern operációs rendszereknek és technológiának megfelelően új funkciókat tartalmaztak. A legutóbbi módosítást 2021 májusában vezették be.


## Műszaki specifikáció ##

Az R egy tolmácsnyelv, és egy parancssori tolmács szükséges a nyelv eléréséhez. A számításokat, például az összeget, a parancspromóban kell beírni, és az eredmények értelmezés után megjelennek. Az adatok és a kódok S-kifejezéseken keresztül jelennek meg. Ennek a nyelvnek egy másik specifikációja, hogy olyan eszköztárként üzemeltethető, amely lehetővé teszi az általános mátrixszámítást.

Különféle alkalmazásokat használnak az R-kód futtatására és szerkesztésére. Integrált fejlesztői környezetek, például Rattle GUI, RKWard is elérhetők az R programozási nyelv kódjának futtatásához. A Microsoft egy másik szoftvere, az úgynevezett Microsoft R open szintén elérhető az R disztribúcióval kompatibilis összetett számításokhoz, például többszálú számításokhoz. Az R egyike a világ öt kiválasztott programozási nyelvének, amely az Apache Spark API-t tartalmazza.

Az R nyelv támogatja az eljárási programozást a funkciókkal együtt. Azonban bizonyos funkciók esetében különösen támogatja az OOP-t (objektum-orientált programozás) az általános funkciók mellett. Az értékek az argumentumok átadására szolgálnak, ha függvények, és kiértékelésük megtörténik, amikor használatuk történik, ami azt jelenti, hogy a függvények meghívásakor nem kerülnek kiértékelésre.

## R fájlformátum példa ##

### Szintaxis ###

```{r}
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

### Funkció ###

```{r}
# Declare function “f” with parameters “x”, “y“
# that returns a linear combination of x and y.
f <- function(x, y) {
  z <- 3 * x + 4 * y
  return(z) ## the return() function is optional here
}
```

```{r}
> f(1, 2)
[1] 11

> f(c(1,2,3), c(5,3,4))
[1] 23 18 25

> f(1:3, 4)
[1] 19 22 25
```

### Adatmodellezés

```{r}
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

## Hivatkozási szám

* [R – a Wikipedia által](https://en.wikipedia.org/wiki/R_(programozási_nyelv))



