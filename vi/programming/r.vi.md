{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "file", "extension", "file format", "libraries of R", "Programming Guide", "r example", "code of R", "libraries of R", "Microsoft R" , "Mã R", "Ngôn ngữ R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Tệp ngôn ngữ lập trình",
  "description":"Tìm hiểu về định dạng tệp R và API có thể tạo và mở tệp R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Tệp R là gì?

Tệp có phần mở rộng .r thuộc về ngôn ngữ lập trình R. Ngôn ngữ này được chỉ định cho tính toán thống kê và phổ biến trong cộng đồng các nhà thống kê. Phân tích dữ liệu và phát triển phần mềm thống kê là hai hạng mục chính được thực hiện bởi ngôn ngữ này trong lĩnh vực khai thác dữ liệu. Một ưu điểm khác của việc sử dụng ngôn ngữ và phần mềm này là nó cung cấp cơ sở của các biểu đồ tĩnh, hữu ích trong việc tạo ra các biểu đồ chất lượng. Một số gói bổ sung được sử dụng cho đồ họa động và tương tác.

Phần mềm của ngôn ngữ này có Giấy phép Công cộng nên tính khả dụng của nó là miễn phí. Mã của R thường được viết bằng các ngôn ngữ cấp cao như [C](/vi/programming/c/) và chính R cũng vậy. Phần mềm bao gồm giao diện dòng lệnh cùng với sự sẵn có của giao diện bên thứ ba như giao diện người dùng đồ họa của RStudio và Jupyter (giao diện máy tính xách tay). Có các kỹ thuật thống kê được sử dụng trong việc triển khai các thư viện của R. Nó cũng bao gồm các mô hình như tuyến tính và phi tuyến tính.


## Lược Sử ##

Ngôn ngữ này là một triển khai Ngữ nghĩa của phạm vi từ vựng cùng với ngôn ngữ S. Năm 1976 tại Bell Labs, John Chambers đã phát triển ngôn ngữ S. Thậm chí không có sự thay đổi nào trong phần lớn mã của S-PLUS khi được sử dụng bằng ngôn ngữ R. Năm 1995, Martin Maechler và những người bạn đồng hành của ông đã tạo ra ngôn ngữ R cùng với phần mềm miễn phí theo giấy phép General Public.

Thông báo chính thức về Mạng lưu trữ R toàn diện được đưa ra vào ngày 23 tháng 4 năm 1997. Năm 2000, phiên bản 1. 0, bản beta ổn định đầu tiên, được phát hành chính thức. Bản phát hành đầu tiên của nó diễn ra vào năm 1995, trong khi CRAN (mạng lưu trữ R toàn diện) được phát hành trong những năm sau đó.

Một nhóm cốt lõi được thành lập vào năm 1997 để phát triển thêm ngôn ngữ sau những bản phát hành đầu tiên. Nhiều bản cập nhật và phiên bản sửa đổi đã được phát hành trong những năm sau đó và bao gồm các tính năng mới theo công nghệ và hệ điều hành hiện đại. Bản sửa đổi gần đây đã được giới thiệu vào tháng 5 năm 2021.


## Đặc điểm kỹ thuật ##

R là ngôn ngữ thông dịch và cần có trình thông dịch dòng lệnh để truy cập ngôn ngữ này. Các tính toán như tổng được nhập vào lệnh promo và kết quả được hiển thị sau khi diễn giải. Dữ liệu và mã được biểu diễn thông qua biểu thức S. Một đặc điểm kỹ thuật khác của ngôn ngữ này là nó có thể được vận hành như một hộp công cụ cung cấp khả năng tính toán ma trận chung.

Các ứng dụng khác nhau được sử dụng để chạy và chỉnh sửa mã R. Các môi trường phát triển tích hợp như Rattle GUI, RKWard cũng có sẵn để chạy mã của ngôn ngữ lập trình R. Một phần mềm khác của Microsoft được gọi là Microsoft R open cũng có khả năng tương thích với phân phối R cho các tính toán phức tạp như tính toán đa luồng. R là một trong năm ngôn ngữ lập trình được chọn trên toàn thế giới bao gồm Apache Spark API.

Ngôn ngữ R hỗ trợ lập trình thủ tục cùng với các chức năng. Tuy nhiên, đối với một số chức năng đặc biệt, nó hỗ trợ OOP (lập trình hướng đối tượng) cùng với các chức năng chung. Các giá trị được sử dụng để truyền đối số nếu các hàm và việc đánh giá chúng diễn ra khi chúng được sử dụng, điều đó có nghĩa là chúng không được đánh giá khi các hàm được gọi.

## Ví dụ về định dạng tệp R ##

### Cú pháp ###

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

### Hàm số ###

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

### Mô hình hóa dữ liệu

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

## Tài liệu tham khảo ##

* [R - theo Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



