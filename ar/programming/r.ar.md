{
  "date" : "2021-09-06", 
  "keywords" :["R", "file", "extension", "file format", "libraries of R", "Programming Guide", "r example", "code of R", "libraries of R", "Microsoft R" , "كود R" , "لغة R" , "RStudio"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"R - ملف لغة البرمجة" ,
  "description":"تعرف على تنسيق ملف R وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات R وفتحها." ,
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-09-06"
}

## ما هو ملف R؟

ينتمي ملف بامتداد .r إلى لغة البرمجة R. هذه اللغة مخصصة للحوسبة الإحصائية وهي شائعة بين مجتمع الإحصائيين. يعد تحليل البيانات وتطوير البرامج الإحصائية فئتين رئيسيتين تؤديهما هذه اللغة في مجال التنقيب عن البيانات. ميزة أخرى لاستخدام هذه اللغة والبرنامج هي أنه يوفر تسهيلات الرسوم البيانية الثابتة التي تساعد في إنتاج الرسوم البيانية عالية الجودة. يتم استخدام بعض الحزم الإضافية للرسومات الديناميكية والتفاعلية.

يحتوي برنامج هذه اللغة على رخصة عامة عامة لذا فإن توفرها مجاني. عادةً ما يتم كتابة رمز R بلغات عالية المستوى مثل [C](/ar/programming/c/) و R نفسها أيضًا. يشتمل البرنامج على واجهة سطر أوامر جنبًا إلى جنب مع توفر واجهات الطرف الثالث مثل واجهات المستخدم الرسومية لـ RStudio و Jupyter (واجهة الكمبيوتر المحمول). هناك تقنيات إحصائية مستخدمة في تنفيذ مكتبات R. وتشمل أيضًا النمذجة مثل الخطي وغير الخطي.


## نبذة تاريخية ##

هذه اللغة هي تنفيذ لدلالات النطاق المعجمي جنبًا إلى جنب مع لغة S. في عام 1976 في Bell Labs ، طور John Chambers لغة S. حتى أنه لا يوجد تغيير في الكثير من كود S-PLUS عند استخدامه في لغة R. في عام 1995 ، ابتكر Martin Maechler ورفاقه لغة R جنبًا إلى جنب مع البرمجيات الحرة بموجب الترخيص العام العام.

تم الإعلان الرسمي عن شبكة أرشيف R الشاملة في 23 أبريل 1997. في عام 2000 ، تم إطلاق الإصدار 1. 0 ، الذي كان أول إصدار تجريبي مستقر ، رسميًا. تم إصداره لأول مرة في عام 1995 ، بينما تم إصدار CRAN (شبكة أرشيف R الشاملة) في السنوات اللاحقة.

تم تشكيل فريق أساسي في عام 1997 لمواصلة تطوير اللغة بعد الإصدارات الأولى. تم إصدار العديد من التحديثات والإصدارات المعدلة في السنوات اللاحقة وتضمنت ميزات جديدة وفقًا لأنظمة التشغيل والتكنولوجيا الحديثة. تم تقديم التعديل الأخير في مايو من عام 2021.


## مواصفات تكنيكال ##

R هي لغة ترجمة ومترجم سطر أوامر مطلوب للوصول إلى هذه اللغة. تتم كتابة العمليات الحسابية مثل sum في عرض الأوامر وتظهر النتائج بعد التفسير. يتم تمثيل البيانات والرمز من خلال تعبيرات S. من المواصفات الأخرى لهذه اللغة أنه يمكن تشغيلها كصندوق أدوات يوفر إمكانية حساب المصفوفة العامة.

تستخدم العديد من التطبيقات لتشغيل وتحرير كود R. تتوفر أيضًا بيئات التطوير المتكاملة مثل Rattle GUI و RKWard لتشغيل كود لغة البرمجة R. يتوفر أيضًا برنامج آخر من Microsoft يُعرف باسم Microsoft R open مع التوافق مع توزيع R للحسابات المعقدة مثل الحسابات متعددة مؤشرات الترابط. R هي إحدى لغات البرمجة الخمس المختارة حول العالم والتي تضم Apache Spark API.

تدعم لغة R البرمجة الإجرائية جنبًا إلى جنب مع الوظائف. ومع ذلك ، بالنسبة لبعض الوظائف على وجه الخصوص ، فهي تدعم OOP (البرمجة الشيئية) جنبًا إلى جنب مع الوظائف العامة. تُستخدم القيم لتمرير الوسيطات في حالة حدوث الدوال وتقييمها عند استخدامها ، مما يعني أنه لا يتم تقييمها عند استدعاء الوظائف.

## مثال على تنسيق ملف R ##

### بناء الجملة ###

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

### دور ###

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

### نمذجة البيانات

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

## المرجعي ##

* [R - بواسطة Wikipedia](https://en.wikipedia.org/wiki/R_ (developer_language))



