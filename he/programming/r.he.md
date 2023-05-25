{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "קובץ", "הרחבה", "פורמט קובץ", "ספריות של R", "מדריך תכנות", "דוגמה של R", "קוד של R", "ספריות של R", "Microsoft R" , "R code", "R language", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - קובץ שפת תכנות",
  "description":"למד על פורמט קובץ R וממשקי API שיכולים ליצור ולפתוח קבצי R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## מהו קובץ R?

קובץ עם סיומת .r שייך לשפת התכנות R. שפה זו מוגדרת עבור מחשוב סטטיסטי והיא פופולרית בקרב קהילת הסטטיסטיקאים. ניתוח נתונים ופיתוח תוכנות סטטיסטיות הן שתי קטגוריות עיקריות המבוצעות על ידי שפה זו בתחום כריית הנתונים. יתרון נוסף בשימוש בשפה ובתוכנה זו הוא בכך שהיא מספקת את המתקן של גרפים סטטיים אשר מועילים בהפקת גרפים איכותיים. כמה חבילות נוספות משמשות עבור הגרפיקה הדינמית והאינטראקטיבית.

התוכנה של שפה זו מכילה רישיון ציבורי כללי כך שהזמינות שלה היא בחינם. הקוד של R נכתב בדרך כלל בשפות ברמה גבוהה כמו [C](/he/programming/c/) וגם R עצמו. התוכנה כוללת ממשק שורת פקודה יחד עם זמינות ממשקי צד שלישי כגון ממשקי משתמש גרפיים של RStudio ו-Jupyter (ממשק מחברת). ישנן טכניקות סטטיסטיות בשימוש ביישום ספריות של R. זה כולל גם מודלים כמו ליניארי ולא ליניארי.


## היסטוריה קצרה ##

שפה זו היא יישום של סמנטיקה של היקף מילוני יחד עם שפת S. בשנת 1976 ב-Bell Labs, ג'ון צ'יימברס פיתח את שפת S. אפילו אין שינוי בחלק גדול מהקוד של S-PLUS כאשר נעשה שימוש בשפת R. בשנת 1995, מרטין מייקלר וחבריו יצרו את שפת R יחד עם התוכנה החינמית תחת רישיון הציבור הכללי.

ההכרזה הרשמית של Comprehensive R Archive Network פורסמה ב-23 באפריל 1997. בשנת 2000 שוחררה רשמית גרסה 1.0, שהייתה הבטא היציבה הראשונה. השחרור הראשון שלו התרחש בשנת 1995, בזמן ש-CRAN (רשת ארכיון R מקיפה) שוחררה בשנים מאוחרות יותר.

צוות ליבה הוקם בשנת 1997 להמשך פיתוח השפה לאחר השחרורים הראשונים. עדכונים רבים וגרסאות שונו שוחררו בשנים מאוחרות יותר וכללו תכונות חדשות בהתאם למערכות הפעלה וטכנולוגיה מודרניים. השינוי האחרון הוצג במאי 2021.


## מפרט טכני ##

R היא שפה מתורגמת ונדרש מתורגמן בשורת פקודה כדי לגשת לשפה זו. החישובים כמו סכום מוקלדים בפרומו הפקודה והתוצאות מוצגות לאחר פירוש. נתונים וקוד מיוצגים באמצעות ביטויי S. מפרט נוסף של שפה זו הוא שניתן להפעיל אותה כארגז כלים המספק את המתקן של חישוב מטריצות כללי.

יישומים שונים משמשים להפעלה ועריכה של קוד R. סביבות פיתוח משולבות כגון Rattle GUI, RKWard זמינות גם להפעלת הקוד של שפת התכנות R. תוכנה נוספת של מיקרוסופט המכונה Microsoft R open זמינה גם היא עם תאימות להפצת R עבור חישובים מורכבים כגון חישובים מרובי-הליכים. R היא אחת מחמש שפות התכנות הנבחרות ברחבי העולם המרכיבות את Apache Spark API.

שפת R תומכת בתכנות פרוצדורלי יחד עם הפונקציות. עם זאת, עבור פונקציות מסוימות במיוחד, הוא תומך ב-OOP (תכנות מונחה עצמים) יחד עם הפונקציות הגנריות. ערכים משמשים להעברת ארגומנטים אם פונקציות והערכתן מתרחשות כאשר נעשה בהן שימוש, מה שאומר שהם לא מוערכים כאשר פונקציות נקראות.

## דוגמה לפורמט קובץ R ##

### תחביר ###

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

### פונקציה ###

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

### מודל נתונים

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

## התייחסות ##

* [R - מאת ויקיפדיה](https://en.wikipedia.org/wiki/R_(programming_language))



