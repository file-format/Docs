{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "file", "ekstensi", "format file", "perpustakaan R", "Panduan Pemrograman", "contoh r", "kode R", "perpustakaan R", "Microsoft R" , "Kode R", "Bahasa R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - File Bahasa Pemrograman",
  "description":"Pelajari tentang format file R dan API yang dapat membuat dan membuka file R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Apa itu file R?

File dengan ekstensi .r milik bahasa pemrograman R. Bahasa ini ditentukan untuk komputasi statistik dan populer di kalangan komunitas ahli statistik. Analisis data dan pengembangan perangkat lunak statistik adalah dua kategori utama yang dilakukan oleh bahasa ini di bidang penambangan data. Keuntungan lain menggunakan bahasa dan perangkat lunak ini adalah menyediakan fasilitas grafik statis yang sangat membantu dalam produksi grafik berkualitas. Beberapa paket tambahan digunakan untuk grafik dinamis dan interaktif.

Perangkat lunak bahasa ini berisi Lisensi Publik Umum sehingga ketersediaannya gratis. Kode R biasanya ditulis dalam bahasa tingkat tinggi seperti [C](/id/programming/c/) dan juga R itu sendiri. Perangkat lunak ini melibatkan antarmuka baris perintah bersama dengan ketersediaan antarmuka pihak ketiga seperti antarmuka pengguna grafis RStudio dan Jupyter (antarmuka notebook). Ada teknik statistik yang digunakan dalam implementasi pustaka R. Ini juga mencakup pemodelan seperti linier dan nonlinier.


## Sejarah Singkat ##

Bahasa ini merupakan implementasi dari Semantics of lexical scoping bersama dengan bahasa S. Pada tahun 1976 di Bell Labs, John Chambers mengembangkan bahasa S. Bahkan tidak banyak perubahan kode S-PLUS saat digunakan dalam bahasa R. Pada tahun 1995, Martin Maechler dan rekan-rekannya membuat bahasa R bersama dengan perangkat lunak gratis di bawah lisensi publik.

Pengumuman resmi Comprehensive R Archive Network dibuat pada tanggal 23 April 1997. Pada tahun 2000 versi 1.0, yang merupakan beta stabil pertama, dirilis secara resmi. Rilis pertamanya terjadi pada tahun 1995, sedangkan CRAN (jaringan arsip R komprehensif) dirilis pada tahun-tahun berikutnya.

Tim inti dibentuk pada tahun 1997 untuk pengembangan bahasa lebih lanjut setelah rilis pertama. Banyak pembaruan dan versi modifikasi dirilis pada tahun-tahun berikutnya dan melibatkan fitur-fitur baru sesuai dengan sistem operasi dan teknologi modern. Modifikasi terbaru diperkenalkan pada Mei 2021.


## Spesifikasi Teknis ##

R adalah bahasa interpretasi dan juru bahasa baris perintah diperlukan untuk mengakses bahasa ini. Perhitungan seperti jumlah diketik dalam perintah promo dan hasilnya ditampilkan setelah interpretasi. Data dan kode direpresentasikan melalui ekspresi-S. Spesifikasi lain dari bahasa ini adalah dapat dioperasikan sebagai toolbox yang menyediakan fasilitas perhitungan matriks secara umum.

Berbagai aplikasi digunakan untuk menjalankan dan mengedit kode R. Lingkungan pengembangan terintegrasi seperti Rattle GUI, RKWard juga tersedia untuk menjalankan kode bahasa pemrograman R. Perangkat lunak lain oleh Microsoft yang dikenal sebagai Microsoft R open juga tersedia dengan kompatibilitas dengan distribusi R untuk komputasi kompleks seperti komputasi multithreaded. R adalah salah satu dari lima bahasa pemrograman terpilih di seluruh dunia yang terdiri dari Apache Spark API.

Bahasa R mendukung pemrograman prosedural bersama dengan fungsinya. Namun, untuk beberapa fungsi khususnya, mendukung OOP (pemrograman berorientasi objek) bersama dengan fungsi generik. Nilai digunakan untuk meneruskan argumen jika fungsi dan evaluasinya terjadi saat digunakan, yang berarti nilai tidak dievaluasi saat fungsi dipanggil.

## Contoh Format File R ##

### Sintaks ###

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

### Fungsi ###

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

### Pemodelan Data

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

## Referensi ##

* [R - oleh Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



