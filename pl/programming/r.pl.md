{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "plik", "rozszerzenie", "format pliku", "biblioteki R", "Przewodnik programowania", "przykład r", "kod R", "biblioteki R", "Microsoft R" , "Kod R", "Język R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Plik Języka Programowania",
  "description":"Poznaj format pliku R i interfejsy API, które mogą tworzyć i otwierać pliki R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Czym jest plik R?

Plik z rozszerzeniem .r należy do języka programowania R. Język ten jest przeznaczony do obliczeń statystycznych i jest popularny wśród statystyków. Analiza danych i tworzenie oprogramowania statystycznego to dwie główne kategorie wykonywane przez ten język w dziedzinie eksploracji danych. Kolejną zaletą korzystania z tego języka i oprogramowania jest to, że zapewnia on łatwość tworzenia statycznych wykresów, które są pomocne w tworzeniu wysokiej jakości wykresów. Niektóre dodatkowe pakiety są używane do dynamicznej i interaktywnej grafiki.

Oprogramowanie w tym języku zawiera Powszechną Licencję Publiczną, więc jego dostępność jest bezpłatna. Kod R jest zwykle napisany w językach wysokiego poziomu, takich jak [C](/pl/programming/c/) i sam R również. Oprogramowanie obejmuje interfejs wiersza poleceń wraz z dostępnością interfejsów innych firm, takich jak graficzne interfejsy użytkownika RStudio i Jupyter (interfejs notebooka). Istnieją techniki statystyczne stosowane w implementacji bibliotek R. Obejmuje to również modelowanie liniowe i nieliniowe.


## Krótka historia ##

Język ten jest implementacją semantyki zakresu leksykalnego wraz z językiem S. W 1976 roku w Bell Labs John Chambers opracował język S. Nawet nie ma zmian w dużej części kodu S-PLUS, gdy jest używany w języku R. W 1995 roku Martin Maechler i jego towarzysze stworzyli język R wraz z wolnym oprogramowaniem na licencji General Public License.

Oficjalne ogłoszenie Comprehensive R Archive Network miało miejsce 23 kwietnia 1997 roku. W 2000 roku została oficjalnie wydana wersja 1.0, która była pierwszą stabilną wersją beta. Jego pierwsze wydanie miało miejsce w 1995 roku, natomiast CRAN (comprehensive R Archive Network) był wydawany w latach późniejszych.

Podstawowy zespół powstał w 1997 roku w celu dalszego rozwoju języka po pierwszych wydaniach. W późniejszych latach wydano wiele aktualizacji i zmodyfikowanych wersji, które obejmowały nowe funkcje zgodnie z nowoczesnymi systemami operacyjnymi i technologią. Ostatnia modyfikacja została wprowadzona w maju 2021 roku.


## Specyfikacja techniczna ##

R jest językiem tłumaczącym i do uzyskania dostępu do tego języka wymagany jest interpreter wiersza poleceń. Obliczenia, takie jak suma, są wpisywane w promo polecenia, a wyniki są wyświetlane po interpretacji. Dane i kod są reprezentowane przez S-wyrażenia. Inną specyfikacją tego języka jest to, że może on działać jako zestaw narzędzi, który zapewnia łatwość ogólnego obliczania macierzy.

Do uruchamiania i edytowania kodu R używane są różne aplikacje. Zintegrowane środowiska programistyczne, takie jak Rattle GUI, RKWard, są również dostępne do uruchamiania kodu języka programowania R. Inne oprogramowanie firmy Microsoft, znane jako Microsoft R open, jest również dostępne z kompatybilnością z dystrybucją R do złożonych obliczeń, takich jak obliczenia wielowątkowe. R jest jednym z pięciu wybranych na całym świecie języków programowania, które składają się na Apache Spark API.

Język R obsługuje programowanie proceduralne wraz z funkcjami. Jednak w szczególności w przypadku niektórych funkcji obsługuje OOP (programowanie obiektowe) wraz z funkcjami ogólnymi. Wartości służą do przekazywania argumentów, jeśli funkcje mają miejsce, a ich ocena ma miejsce podczas ich używania, co oznacza, że nie są one oceniane podczas wywoływania funkcji.

## Przykład formatu pliku R ##

### Składnia ###

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

### Funkcja ###

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

### Modelowanie danych

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

## Odniesienie ##

* [R – z Wikipedii](https://en.wikipedia.org/wiki/R_(język_programowania))



