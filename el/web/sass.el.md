---
date: 2019-10-11
keywords: sass, .sass, μορφή αρχείου sass, πώς να ανοίξετε αρχεία sass, συντακτικά φοβερό φύλλο στυλ, προεπεξεργαστής css, sass
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Μορφή αρχείου Sass
linktitle: Sass
description: "Μάθετε για τη μορφή αρχείου Sass και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Τι είναι ένα αρχείο SASS; ##

Το Sass (συντακτικά φοβερά φύλλα στυλ) είναι μια γλώσσα προγραμματισμού προεπεξεργαστή. Μεταγλωττίζεται σε [CSS](/el/web/css/) και αποθηκεύεται με την επέκταση .sass. Το Sass αποτελείται από δύο συντάξεις, το πρωτότυπο που βασίζεται σε εσοχές που χρησιμοποιεί την επέκταση .sass και το νεότερο SCSS με μορφοποίηση μπλοκ όπως το CSS που χρησιμοποιεί την επέκταση .scss.

## Γιατί να χρησιμοποιήσετε το Sass ##

Το Sass είναι πραγματικά χρήσιμο στη διατήρηση στυλ, καθώς παρέχει πολλές δυνατότητες, όπως εισάγει μεταβλητές, ένθεση, μίξεις, εισαγωγές και κληρονομικότητα επιλογέα που κάνουν την εργασία με στυλ διασκεδαστική.

## Πώς να χρησιμοποιήσετε αρχεία SASS ##

Τα αρχεία SASS δεν περιλαμβάνονται απευθείας στο έγγραφο [HTML](/el/web/html/), αλλά μάλλον μετατρέπονται σε αρχεία CSS που περιλαμβάνονται σε αρχεία HTML. Μπορείτε να εγκαταστήσετε το Sass του συστήματός σας ακολουθώντας τις οδηγίες που δίνονται στον [Επίσημο ιστότοπο Sass](https://sass-lang.com/install).

Το Sass μπορεί να μετατραπεί σε CSS είτε μετατρέποντας ένα ήδη αποθηκευμένο αρχείο SASS είτε παρακολουθώντας τις αλλαγές και μετατρέποντας καθώς αποθηκεύεται το αρχείο. Οι εντολές και για τα δύο δίνονται παρακάτω.

### Μετατροπή μία φορά ###

Η πρώτη παράμετρος της εντολής είναι το αρχείο προέλευσης SASS και η δεύτερη παράμετρος είναι το αρχείο CSS εξόδου.

```cmd
sass main.sass main.css
```

### Παρακολουθήστε τις αλλαγές ###

Η παραπάνω εντολή μπορεί να εκτελεστεί με μια πρόσθετη σημαία *watch* που διατηρεί την εντολή σε λειτουργία και μόλις αποθηκευτεί το αρχείο Sass, δημιουργείται CSS εξόδου.

```cmd
sass --watch main.sass main.css
```

## Sass Σύνταξη ##

Το Sass υποστηρίζει μεταβλητές, ένθεση, mixins, εισαγωγές, κληρονομικότητα επιλογέα κ.λπ. Παρακάτω δίνονται παραδείγματα αυτών των δυνατοτήτων.

### Μεταβλητές ###

Οι μεταβλητές μπορούν να χρησιμοποιηθούν για τον ορισμό επαναχρησιμοποιήσιμων πληροφοριών, όπως το κύριο χρώμα ή το padding για ένα κουμπί. Αυτό μπορεί να αποδειχθεί χρήσιμο εάν στο μέλλον χρειαστεί να αλλάξετε αυτές τις πληροφορίες, απλώς τις αλλάξετε σε μια τοποθεσία και ενημερώνεται παντού.

**Σας**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**Δημιουργήθηκε CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Ένθεση ###

Οι επιλογείς CSS μπορούν να είναι ένθετοι παρόμοια με την ιεραρχία της HTML. Στο ακόλουθο παράδειγμα, το διάστημα είναι ένθετο μέσα στο μπλοκ h1.

**Σας**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**Δημιουργήθηκε CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Μίξεις ###

Τα μείγματα χρησιμοποιούνται για την ομαδοποίηση παρόμοιων ιδιοτήτων που χρησιμοποιούνται σε πολλά μέρη. Τα μείγματα υποστηρίζουν επίσης παραμέτρους.

**Σας**

**Δήλωση μίξης**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Χρησιμοποιώντας ένα mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Δημιουργήθηκε CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Επέκταση ###

Το Extend/Inheritance μπορεί να αποδειχθεί χρήσιμο σε περιπτώσεις όπου οι ιδιότητες ενός επιλογέα πρέπει να κοινοποιηθούν με έναν άλλο επιλογέα. Στο παρακάτω παράδειγμα, ο επιλογέας *.error-notice* λαμβάνει όλες τις ιδιότητες του επιλογέα *.error-text* και προσθέτει ιδιότητες περιγράμματος και padding.

**Σας**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**Δημιουργήθηκε CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Εισαγωγή ###

Η εισαγωγή μπορεί να είναι χρήσιμη εάν δομείτε τα στυλ σας σε διαφορετικά αρχεία με βάση τη λειτουργικότητα ή οποιαδήποτε άλλη δομή που ακολουθείτε. Μπορείτε να εισαγάγετε όλα αυτά τα αρχεία σε ένα πρωτεύον αρχείο SASS που αργότερα θα μετατραπεί σε CSS. Κατά την εισαγωγή, δεν χρειάζεται να καθορίσετε την επέκταση αρχείου στην οδηγία εισαγωγής. Το Sass μεταγλωττίζει απευθείας όλα τα αρχεία SASS. Για να αποφύγετε την απευθείας μεταγλώττιση αρχείων εισαγωγής, μπορείτε να τα κάνετε επιμέρους προσθέτοντας την υπογράμμιση(_) στην αρχή του ονόματός τους. Τα τμήματα εισάγονται παρόμοια με τα κανονικά αρχεία Sass.

**Σας**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Το CSS εξόδου θα έχει τα στυλ από όλα τα εισαγόμενα αρχεία.

## Βιβλιογραφικές αναφορές ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

