{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "αρχείο", "επέκταση", "μορφή αρχείου", "βιβλιοθήκες του R", "Οδηγός προγραμματισμού", "r παράδειγμα", "κώδικας R", "βιβλιοθήκες του R", "Microsoft R" , "R code", "R language", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Αρχείο γλώσσας προγραμματισμού",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου R και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Τι είναι ένα αρχείο R;

Ένα αρχείο με επέκταση .r ανήκει στη γλώσσα προγραμματισμού R. Αυτή η γλώσσα έχει καθοριστεί για στατιστικούς υπολογισμούς και είναι δημοφιλής στην κοινότητα των στατιστικολόγων. Η ανάλυση δεδομένων και η ανάπτυξη στατιστικού λογισμικού είναι δύο κύριες κατηγορίες που πραγματοποιεί αυτή η γλώσσα στον τομέα της εξόρυξης δεδομένων. Ένα άλλο πλεονέκτημα της χρήσης αυτής της γλώσσας και του λογισμικού είναι ότι παρέχει τη δυνατότητα στατικών γραφημάτων που βοηθούν στην παραγωγή ποιοτικών γραφημάτων. Μερικά πρόσθετα πακέτα χρησιμοποιούνται για τα δυναμικά και διαδραστικά γραφικά.

Το λογισμικό αυτής της γλώσσας περιέχει μια Γενική Δημόσια Άδεια, επομένως η διαθεσιμότητά του είναι δωρεάν. Ο κώδικας του R είναι συνήθως γραμμένος σε γλώσσες υψηλού επιπέδου όπως [C](/el/programming/c/) και το ίδιο το R επίσης. Το λογισμικό περιλαμβάνει μια διεπαφή γραμμής εντολών μαζί με τη διαθεσιμότητα διεπαφών τρίτων, όπως γραφικές διεπαφές χρήστη του RStudio και του Jupyter (διεπαφή φορητού υπολογιστή). Υπάρχουν στατιστικές τεχνικές που χρησιμοποιούνται στην υλοποίηση βιβλιοθηκών του R. Περιλαμβάνει επίσης μοντελοποίηση όπως γραμμική και μη γραμμική.


## Σύντομη Ιστορία ##

Αυτή η γλώσσα είναι μια υλοποίηση της Σημασιολογίας του λεξικού πεδίου εφαρμογής μαζί με τη γλώσσα S. Το 1976 στα Bell Labs, ο John Chambers ανέπτυξε τη γλώσσα S. Ακόμη και δεν υπάρχει καμία αλλαγή σε μεγάλο μέρος του κώδικα του S-PLUS όταν χρησιμοποιείται στη γλώσσα R. Το 1995, ο Martin Maechler και οι σύντροφοί του έφτιαξαν τη γλώσσα R μαζί με το ελεύθερο λογισμικό με την άδεια γενικής χρήσης.

Η επίσημη ανακοίνωση του Comprehensive R Archive Network έγινε στις 23 Απριλίου 1997. Το 2000 η έκδοση 1. 0, που ήταν η πρώτη σταθερή beta, κυκλοφόρησε επίσημα. Η πρώτη του κυκλοφορία έγινε το 1995, ενώ το CRAN (περιεκτικό δίκτυο αρχείων R) κυκλοφόρησε τα επόμενα χρόνια.

Μια βασική ομάδα δημιουργήθηκε το 1997 για την περαιτέρω ανάπτυξη της γλώσσας μετά τις πρώτες κυκλοφορίες. Πολλές ενημερώσεις και τροποποιημένες εκδόσεις κυκλοφόρησαν τα τελευταία χρόνια και περιλάμβαναν νέα χαρακτηριστικά σύμφωνα με τα σύγχρονα λειτουργικά συστήματα και τεχνολογία. Η πρόσφατη τροποποίηση εισήχθη τον Μάιο του 2021.


## Τεχνική προδιαγραφή ##

Η R είναι μια γλώσσα διερμηνείας και απαιτείται διερμηνέας γραμμής εντολών για πρόσβαση σε αυτήν τη γλώσσα. Οι υπολογισμοί όπως το άθροισμα πληκτρολογούνται στην εντολή promo και τα αποτελέσματα εμφανίζονται μετά την ερμηνεία. Τα δεδομένα και ο κώδικας αντιπροσωπεύονται μέσω S-expressions. Μια άλλη προδιαγραφή αυτής της γλώσσας είναι ότι μπορεί να λειτουργήσει ως εργαλειοθήκη που παρέχει τη δυνατότητα υπολογισμού γενικού πίνακα.

Διάφορες εφαρμογές χρησιμοποιούνται για την εκτέλεση και την επεξεργασία του κώδικα R. Ενσωματωμένα περιβάλλοντα ανάπτυξης όπως το Rattle GUI, το RKWard είναι επίσης διαθέσιμα για την εκτέλεση του κώδικα της γλώσσας προγραμματισμού R. Ένα άλλο λογισμικό της Microsoft, γνωστό ως Microsoft R open, είναι επίσης διαθέσιμο με συμβατότητα με διανομή R για πολύπλοκους υπολογισμούς, όπως υπολογισμούς πολλαπλών νημάτων. Η R είναι μία από τις πέντε επιλεγμένες γλώσσες προγραμματισμού σε όλο τον κόσμο που περιλαμβάνουν το Apache Spark API.

Η γλώσσα R υποστηρίζει διαδικαστικό προγραμματισμό μαζί με τις λειτουργίες. Ωστόσο, ειδικά για ορισμένες λειτουργίες, υποστηρίζει OOP (αντικειμενοστραφή προγραμματισμό) μαζί με τις γενικές συναρτήσεις. Οι τιμές χρησιμοποιούνται για να περάσουν ορίσματα εάν οι συναρτήσεις και η αξιολόγησή τους πραγματοποιείται όταν χρησιμοποιούνται, πράγμα που σημαίνει ότι δεν αξιολογούνται όταν καλούνται συναρτήσεις.

## Παράδειγμα μορφής αρχείου R ##

### Σύνταξη ###

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

### Λειτουργία ###

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

### Μοντελοποίηση δεδομένων

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

## Αναφορά ##

* [R - από τη Wikipedia](https://en.wikipedia.org/wiki/R_(programming_language))



