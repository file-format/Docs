{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "fichier", "extension", "format de fichier", "bibliothèques de R", "Guide de programmation", "r exemple", "code de R", "bibliothèques de R", "Microsoft R" , "Code R", "Langage R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Fichier de langage de programmation",
  "description":"En savoir plus sur le format de fichier R et les API qui peuvent créer et ouvrir des fichiers R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Qu'est-ce qu'un fichier R ?

Un fichier avec l'extension .r appartient au langage de programmation R. Ce langage est spécifié pour le calcul statistique et est populaire parmi la communauté des statisticiens. L'analyse de données et le développement de logiciels statistiques sont deux grandes catégories réalisées par ce langage dans le domaine de l'exploration de données. Un autre avantage de l'utilisation de ce langage et de ce logiciel est qu'il offre la possibilité de créer des graphiques statiques utiles à la production de graphiques de qualité. Certains packages supplémentaires sont utilisés pour les graphiques dynamiques et interactifs.

Le logiciel de cette langue contient une licence publique générale, sa disponibilité est donc gratuite. Le code de R est généralement écrit dans des langages de haut niveau tels que [C](/fr/programming/c/) et R lui-même également. Le logiciel implique une interface de ligne de commande ainsi que la disponibilité d'interfaces tierces telles que les interfaces utilisateur graphiques de RStudio et Jupyter (interface pour ordinateur portable). Il existe des techniques statistiques utilisées dans la mise en œuvre des bibliothèques de R. Il comprend également la modélisation comme linéaire et non linéaire.


## Bref historique ##

Ce langage est une implémentation de la sémantique de la portée lexicale avec le langage S. En 1976, aux Bell Labs, John Chambers développe le langage S. Même il n'y a pas de modification dans une grande partie du code de S-PLUS lorsqu'il est utilisé en langage R. En 1995, Martin Maechler et ses compagnons ont créé le langage R en même temps que le logiciel libre sous licence grand public.

L'annonce officielle du Comprehensive R Archive Network a été faite le 23 avril 1997. En 2000, la version 1. 0, qui était la première version bêta stable, a été officiellement publiée. Sa première version a eu lieu en 1995, tandis que le CRAN (réseau d'archives R complet) a été publié les années suivantes.

Une équipe centrale a été formée en 1997 pour poursuivre le développement du langage après les premières versions. De nombreuses mises à jour et versions modifiées ont été publiées au cours des dernières années et impliquaient de nouvelles fonctionnalités selon les systèmes d'exploitation et la technologie modernes. La modification récente a été introduite en mai 2021.


## Spécification technique ##

R est un langage d'interprétation et un interpréteur de ligne de commande est nécessaire pour accéder à ce langage. Les calculs comme somme sont tapés dans la commande promo et les résultats sont affichés après interprétation. Les données et le code sont représentés par des expressions S. Une autre spécification de ce langage est qu'il peut être utilisé comme une boîte à outils qui fournit la possibilité de calcul matriciel général.

Diverses applications sont utilisées pour exécuter et modifier le code R. Des environnements de développement intégrés tels que Rattle GUI, RKWard sont également disponibles pour exécuter le code du langage de programmation R. Un autre logiciel de Microsoft connu sous le nom de Microsoft R open est également disponible avec une compatibilité avec la distribution R pour les calculs complexes tels que les calculs multithreads. R est l'un des cinq langages de programmation sélectionnés dans le monde qui composent l'API Apache Spark.

Le langage R prend en charge la programmation procédurale avec les fonctions. Cependant, pour certaines fonctions en particulier, il prend en charge la POO (programmation orientée objet) ainsi que les fonctions génériques. Les valeurs sont utilisées pour passer des arguments si les fonctions et leur évaluation a lieu lorsqu'elles sont utilisées, ce qui signifie qu'elles ne sont pas évaluées lorsque les fonctions sont appelées.

## Exemple de format de fichier R ##

### Syntaxe ###

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

### Fonction ###

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

### La modélisation des données

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

## Référence ##

* [R - par Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



