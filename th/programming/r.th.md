{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "ไลบรารีของ R", "คู่มือการเขียนโปรแกรม", "ตัวอย่าง r", "โค้ดของ R", "ไลบรารีของ R", "Microsoft R" , "รหัส R", "ภาษา R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - ไฟล์ภาษาโปรแกรม",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ R และ API ที่สามารถสร้างและเปิดไฟล์ R",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## ไฟล์ R คืออะไร??

ไฟล์ที่มีนามสกุล .r เป็นของภาษาการเขียนโปรแกรม R ภาษานี้ถูกระบุสำหรับการคำนวณทางสถิติและเป็นที่นิยมในหมู่ชุมชนนักสถิติ การวิเคราะห์ข้อมูลและการพัฒนาซอฟต์แวร์ทางสถิติเป็นสองประเภทหลักที่ดำเนินการโดยภาษานี้ในด้านการทำเหมืองข้อมูล ข้อดีอีกประการของการใช้ภาษาและซอฟต์แวร์นี้คือให้ความสะดวกของกราฟคงที่ซึ่งเป็นประโยชน์ในการผลิตกราฟคุณภาพ แพ็คเกจเพิ่มเติมบางอย่างใช้สำหรับกราฟิกไดนามิกและอินเทอร์แอคทีฟ

ซอฟต์แวร์ของภาษานี้มีสัญญาอนุญาตแบบสาธารณะทั่วไป ดังนั้นจึงมีให้ใช้งานได้ฟรี โค้ดของ R มักเขียนด้วยภาษาระดับสูง เช่น [C](/th/programming/c/) และ R เองก็เช่นกัน ซอฟต์แวร์เกี่ยวข้องกับอินเทอร์เฟซบรรทัดคำสั่งพร้อมกับความพร้อมใช้งานของอินเทอร์เฟซบุคคลที่สาม เช่น อินเทอร์เฟซผู้ใช้แบบกราฟิกของ RStudio และ Jupyter (อินเทอร์เฟซโน้ตบุ๊ก) มีเทคนิคทางสถิติที่ใช้ในการดำเนินการห้องสมุดของอาร์ นอกจากนี้ยังรวมถึงการสร้างแบบจำลองเช่นเชิงเส้นและไม่เชิงเส้น


## ประวัติย่อ ##

ภาษานี้เป็นการนำ Semantics ของ lexical scoping ไปใช้กับภาษา S ในปี 1976 ที่ Bell Labs John Chambers ได้พัฒนาภาษา S แม้จะไม่มีการเปลี่ยนแปลงในโค้ดส่วนใหญ่ของ S-PLUS เมื่อใช้ในภาษา R ในปี 1995 Martin Maechler และเพื่อนของเขาได้สร้างภาษา R พร้อมกับซอฟต์แวร์ฟรีภายใต้ใบอนุญาตสาธารณะทั่วไป

การประกาศอย่างเป็นทางการของ Comprehensive R Archive Network มีขึ้นเมื่อวันที่ 23 เมษายน พ.ศ. 2540 ในปี พ.ศ. 2543 เวอร์ชัน 1.0 ซึ่งเป็นเบต้าเสถียรตัวแรกได้รับการเผยแพร่อย่างเป็นทางการ การเปิดตัวครั้งแรกเกิดขึ้นในปี 1995 ในขณะที่ CRAN (เครือข่าย R archive ที่ครอบคลุม) ได้รับการเผยแพร่ในปีถัดมา

ทีมงานหลักก่อตั้งขึ้นในปี 1997 เพื่อการพัฒนาเพิ่มเติมของภาษาหลังจากเผยแพร่ครั้งแรก การอัปเดตและเวอร์ชันที่แก้ไขจำนวนมากได้รับการเผยแพร่ในปีต่อๆ มา และเกี่ยวข้องกับคุณลักษณะใหม่ๆ ตามระบบปฏิบัติการและเทคโนโลยีสมัยใหม่ การปรับเปลี่ยนล่าสุดเปิดตัวในเดือนพฤษภาคม 2021


## ข้อมูลจำเพาะทางเทคนิค ##

R เป็นภาษาล่ามและต้องมีล่ามบรรทัดคำสั่งเพื่อเข้าถึงภาษานี้ การคำนวณ เช่น ผลรวม จะถูกพิมพ์ในคำสั่ง promo และผลลัพธ์จะแสดงขึ้นหลังจากการตีความ ข้อมูลและรหัสแสดงผ่าน S-expressions ข้อกำหนดอีกอย่างหนึ่งของภาษานี้คือสามารถใช้เป็นกล่องเครื่องมือที่ให้ความสะดวกในการคำนวณเมทริกซ์ทั่วไป

แอปพลิเคชั่นต่าง ๆ ใช้เพื่อเรียกใช้และแก้ไขรหัส R สภาพแวดล้อมการพัฒนาแบบรวม เช่น Rattle GUI, RKWard ก็มีให้ใช้งานเพื่อรันโค้ดของภาษาโปรแกรม R ซอฟต์แวร์อื่นจาก Microsoft ที่รู้จักในชื่อ Microsoft R open ยังพร้อมใช้งานที่เข้ากันได้กับการแจกจ่าย R สำหรับการคำนวณที่ซับซ้อน เช่น การคำนวณแบบมัลติเธรด R เป็นหนึ่งในห้าภาษาโปรแกรมที่ได้รับการคัดเลือกจากทั่วโลก ซึ่งประกอบด้วย Apache Spark API

ภาษา R รองรับการเขียนโปรแกรมตามขั้นตอนพร้อมกับฟังก์ชันต่างๆ อย่างไรก็ตาม สำหรับบางฟังก์ชันโดยเฉพาะ จะสนับสนุน OOP (การเขียนโปรแกรมเชิงวัตถุ) พร้อมกับฟังก์ชันทั่วไป ค่าจะใช้เพื่อส่งผ่านอาร์กิวเมนต์หากฟังก์ชันและการประเมินค่าเกิดขึ้นเมื่อใช้งาน ซึ่งหมายความว่าจะไม่ได้รับการประเมินเมื่อฟังก์ชันถูกเรียกใช้

## ตัวอย่างรูปแบบไฟล์ R ##

### ไวยากรณ์ ###

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

### การทำงาน ###

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

### การสร้างแบบจำลองข้อมูล

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

## อ้างอิง ##

* [R - โดย Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



