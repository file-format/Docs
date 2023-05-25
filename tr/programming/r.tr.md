{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "dosya", "uzantı", "dosya biçimi", "R kitaplıkları", "Programlama Kılavuzu", "r örneği", "R kodu", "R kitaplıkları", "Microsoft R" , "R kodu", "R dili", "RStudio"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Programlama Dili Dosyası",
  "description":"R dosya formatı ve R dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## R dosyası nedir?

.r uzantılı bir dosya, R programlama diline aittir. Bu dil, istatistiksel hesaplama için belirtilmiştir ve istatistikçiler topluluğu arasında popülerdir. Veri analizi ve istatistiksel yazılımın geliştirilmesi, veri madenciliği alanında bu dil tarafından gerçekleştirilen iki ana kategoridir. Bu dili ve yazılımı kullanmanın bir başka avantajı da, kaliteli grafiklerin üretilmesine yardımcı olan statik grafikler oluşturma olanağı sağlamasıdır. Dinamik ve etkileşimli grafikler için bazı ek paketler kullanılır.

Bu dilin yazılımı bir Genel Kamu Lisansı içerir, dolayısıyla kullanılabilirliği ücretsizdir. R'nin kodu genellikle [C](/tr/programming/c/) ve R'nin kendisi gibi yüksek seviyeli dillerde yazılır. Yazılım, RStudio ve Jupyter'in grafik kullanıcı arabirimleri (dizüstü bilgisayar arabirimi) gibi üçüncü taraf arabirimlerin kullanılabilirliği ile birlikte bir komut satırı arabirimi içerir. R kütüphanelerinin uygulanmasında kullanılan istatistiksel teknikler vardır. Ayrıca doğrusal ve doğrusal olmayan modellemeyi de içerir.


## Kısa Tarih ##

Bu dil, S diliyle birlikte sözcüksel kapsam belirleme Semantiğinin bir uygulamasıdır. 1976'da Bell Laboratuarlarında John Chambers, S dilini geliştirdi. Hatta S-PLUS'ın kodunda R dilinde kullanıldığında pek bir değişiklik olmuyor. 1995 yılında Martin Maechler ve arkadaşları, Genel kamu lisansı altında ücretsiz yazılımla birlikte R dilini yaptı.

Comprehensive R Archive Network'ün resmi duyurusu 23 Nisan 1997'de yapıldı. 2000 yılında ilk kararlı beta olan 1.0 versiyonu resmi olarak yayınlandı. İlk sürümü 1995 yılında gerçekleşirken, daha sonraki yıllarda CRAN (kapsamlı R arşiv ağı) piyasaya sürülüyordu.

İlk sürümlerden sonra dilin daha da geliştirilmesi için 1997 yılında çekirdek bir ekip oluşturuldu. Daha sonraki yıllarda birçok güncelleme ve değiştirilmiş sürüm yayınlandı ve modern işletim sistemlerine ve teknolojisine göre yeni özellikler içeriyordu. Son değişiklik Mayıs 2021'de tanıtıldı.


## Teknik Şartname ##

R bir yorumlama dilidir ve bu dile erişmek için bir komut satırı yorumlayıcısı gerekir. Toplam gibi hesaplamalar promo komutunda yazılır ve yorumlandıktan sonra sonuçlar gösterilir. Veriler ve kod, S ifadeleriyle temsil edilir. Bu dilin bir başka özelliği de, genel matris hesaplama kolaylığı sağlayan bir araç kutusu olarak çalıştırılabilmesidir.

R kodunu çalıştırmak ve düzenlemek için çeşitli uygulamalar kullanılır. R programlama dilinin kodunu çalıştırmak için Rattle GUI, RKWard gibi entegre geliştirme ortamları da mevcuttur. Microsoft R open olarak bilinen başka bir Microsoft yazılımı da çok iş parçacıklı hesaplamalar gibi karmaşık hesaplamalar için R dağıtımıyla uyumlu olarak mevcuttur. R, dünya çapında Apache Spark API'yi içeren seçilmiş beş programlama dilinden biridir.

R dili, işlevlerle birlikte yordamsal programlamayı destekler. Bununla birlikte, özellikle bazı işlevler için, genel işlevlerle birlikte OOP'yi (nesne yönelimli programlama) destekler. Değerler, işlevler ve bunların değerlendirilmesi kullanıldıklarında gerçekleşirse argümanları iletmek için kullanılır, yani işlevler çağrılırken değerlendirilmezler.

## R Dosya Biçimi Örneği ##

### Sözdizimi ###

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

### İşlev ###

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

### Veri Modelleme

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

## Referans ##

* [R - Wikipedia'dan](https://en.wikipedia.org/wiki/R_(programming_language))



