{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "파일", "확장자", "파일 형식", "R 라이브러리", "프로그래밍 가이드", "r 예제", "R 코드", "R 라이브러리", "Microsoft R" , "R 코드", "R 언어", "RStudio"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - 프로그래밍 언어 파일",
  "description":"R 파일 형식과 R 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## .R 파일이란?

확장자가 .r인 파일은 프로그래밍 언어 R에 속합니다. 이 언어는 통계 컴퓨팅을 위해 지정되었으며 통계 전문가 커뮤니티에서 널리 사용됩니다. 데이터 분석 및 통계 소프트웨어 개발은 데이터 마이닝 분야에서 이 언어로 수행되는 두 가지 주요 범주입니다. 이 언어와 소프트웨어를 사용하는 또 다른 장점은 고품질 그래프를 생성하는 데 도움이 되는 정적 그래프 기능을 제공한다는 것입니다. 동적 및 대화형 그래픽에 일부 추가 패키지가 사용됩니다.

이 언어의 소프트웨어에는 일반 공중 라이선스가 포함되어 있으므로 무료로 사용할 수 있습니다. R의 코드는 일반적으로 [C](/ko/programming/c/) 및 R 자체와 같은 고급 언어로 작성됩니다. 이 소프트웨어에는 RStudio 및 Jupyter(노트북 인터페이스)의 그래픽 사용자 인터페이스와 같은 타사 인터페이스의 가용성과 함께 명령줄 인터페이스가 포함됩니다. R 라이브러리의 구현에 사용되는 통계 기술이 있습니다. 여기에는 선형 및 비선형과 같은 모델링도 포함됩니다.


## 간략한 역사 ##

이 언어는 S 언어와 함께 어휘 범위의 의미론을 구현한 것입니다. 1976년 Bell Labs에서 John Chambers는 S 언어를 개발했습니다. S-PLUS의 코드를 R 언어로 사용하는 경우에도 많은 부분이 변경되지 않습니다. 1995년 Martin Maechler와 그의 동료들은 일반 공중 라이선스에 따라 자유 소프트웨어와 함께 R 언어를 만들었습니다.

Comprehensive R Archive Network의 공식 발표는 1997년 4월 23일에 이루어졌습니다. 2000년 첫 번째 안정 베타인 버전 1.0이 공식적으로 출시되었습니다. 첫 번째 릴리스는 1995년에 이루어졌으며 CRAN(종합 R 아카이브 네트워크)은 나중에 릴리스되었습니다.

첫 번째 릴리스 이후 언어의 추가 개발을 위해 1997년에 핵심 팀이 구성되었습니다. 많은 업데이트와 수정된 버전이 후기에 출시되었으며 최신 운영 체제 및 기술에 따른 새로운 기능이 포함되었습니다. 최근 수정 사항은 2021년 5월에 도입되었습니다.


## 기술 사양 ##

R은 통역 언어이며 이 언어에 액세스하려면 명령줄 인터프리터가 필요합니다. sum과 같은 계산은 명령 promo에 입력되고 결과는 해석 후 표시됩니다. 데이터와 코드는 S-표현식을 통해 표현됩니다. 이 언어의 또 다른 사양은 일반 행렬 계산 기능을 제공하는 도구 상자로 작동할 수 있다는 것입니다.

다양한 응용 프로그램이 R 코드를 실행하고 편집하는 데 사용됩니다. Rattle GUI, RKWard와 같은 통합 개발 환경에서도 R 프로그래밍 언어의 코드를 실행할 수 있습니다. Microsoft R open으로 알려진 Microsoft의 다른 소프트웨어도 다중 스레드 계산과 같은 복잡한 계산을 위한 R 배포와 호환됩니다. R은 Apache Spark API를 구성하는 전 세계적으로 선택된 5가지 프로그래밍 언어 중 하나입니다.

R 언어는 함수와 함께 절차적 프로그래밍을 지원합니다. 그러나 특히 일부 기능의 경우 일반 기능과 함께 OOP(객체 지향 프로그래밍)를 지원합니다. 값은 함수와 해당 평가가 사용될 때 발생하는 경우 인수를 전달하는 데 사용됩니다. 즉, 함수가 호출될 때 평가되지 않습니다.

## R 파일 형식 예 ##

### 구문 ###

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

### 기능 ###

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

### 데이터 모델링

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

## 참조 ##

* [R - by Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



