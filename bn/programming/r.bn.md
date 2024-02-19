{
  "date": "2021-09-06",
  "keywords": [
    "R",
    "file",
    "extension",
    "file format",
    "libraries of R",
    "Programming Guide",
    "r example",
    "code of R",
    "libraries of R",
    "Microsoft R",
    "R code",
    "R language",
    "RStudio"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "R - প্রোগ্রামিং ল্যাঙ্গুয়েজ ফাইল",
  "description": "R ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যা R ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle": "R",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-r-bn"
    }
  },
  "lastmod": "2021-09-06"
}

## একটি R ফাইল কি?

এক্সটেনশন .r সহ একটি ফাইল R প্রোগ্রামিং ভাষার অন্তর্গত। এই ভাষাটি পরিসংখ্যানগত কম্পিউটিং-এর জন্য নির্দিষ্ট করা হয়েছে এবং পরিসংখ্যানবিদদের সম্প্রদায়ের মধ্যে জনপ্রিয়। ডেটা বিশ্লেষণ এবং পরিসংখ্যানগত সফ্টওয়্যারের বিকাশ হল দুটি প্রধান বিভাগ যা ডেটা মাইনিংয়ের ক্ষেত্রে এই ভাষা দ্বারা সঞ্চালিত হয়। এই ভাষা এবং সফ্টওয়্যার ব্যবহার করার আরেকটি সুবিধা হল এটি স্ট্যাটিক গ্রাফের সুবিধা প্রদান করে যা মানসম্পন্ন গ্রাফ তৈরিতে সহায়ক। কিছু অতিরিক্ত প্যাকেজ গতিশীল এবং ইন্টারেক্টিভ গ্রাফিক্সের জন্য ব্যবহার করা হয়।

এই ভাষার সফ্টওয়্যারটিতে একটি সাধারণ পাবলিক লাইসেন্স রয়েছে তাই এর প্রাপ্যতা বিনামূল্যে। R-এর কোড সাধারণত উচ্চ-স্তরের ভাষায় লেখা হয় যেমন [C](/programming/c/) এবং R নিজেও। সফ্টওয়্যারটিতে একটি কমান্ড-লাইন ইন্টারফেস এবং তৃতীয় পক্ষের ইন্টারফেস যেমন RStudio এবং Jupyter (নোটবুক ইন্টারফেস) এর গ্রাফিকাল ইউজার ইন্টারফেসের উপলব্ধতা রয়েছে। R-এর লাইব্রেরি বাস্তবায়নে পরিসংখ্যানগত কৌশল ব্যবহার করা হয়েছে। এতে লিনিয়ার এবং ননলাইনারের মতো মডেলিংও অন্তর্ভুক্ত রয়েছে।


## সংক্ষিপ্ত ইতিহাস ##

এই ভাষাটি S ভাষার সাথে আভিধানিক স্কোপিংয়ের শব্দার্থবিদ্যার একটি বাস্তবায়ন। 1976 সালে বেল ল্যাবসে, জন চেম্বার্স এস ভাষা তৈরি করেন। এমনকি R ভাষায় ব্যবহার করার সময় S-PLUS এর কোডের অনেকাংশে কোনো পরিবর্তন নেই। 1995 সালে, মার্টিন মেচলার এবং তার সঙ্গীরা সাধারণ পাবলিক লাইসেন্সের অধীনে বিনামূল্যের সফ্টওয়্যারের সাথে R ভাষা তৈরি করেছিলেন।

The official announcement of the Comprehensive R Archive Network was made on 23rd April 1997. 2000 সালে সংস্করণ 1. 0, যা ছিল প্রথম স্থিতিশীল বিটা, আনুষ্ঠানিকভাবে প্রকাশিত হয়েছিল। এটির প্রথম প্রকাশ 1995 সালে হয়েছিল, যখন CRAN (বিস্তৃত আর আর্কাইভ নেটওয়ার্ক) পরবর্তী বছরগুলিতে প্রকাশিত হয়েছিল। 

প্রথম প্রকাশের পরে ভাষার আরও বিকাশের জন্য 1997 সালে একটি মূল দল গঠন করা হয়েছিল। পরবর্তী বছরগুলিতে অনেক আপডেট এবং পরিবর্তিত সংস্করণ প্রকাশ করা হয়েছিল এবং আধুনিক অপারেটিং সিস্টেম এবং প্রযুক্তি অনুসারে নতুন বৈশিষ্ট্যগুলি জড়িত ছিল। সাম্প্রতিক পরিবর্তনটি 2021 সালের মে মাসে চালু করা হয়েছিল।


## প্রযুক্তিগত স্পেসিফিকেশন ##

R একটি দোভাষী ভাষা এবং এই ভাষাটি অ্যাক্সেস করার জন্য একটি কমান্ড-লাইন দোভাষীর প্রয়োজন। যোগফলের মতো গণনা কমান্ড প্রচারে টাইপ করা হয় এবং ব্যাখ্যার পরে ফলাফল দেখানো হয়। ডেটা এবং কোড এস-এক্সপ্রেশনের মাধ্যমে উপস্থাপন করা হয়। এই ভাষার আরেকটি স্পেসিফিকেশন হল যে এটি একটি টুলবক্স হিসাবে পরিচালিত হতে পারে যা সাধারণ ম্যাট্রিক্স গণনার সুবিধা প্রদান করে।

R কোড চালানো এবং সম্পাদনা করতে বিভিন্ন অ্যাপ্লিকেশন ব্যবহার করা হয়। R প্রোগ্রামিং ভাষার কোড চালানোর জন্য Rattle GUI, RKWard এর মতো সমন্বিত উন্নয়ন পরিবেশও উপলব্ধ। মাইক্রোসফটের আর একটি সফ্টওয়্যার যা মাইক্রোসফ্ট আর ওপেন নামে পরিচিত, এটি মাল্টিথ্রেড কম্পিউটেশনের মতো জটিল গণনার জন্য R বিতরণের সাথে সামঞ্জস্যের সাথে উপলব্ধ। R হল বিশ্বের পাঁচটি নির্বাচিত প্রোগ্রামিং ভাষার মধ্যে একটি যা Apache Spark API নিয়ে গঠিত।

R ভাষা ফাংশন সহ পদ্ধতিগত প্রোগ্রামিং সমর্থন করে। যাইহোক, বিশেষত কিছু ফাংশনের জন্য, এটি জেনেরিক ফাংশনের সাথে ওওপি (অবজেক্ট-ওরিয়েন্টেড প্রোগ্রামিং) সমর্থন করে। মানগুলি আর্গুমেন্ট পাস করার জন্য ব্যবহার করা হয় যদি ফাংশনগুলি ব্যবহার করা হয় এবং তাদের মূল্যায়ন করা হয় যখন সেগুলি ব্যবহার করা হয়, যার অর্থ ফাংশনগুলিকে কল করার সময় তাদের মূল্যায়ন করা হয় না।

## R ফাইল ফরম্যাটের উদাহরণ ##

### বাক্য গঠন ###

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

### ফাংশন ###

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

### ডেটা মডেলিং

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

## রেফারেন্স ##

* [আর - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/R_(programming_language))




