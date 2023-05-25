{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "Datei", "Erweiterung", "Dateiformat", "Bibliotheken von R", "Programmierhandbuch", "R-Beispiel", "Code von R", "Bibliotheken von R", "Microsoft R" , "R-Code", "R-Sprache", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Programmiersprachendatei",
  "description":"Erfahren Sie mehr über das R-Dateiformat und APIs, die R-Dateien erstellen und öffnen können.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Was ist eine R-Datei?

Eine Datei mit der Erweiterung .r gehört zur Programmiersprache R. Diese Sprache ist für statistische Berechnungen spezifiziert und in der Gemeinschaft der Statistiker beliebt. Datenanalyse und Entwicklung statistischer Software sind zwei Hauptkategorien, die von dieser Sprache im Bereich Data Mining durchgeführt werden. Ein weiterer Vorteil der Verwendung dieser Sprache und Software besteht darin, dass sie die Möglichkeit statischer Diagramme bietet, die bei der Erstellung hochwertiger Diagramme hilfreich sind. Einige zusätzliche Pakete werden für die dynamischen und interaktiven Grafiken verwendet.

Die Software dieser Sprache enthält eine General Public License, sodass ihre Verfügbarkeit kostenlos ist. Der Code von R ist normalerweise in Hochsprachen wie [C](/de/programming/c/) und R selbst auch geschrieben. Die Software umfasst eine Befehlszeilenschnittstelle sowie die Verfügbarkeit von Schnittstellen von Drittanbietern, wie z. B. grafische Benutzeroberflächen von RStudio und Jupyter (Notebook-Schnittstelle). Es gibt statistische Techniken, die bei der Implementierung von Bibliotheken von R verwendet werden. Es umfasst auch Modellierung wie lineare und nichtlineare.


## Kurze Geschichte ##

Diese Sprache ist eine Implementierung der Semantik des lexikalischen Bereichs zusammen mit der S-Sprache. 1976 entwickelte John Chambers in den Bell Labs die S-Sprache. Auch bei der Verwendung in der R-Sprache gibt es keine großen Änderungen im Code von S-PLUS. 1995 stellten Martin Maechler und seine Mitstreiter die Sprache R zusammen mit der freien Software unter die General Public License.

Die offizielle Ankündigung des Comprehensive R Archive Network erfolgte am 23. April 1997. Im Jahr 2000 wurde die Version 1.0, die erste stabile Beta, offiziell veröffentlicht. Seine erste Veröffentlichung fand 1995 statt, während das CRAN (Comprehensive R Archive Network) in späteren Jahren veröffentlicht wurde.

Für die Weiterentwicklung der Sprache nach den ersten Releases wurde 1997 ein Kernteam gebildet. Viele Updates und modifizierte Versionen wurden in den späteren Jahren veröffentlicht und beinhalteten neue Funktionen gemäß modernen Betriebssystemen und Technologien. Die letzte Änderung wurde im Mai 2021 eingeführt.


## Technische Spezifikation ##

R ist eine interpretierende Sprache, und für den Zugriff auf diese Sprache ist ein Befehlszeileninterpreter erforderlich. Die Berechnungen wie Summe werden in den Befehl Promo eingegeben und die Ergebnisse werden nach der Interpretation angezeigt. Daten und Code werden durch S-Ausdrücke dargestellt. Eine weitere Besonderheit dieser Sprache ist, dass sie als Werkzeugkasten betrieben werden kann, der die Möglichkeit der allgemeinen Matrizenberechnung bietet.

Verschiedene Anwendungen werden verwendet, um den R-Code auszuführen und zu bearbeiten. Integrierte Entwicklungsumgebungen wie Rattle GUI, RKWard sind ebenfalls verfügbar, um den Code der Programmiersprache R auszuführen. Eine andere Software von Microsoft, die als Microsoft R open bekannt ist, ist ebenfalls mit Kompatibilität mit der R-Distribution für komplexe Berechnungen wie Multithread-Berechnungen verfügbar. R ist eine der fünf ausgewählten Programmiersprachen auf der ganzen Welt, die die Apache Spark-API umfassen.

Die R-Sprache unterstützt die prozedurale Programmierung zusammen mit den Funktionen. Für einige Funktionen unterstützt es jedoch OOP (objektorientierte Programmierung) zusammen mit den generischen Funktionen. Werte werden verwendet, um Argumente zu übergeben, wenn Funktionen verwendet werden, und ihre Auswertung erfolgt, wenn sie verwendet werden, was bedeutet, dass sie nicht ausgewertet werden, wenn Funktionen aufgerufen werden.

## Beispiel für ein R-Dateiformat ##

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

### Datenmodellierung

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

## Bezug ##

* [R - von Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



