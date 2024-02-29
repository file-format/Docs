{
  "date": "2021-09-06",
  "keywords": [
"آر",
"فایل",
"افزونه",
"فرمت فایل",
"کتابخانه های R",
"راهنمای برنامه نویسی",
"r مثال",
"کد R",
"کتابخانه های R",
"مایکروسافت آر",
"کد R",
"زبان R",
"RStudio"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "R - فایل زبان برنامه نویسی",
  "description": "با فرمت فایل R و APIهایی که می توانند فایل های R را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--far"
}
},
  "lastmod": "2021-09-06"
}

## فایل R چیست؟

فایلی با پسوند .r متعلق به زبان برنامه نویسی R است. این زبان برای محاسبات آماری مشخص شده و در بین جامعه آماردانان محبوب است. تجزیه و تحلیل داده ها و توسعه نرم افزارهای آماری دو مقوله اصلی است که توسط این زبان در زمینه داده کاوی انجام می شود. یکی دیگر از مزایای استفاده از این زبان و نرم افزار این است که امکان نمودارهای ثابت را فراهم می کند که در تولید نمودارهای با کیفیت کمک کننده است. برخی از بسته های اضافی برای گرافیک پویا و تعاملی استفاده می شود.

نرم افزار این زبان حاوی مجوز عمومی عمومی است بنابراین در دسترس بودن آن رایگان است. کد R معمولاً در زبان های سطح بالا مانند [C](/programming/c/) و خود R نیز نوشته می شود. این نرم افزار شامل یک رابط خط فرمان به همراه در دسترس بودن رابط های شخص ثالث مانند رابط های گرافیکی کاربر RStudio و Jupyter (رابط نوت بوک) است. تکنیک‌های آماری در پیاده‌سازی کتابخانه‌های R استفاده می‌شود. همچنین شامل مدل‌سازی خطی و غیرخطی می‌شود.


## تاریخچه مختصر ##

این زبان در کنار زبان S پیاده‌سازی معناشناسی محدوده واژگانی است. در سال 1976 در آزمایشگاه بل، جان چمبرز زبان S را توسعه داد. حتی در بسیاری از کد S-PLUS هنگام استفاده در زبان R تغییری ایجاد نمی شود. در سال 1995، مارتین ماکلر و همراهانش زبان R را به همراه نرم افزار رایگان تحت مجوز عمومی ساختند.

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. در سال 2000 نسخه 1. 0 که اولین نسخه بتا پایدار بود، رسما منتشر شد. اولین انتشار آن در سال 1995 اتفاق افتاد، در حالی که CRAN (شبکه آرشیو جامع R) در سال های بعد منتشر شد. 

یک تیم اصلی در سال 1997 برای توسعه بیشتر زبان پس از اولین نسخه ها تشکیل شد. بسیاری از به روز رسانی ها و نسخه های اصلاح شده در سال های بعد منتشر شد و شامل ویژگی های جدید با توجه به سیستم عامل ها و تکنولوژی مدرن بود. اصلاحات اخیر در ماه می 2021 معرفی شد.


## مشخصات فنی ##

R یک زبان مفسر است و برای دسترسی به این زبان به یک مفسر خط فرمان نیاز است. محاسبات مانند sum در دستور تبلیغاتی تایپ شده و نتایج پس از تفسیر نشان داده می شود. داده ها و کد از طریق S-expressions نشان داده می شوند. یکی دیگر از مشخصات این زبان این است که می توان از آن به عنوان جعبه ابزاری استفاده کرد که امکان محاسبه ماتریس عمومی را فراهم می کند.

برنامه های مختلفی برای اجرا و ویرایش کد R استفاده می شود. محیط های توسعه یکپارچه مانند Rattle GUI، RKWard نیز برای اجرای کدهای زبان برنامه نویسی R در دسترس هستند. نرم افزار دیگر مایکروسافت به نام Microsoft R open نیز با سازگاری با توزیع R برای محاسبات پیچیده مانند محاسبات چند رشته ای موجود است. R یکی از پنج زبان برنامه نویسی منتخب در سراسر جهان است که Apache Spark API را شامل می شود.

زبان R از برنامه نویسی رویه ای همراه با توابع پشتیبانی می کند. با این حال، به ویژه برای برخی از توابع، از OOP (برنامه نویسی شی گرا) همراه با توابع عمومی پشتیبانی می کند. اگر توابع و ارزیابی آنها هنگام استفاده از آنها صورت گیرد، از مقادیر برای ارسال آرگومان استفاده می شود، به این معنی که هنگام فراخوانی توابع ارزیابی نمی شوند.

## فرمت فایل R مثال ##

### نحو ###

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

### تابع ###

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

### مدل سازی داده ها

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

## ارجاع ##

* [R - توسط Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))




