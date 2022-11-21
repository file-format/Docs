{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "arquivo", "extensão", "formato de arquivo", "bibliotecas de R", "Guia de programação", "exemplo r", "código de R", "bibliotecas de R", "Microsoft R" , "código R", "linguagem R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Arquivo de linguagem de programação",
  "description":"Saiba mais sobre o formato de arquivo R e APIs que podem criar e abrir arquivos R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## O que é um arquivo R?

Um arquivo com extensão .r pertence à linguagem de programação R. Essa linguagem é especificada para computação estatística e é popular entre a comunidade de estatísticos. A análise de dados e o desenvolvimento de softwares estatísticos são duas categorias principais realizadas por essa linguagem no campo da mineração de dados. Outra vantagem do uso desta linguagem e software é que ele fornece a facilidade de gráficos estáticos que são úteis na produção de gráficos de qualidade. Alguns pacotes adicionais são usados para os gráficos dinâmicos e interativos.

O software deste idioma contém uma Licença Pública Geral, portanto sua disponibilidade é gratuita. O código do R geralmente é escrito em linguagens de alto nível como [C](/pt/programming/c/) e o próprio R também. O software envolve uma interface de linha de comando juntamente com a disponibilidade de interfaces de terceiros, como interfaces gráficas de usuário do RStudio e Jupyter (interface de notebook). Existem técnicas estatísticas utilizadas na implementação de bibliotecas de R. Também inclui modelagem linear e não linear.


## Breve história ##

Esta linguagem é uma implementação da Semântica de escopo lexical junto com a linguagem S. Em 1976, no Bell Labs, John Chambers desenvolveu a linguagem S. Mesmo não havendo alteração em grande parte do código do S-PLUS ao ser utilizado na linguagem R. Em 1995, Martin Maechler e seus companheiros fizeram a linguagem R junto com o software livre sob a licença pública geral.

O anúncio oficial da Comprehensive R Archive Network foi feito em 23 de abril de 1997. Em 2000, a versão 1.0, que foi a primeira versão beta estável, foi lançada oficialmente. Seu primeiro lançamento ocorreu em 1995, enquanto o CRAN (rede abrangente de arquivos R) estava sendo lançado em anos posteriores.

Uma equipe principal foi formada em 1997 para o desenvolvimento da linguagem após os primeiros lançamentos. Muitas atualizações e versões modificadas foram sendo lançadas nos últimos anos e envolveram novos recursos de acordo com os sistemas operacionais e tecnologias modernas. A modificação recente foi introduzida em maio de 2021.


## Especificação Técnica ##

R é uma linguagem de interpretação e um interpretador de linha de comando é necessário para acessar essa linguagem. Os cálculos como soma são digitados no comando promo e os resultados são mostrados após a interpretação. Dados e código são representados por meio de expressões S. Outra especificação desta linguagem é que ela pode ser operada como uma caixa de ferramentas que fornece a facilidade de cálculo geral de matrizes.

Vários aplicativos são usados para executar e editar o código R. Ambientes de desenvolvimento integrados como Rattle GUI, RKWard também estão disponíveis para executar o código da linguagem de programação R. Outro software da Microsoft conhecido como Microsoft R open também está disponível com compatibilidade com a distribuição R para cálculos complexos, como cálculos multithread. R é uma das cinco linguagens de programação selecionadas em todo o mundo que compõem a API Apache Spark.

A linguagem R suporta programação procedural junto com as funções. No entanto, para algumas funções em particular, ele suporta OOP (programação orientada a objetos) junto com as funções genéricas. Os valores são usados para passar argumentos se as funções e sua avaliação ocorrem quando são usadas, o que significa que não são avaliadas quando as funções estão sendo chamadas.

## R Exemplo de formato de arquivo ##

### Sintaxe ###

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

### Função ###

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

### Modelagem de dados

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

## Referência ##

* [R - por Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



