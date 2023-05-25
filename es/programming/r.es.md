{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "archivo", "extensión", "formato de archivo", "bibliotecas de R", "Guía de programación", "ejemplo de r", "código de R", "bibliotecas de R", "Microsoft R" , "Código R", "Lenguaje R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Archivo de lenguaje de programación",
  "description":"Obtenga información sobre el formato de archivo R y las API que pueden crear y abrir archivos R",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## ¿Qué es un archivo R?

Un archivo con extensión .r pertenece al lenguaje de programación R. Este lenguaje se especifica para la computación estadística y es popular entre la comunidad de estadísticos. El análisis de datos y el desarrollo de software estadístico son dos categorías principales realizadas por este lenguaje en el campo de la minería de datos. Otra ventaja de usar este lenguaje y software es que proporciona la facilidad de gráficos estáticos que son útiles en la producción de gráficos de calidad. Se utilizan algunos paquetes adicionales para los gráficos dinámicos e interactivos.

El software de este lenguaje contiene una Licencia Pública General por lo que su disponibilidad es gratuita. El código de R generalmente se escribe en lenguajes de alto nivel como [C](/es/programming/c/) y R también. El software incluye una interfaz de línea de comandos junto con la disponibilidad de interfaces de terceros, como las interfaces gráficas de usuario de RStudio y Jupyter (interfaz de computadora portátil). Existen técnicas estadísticas utilizadas en la implementación de bibliotecas de R. También incluye modelado como lineal y no lineal.


## Breve historia ##

Este lenguaje es una implementación de la semántica del alcance léxico junto con el lenguaje S. En 1976 en Bell Labs, John Chambers desarrolló el lenguaje S. Incluso no hay una alteración en gran parte del código de S-PLUS cuando se usa en lenguaje R. En 1995, Martin Maechler y sus compañeros crearon el lenguaje R junto con el software libre bajo la licencia pública general.

El anuncio oficial de Comprehensive R Archive Network se realizó el 23 de abril de 1997. En 2000, se lanzó oficialmente la versión 1.0, que fue la primera versión beta estable. Su primer lanzamiento tuvo lugar en 1995, mientras que CRAN (red integral de archivos R) se lanzó en años posteriores.

En 1997 se formó un equipo central para seguir desarrollando el lenguaje después de los primeros lanzamientos. Muchas actualizaciones y versiones modificadas se lanzaron en los últimos años e incluyeron nuevas funciones de acuerdo con los sistemas operativos y la tecnología modernos. La modificación reciente se introdujo en mayo de 2021.


## Especificación técnica ##

R es un lenguaje de interpretación y se requiere un intérprete de línea de comandos para acceder a este lenguaje. Los cálculos como suma se escriben en el comando promo y los resultados se muestran después de la interpretación. Los datos y el código se representan mediante expresiones S. Otra especificación de este lenguaje es que puede funcionar como una caja de herramientas que proporciona la facilidad de cálculo matricial general.

Se utilizan varias aplicaciones para ejecutar y editar el código R. Los entornos de desarrollo integrados como Rattle GUI, RKWard también están disponibles para ejecutar el código del lenguaje de programación R. Otro software de Microsoft conocido como Microsoft R abierto también está disponible con compatibilidad con la distribución R para cálculos complejos, como los cálculos de subprocesos múltiples. R es uno de los cinco lenguajes de programación seleccionados en todo el mundo que componen la API de Apache Spark.

El lenguaje R admite la programación de procedimientos junto con las funciones. Sin embargo, para algunas funciones en particular, admite OOP (programación orientada a objetos) junto con las funciones genéricas. Los valores se usan para pasar argumentos si las funciones y su evaluación tienen lugar cuando se usan, lo que significa que no se evalúan cuando se llama a las funciones.

## Ejemplo de formato de archivo R ##

### Sintaxis ###

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

### Función ###

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

### Modelado de datos

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

## Referencia ##

* [R - por Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



