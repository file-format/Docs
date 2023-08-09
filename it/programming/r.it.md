{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "file", "estensione", "formato file", "librerie di R", "Guida alla programmazione", "r esempio", "codice di R", "librerie di R", "Microsoft R" , "Codice R", "Lingua R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - File del linguaggio di programmazione",
  "description":"Scopri il formato di file R e le API che possono creare e aprire file R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Che cos'è un file R?

Un file con estensione .r appartiene al linguaggio di programmazione R. Questo linguaggio è specifico per il calcolo statistico ed è popolare tra la comunità degli statistici. L'analisi dei dati e lo sviluppo di software statistici sono due categorie principali eseguite da questo linguaggio nel campo del data mining. Un altro vantaggio dell'utilizzo di questo linguaggio e software è che fornisce la possibilità di grafici statici che sono utili nella produzione di grafici di qualità. Alcuni pacchetti aggiuntivi vengono utilizzati per la grafica dinamica e interattiva.

Il software di questa lingua contiene una General Public License, quindi la sua disponibilità è gratuita. Il codice di R è solitamente scritto in linguaggi di alto livello come [C](/it/programmazione/c/) e anche R stesso. Il software prevede un'interfaccia a riga di comando insieme alla disponibilità di interfacce di terze parti come le interfacce utente grafiche di RStudio e Jupyter (interfaccia per notebook). Esistono tecniche statistiche utilizzate nell'implementazione delle librerie di R. Include anche modelli come lineare e non lineare.


## Breve storia ##

Questo linguaggio è un'implementazione della semantica dell'ambito lessicale insieme al linguaggio S. Nel 1976 presso i Bell Labs, John Chambers sviluppò il linguaggio S. Anche non c'è un'alterazione in gran parte del codice di S-PLUS quando viene utilizzato nel linguaggio R. Nel 1995, Martin Maechler e i suoi compagni realizzarono il linguaggio R insieme al software libero sotto licenza General public.

L'annuncio ufficiale del Comprehensive R Archive Network è stato fatto il 23 aprile 1997. Nel 2000 è stata rilasciata ufficialmente la versione 1.0, che è stata la prima beta stabile. Il suo primo rilascio ha avuto luogo nel 1995, mentre il CRAN (rete di archivio R completo) è stato rilasciato negli anni successivi.

Un nucleo centrale è stato formato nel 1997 per l'ulteriore sviluppo del linguaggio dopo i primi rilasci. Molti aggiornamenti e versioni modificate sono stati rilasciati negli ultimi anni e hanno comportato nuove funzionalità in base ai moderni sistemi operativi e tecnologie. La recente modifica è stata introdotta nel maggio del 2021.


## Specifiche tecniche ##

R è una lingua di interpretazione e per accedere a questa lingua è necessario un interprete della riga di comando. I calcoli come la somma sono digitati nel comando promo e i risultati sono mostrati dopo l'interpretazione. I dati e il codice sono rappresentati tramite espressioni S. Un'altra specifica di questo linguaggio è che può essere utilizzato come una cassetta degli attrezzi che fornisce la facilità di calcolo generale della matrice.

Per eseguire e modificare il codice R vengono utilizzate varie applicazioni. Sono inoltre disponibili ambienti di sviluppo integrati come Rattle GUI, RKWard per eseguire il codice del linguaggio di programmazione R. Un altro software di Microsoft noto come Microsoft R open è disponibile anche con compatibilità con la distribuzione R per calcoli complessi come i calcoli multithread. R è uno dei cinque linguaggi di programmazione selezionati in tutto il mondo che compongono l'API Apache Spark.

Il linguaggio R supporta la programmazione procedurale insieme alle funzioni. Tuttavia, in particolare per alcune funzioni, supporta l'OOP (programmazione orientata agli oggetti) insieme alle funzioni generiche. I valori vengono utilizzati per passare argomenti se le funzioni e la loro valutazione hanno luogo quando vengono utilizzate, il che significa che non vengono valutate quando vengono chiamate le funzioni.

## Esempio di formato file R ##

### Sintassi ###

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

### Funzione ###

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

### Modellazione dei dati

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

## Riferimento ##

* [R - di Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



