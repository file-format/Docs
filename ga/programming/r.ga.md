{
  "date": "2021-09-06",
  "keywords": [
"R",
"comhad",
"síneadh",
"formáid comhaid",
"leabharlanna R",
"Treoir Ríomhchlárúcháin",
"r shampla",
"CÓD R",
"leabharlanna R",
"Microsoft R",
"R cód",
"R teanga",
"RSstudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - Comhad Teanga Ríomhchlárúcháin",
  "description": "Foghlaim faoi fhormáid comhaid R agus APIanna ar féidir leo comhaid R a chruthú agus a oscailt.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--gar"
}
},
  "lastmod": "2021-09-06"
}

## Cad is comhad R ann?

Baineann comhad le síneadh .r leis an teanga ríomhchlárúcháin R. Sonraítear an teanga seo do ríomhaireacht staitistiúil agus tá an-tóir uirthi i measc an phobail staitisteoirí. Dhá phríomhchatagóir a dhéanann an teanga seo i réimse an mhianadóireacht sonraí is ea anailís sonraí agus forbairt bogearraí staidrimh. Buntáiste eile a bhaineann leis an teanga agus na bogearraí seo a úsáid ná go soláthraíonn sé áis graif statacha a chuidíonn le graif cáilíochta a tháirgeadh. Úsáidtear roinnt pacáistí breise le haghaidh na ngrafaicí dinimiciúla agus idirghníomhacha.

Tá Ceadúnas Ginearálta Poiblí i mbogearraí na teanga seo agus mar sin tá sé ar fáil saor in aisce. De ghnáth scríobhtar an cód R i dteangacha ardleibhéil mar [C](/programming/c/) agus R féin freisin. Tá comhéadan líne ordaithe i gceist leis na bogearraí mar aon le hinfhaighteacht comhéadain tríú páirtí ar nós comhéadain grafacha úsáideora RStudio agus Jupyter (comhéadan leabhar nótaí). Tá teicnící staitistiúla a úsáidtear chun leabharlanna R a chur i bhfeidhm. Áiríonn sé freisin samhaltú líneach agus neamhlíneach.


## Stair Ghearr ##

Feidhmiú Séimeantaic na scóipe foclóireachta mar aon leis an teanga S í an teanga seo. I 1976 ag Bell Labs, d'fhorbair John Chambers an S teanga. Fiú níl aon athrú ar go leor de chód S-PLUS nuair a úsáidtear é i dteanga R. Sa bhliain 1995, rinne Martin Maechler agus a chompánaigh an teanga R in éineacht leis na bogearraí in aisce faoin gceadúnas Ginearálta poiblí.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. Sa bhliain 2000 an leagan 1. 0, a bhí an chéad cobhsaí béite, a scaoileadh go hoifigiúil. Tharla a chéad eisiúint i 1995, agus an CRAN (líonra cartlainne cuimsitheach R) á scaoileadh sna blianta ina dhiaidh sin. 

Bunaíodh foireann lárnach i 1997 chun an teanga a fhorbairt a thuilleadh tar éis na chéad eisiúintí. Bhí go leor nuashonruithe agus leaganacha modhnaithe á n-eisiúint sna blianta ina dhiaidh sin agus bhí gnéithe nua i gceist leo de réir córais oibriúcháin agus teicneolaíochta nua-aimseartha. Tugadh isteach an modhnú le déanaí i mí na Bealtaine 2021.


## Sonraíocht Theicniúil ##

Is teanga ateangaireachta í R agus tá ateangaire ordú-líne ag teastáil chun an teanga seo a rochtain. Clóscríobhtar na ríomhanna cosúil le suim sa phromóisean ordaithe agus taispeántar na torthaí tar éis léirmhínithe. Léirítear sonraí agus cód trí S-léirithe. Sonraíocht eile den teanga seo ná gur féidir é a oibriú mar bhosca uirlisí a sholáthraíonn áis ríomh maitrís ginearálta.

Úsáidtear feidhmchláir éagsúla chun an cód R a rith agus a chur in eagar. Tá timpeallachtaí forbartha comhtháite ar nós Rattle GUI, RKWard ar fáil freisin chun cód na teanga ríomhchlárúcháin R a rith. Tá bogearraí eile ó Microsoft ar a dtugtar Microsoft R open ar fáil freisin atá comhoiriúnach le dáileadh R le haghaidh ríomhanna casta ar nós ríomhanna ilshnáithe. Tá R ar cheann de na cúig theanga ríomhchláraithe roghnaithe ar fud an domhain a chuimsíonn Apache Spark API.

Tacaíonn teanga R le cláir nós imeachta chomh maith leis na feidhmeanna. I gcás roinnt feidhmeanna go háirithe, áfach, tacaíonn sé le OOP (ríomhchlárú atá dírithe ar réad) mar aon leis na feidhmeanna cineálacha. Úsáidtear luachanna chun argóintí a rith má tharlaíonn feidhmeanna agus a luacháil nuair a úsáidtear iad, rud a chiallaíonn nach ndéantar iad a mheas nuair a bhíonn feidhmeanna á nglao.

## R Sampla Formáid Chomhaid ##

### Comhréir ###

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

### Feidhm ###

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

### Samhaltú Sonraí

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

## Tagairt ##

* [R - le Vicipéid](https://ga.wikipedia.org/wiki/R_(programming_language))




