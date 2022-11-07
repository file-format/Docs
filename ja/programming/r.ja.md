{
  "date" : "2021-09-06", 
  "keywords" :[ "R","ファイル","拡張子","ファイル形式","R のライブラリ","プログラミング ガイド","r の例","R のコード","R のライブラリ","Microsoft R" ,"R コード","R 言語","RStudio"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - プログラミング言語ファイル",
  "description":"R ファイル形式と,R ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## R ファイルとは何ですか?

拡張子が .r のファイルは、プログラミング言語 R に属します。この言語は、統計計算用に指定されており、統計学者のコミュニティで人気があります。データ分析と統計ソフトウェアの開発は、データ マイニングの分野でこの言語によって実行される 2 つの主要なカテゴリです。この言語とソフトウェアを使用するもう 1 つの利点は、高品質のグラフの作成に役立つ静的グラフの機能を提供することです。動的でインタラクティブなグラフィックには、いくつかの追加パッケージが使用されます。

この言語のソフトウェアには General Public License が含まれているため、無料で利用できます。 R のコードは通常、[C](/programming/c/) や R 自体などの高級言語で記述されます。このソフトウェアには、RStudio や Jupyter のグラフィカル ユーザー インターフェイス (ノートブック インターフェイス) などのサードパーティ インターフェイスの可用性に加えて、コマンドライン インターフェイスが含まれます。 R のライブラリの実装で使用される統計手法があります。これには、線形や非線形などのモデリングも含まれます。


## 簡単な歴史 ##

この言語は、S 言語とともにレキシカル スコープのセマンティクスを実装したものです。 1976 年、ベル研究所でジョン・チェンバーズが S 言語を開発しました。 R 言語で使用する場合でも、S-PLUS のコードの大部分は変更されていません。 1995 年、Martin Maechler と彼の仲間は、一般公有ライセンスの下でフリー ソフトウェアと共に R 言語を作成しました。

Comprehensive R Archive Network の公式発表は、1997 年 4 月 23 日に行われました。2000 年には、最初の安定ベータ版であるバージョン 1.0 が正式にリリースされました。最初のリリースは 1995 年に行われ、CRAN (包括的な R アーカイブ ネットワーク) は後年リリースされました。

最初のリリース後の言語のさらなる開発のために、1997 年にコア チームが結成されました。後年、多くの更新と修正版がリリースされ、最新のオペレーティング システムとテクノロジに応じた新機能が含まれていました。最近の変更は、2021 年 5 月に導入されました。


## 技術仕様 ##

R はインタープリター言語であり、この言語にアクセスするにはコマンドライン インタープリターが必要です。 sum などの計算はコマンド promo に入力され、解釈後に結果が表示されます。データとコードは S 式で表されます。この言語のもう 1 つの仕様は、一般的な行列計算の機能を提供するツールボックスとして操作できることです。

R コードの実行と編集には、さまざまなアプリケーションが使用されます。 R プログラミング言語のコードを実行するために、Rattle GUI、RKWard などの統合開発環境も利用できます。 Microsoft R open として知られる Microsoft の別のソフトウェアも、マルチスレッド計算などの複雑な計算用の R ディストリビューションと互換性があります。 R は、Apache Spark API を構成する、世界中で選ばれた 5 つのプログラミング言語の 1 つです。

R言語は、関数とともに手続き型プログラミングをサポートしています。ただし、特に一部の関数については、汎用関数とともに OOP (オブジェクト指向プログラミング) をサポートしています。関数とその評価が使用時に行われる場合、引数を渡すために値が使用されます。つまり、関数が呼び出されているときに評価されません。

## R ファイル形式の例 ##

### 構文 ###

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

＃＃＃ 関数 ＃＃＃

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

### データモデリング

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

## 参照 ＃＃

* [R - ウィキペディアによる](https://en.wikipedia.org/wiki/R_(programming_language))



