{
  "date": "2021-09-06",
  "keywords": [
"R",
"fayl",
"uzadılması",
"fayl formatı",
"R-nin kitabxanaları",
"Proqramlaşdırma bələdçisi",
"r misal",
"kodu R",
"R-nin kitabxanaları",
"Microsoft R",
"R kodu",
"R dili",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - Proqramlaşdırma Dili Faylı",
  "description": "R faylları yarada və aça bilən R fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--azr"
}
},
  "lastmod": "2021-09-06"
}

## R faylı nədir?

.r uzantılı fayl R proqramlaşdırma dilinə aiddir. Bu dil statistik hesablamalar üçün nəzərdə tutulub və statistiklər icması arasında populyardır. Məlumatların təhlili və statistik proqram təminatının inkişafı bu dil tərəfindən verilənlərin istehsalı sahəsində həyata keçirilən iki əsas kateqoriyadır. Bu dil və proqram təminatından istifadənin digər üstünlüyü keyfiyyətli qrafiklərin istehsalında faydalı olan statik qrafiklərin imkanını təmin etməsidir. Dinamik və interaktiv qrafiklər üçün bəzi əlavə paketlərdən istifadə olunur.

Bu dilin proqram təminatı Ümumi İctimai Lisenziyaya malikdir, ona görə də onun mövcudluğu pulsuzdur. R kodu adətən [C](/programming/c/) və R-nin özü kimi yüksək səviyyəli dillərdə yazılır. Proqram təminatı, RStudio və Jupyter (notebook interfeysi) qrafik istifadəçi interfeysləri kimi üçüncü tərəf interfeyslərinin mövcudluğu ilə yanaşı, komanda xətti interfeysini əhatə edir. R-nin kitabxanalarının həyata keçirilməsində istifadə olunan statistik üsullar var. Buraya xətti və qeyri-xətti kimi modelləşdirmə də daxildir.


## Qısa tarix ##

Bu dil S dili ilə birlikdə leksik əhatə dairəsinin Semantikasının tətbiqidir. 1976-cı ildə Bell Labs-da Con Çembers S dilini inkişaf etdirdi. Hətta R dilində istifadə edildikdə S-PLUS kodunun çoxunda dəyişiklik yoxdur. 1995-ci ildə Martin Maechler və onun yoldaşları ümumi ictimai lisenziya altında pulsuz proqram təminatı ilə birlikdə R dilini yaratdılar.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. 2000-ci ildə ilk stabil beta olan 1.0 versiyası rəsmi olaraq buraxıldı. İlk buraxılışı 1995-ci ildə baş verdi, CRAN (hərtərəfli R arxiv şəbəkəsi) sonrakı illərdə buraxıldı. 

İlk buraxılışlardan sonra dilin daha da inkişafı üçün 1997-ci ildə əsas komanda yaradılmışdır. Sonrakı illərdə bir çox yeniləmələr və dəyişdirilmiş versiyalar buraxıldı və müasir əməliyyat sistemləri və texnologiyasına uyğun olaraq yeni funksiyaları əhatə etdi. Son modifikasiya 2021-ci ilin may ayında təqdim edildi.


## Texniki Spesifikasiya ##

R tərcümə dilidir və bu dilə daxil olmaq üçün komanda xətti tərcüməçisi tələb olunur. Məbləğ kimi hesablamalar əmr promosunda yazılır və nəticələr şərh edildikdən sonra göstərilir. Məlumat və kod S-ifadələri ilə təmsil olunur. Bu dilin başqa bir xüsusiyyəti ondan ibarətdir ki, o, ümumi matrisin hesablanması imkanını təmin edən alətlər qutusu kimi işlədilə bilər.

R kodunu işə salmaq və redaktə etmək üçün müxtəlif proqramlardan istifadə olunur. R proqramlaşdırma dilinin kodunu işlətmək üçün Rattle GUI, RKWard kimi inteqrasiya olunmuş inkişaf mühitləri də mövcuddur. Microsoft tərəfindən Microsoft R open kimi tanınan başqa bir proqram da çox yivli hesablamalar kimi mürəkkəb hesablamalar üçün R paylanması ilə uyğunluqla mövcuddur. R, Apache Spark API-dən ibarət bütün dünyada seçilmiş beş proqramlaşdırma dilindən biridir.

R dili funksiyalarla yanaşı prosedur proqramlaşdırmanı dəstəkləyir. Bununla belə, xüsusən bəzi funksiyalar üçün ümumi funksiyalarla birlikdə OOP (obyekt yönümlü proqramlaşdırma) dəstəkləyir. Dəyərlər arqumentləri ötürmək üçün istifadə olunur, əgər funksiyalar istifadə edildikdə və onların qiymətləndirilməsi baş verirsə, yəni funksiyalar çağırılan zaman qiymətləndirilmir.

## R Fayl Format Nümunəsi ##

### Sintaksis ###

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

### Funksiya ###

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

### Məlumatların Modelləşdirilməsi

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

## İstinad ##

* [R - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/R_(proqramlaşdırma_dili))




