---
date: 2019-10-11
keywords: scss, .scss, μορφή αρχείου scss, πώς να ανοίγετε αρχεία scss, συντακτικά φοβερό φύλλο στυλ, προεπεξεργαστής css, sass
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Μορφή αρχείου SCSS - Sass Cascading Style Sheet
linktitle: SCSS
description: "Μάθετε για τη μορφή αρχείου SCSS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Τι είναι ένα αρχείο SCSS; ##

Το SCSS είναι η δεύτερη σύνταξη του Sass (Syntactically Awesome Stylesheet) που χρησιμοποιεί αγκύλες αντί για εσοχές. Το SCSS σχεδιάστηκε με τέτοιο τρόπο ώστε ένα έγκυρο αρχείο CSS3 να είναι επίσης έγκυρο αρχείο SCSS. Τα αρχεία SCSS αποθηκεύονται με την επέκταση .scss.

## Γιατί να χρησιμοποιήσετε το SCSS ##

Καθώς τα σχέδια των ιστοσελίδων γίνονται πολύπλοκα με αποτέλεσμα μεγάλα αρχεία [CSS](/el/web/css/). Τέτοια αρχεία είναι πιο δύσκολο να διατηρηθούν. Εδώ μπαίνει το SCSS. Το SCSS εισάγει μεταβλητές, ένθεση, μίξεις, εισαγωγές και κληρονομικότητα επιλογέα στην ανάπτυξη CSS. Αυτές οι προσθήκες κάνουν την εργασία με το σχέδιο πολύ πιο διασκεδαστική.

## Πώς να χρησιμοποιήσετε αρχεία SCSS ##

Τα αρχεία SCSS δεν περιλαμβάνονται απευθείας στο έγγραφο [HTML](/el/web/html/), όπως το CSS. Αντίθετα, τα αρχεία SCSS μετατρέπονται σε αρχεία CSS που περιλαμβάνονται σε αρχεία HTML. Για να εγκαταστήσετε το SCSS στο σύστημά σας, ακολουθήστε τις οδηγίες που δίνονται στον [Επίσημο ιστότοπο Sass](https://sass-lang.com/install).
Για να μετατρέψετε το SCSS σε CSS, μπορείτε είτε να μετατρέψετε ένα ήδη αποθηκευμένο αρχείο SCSS ή να παρακολουθήσετε τις αλλαγές και να το μετατρέψετε καθώς το αρχείο αποθηκεύεται. Οι εντολές και για τα δύο δίνονται παρακάτω.

### Μετατροπή μία φορά ###

Η πρώτη παράμετρος είναι το αρχείο προέλευσης SCSS και η δεύτερη παράμετρος είναι το αρχείο CSS εξόδου.

```cmd
sass main.scss main.css
```

### Παρακολουθήστε τις αλλαγές ###

Η εντολή έχει μια πρόσθετη σημαία *watch** που διατηρεί την εντολή σε λειτουργία και μόλις αποθηκευτεί το αρχείο SCSS, δημιουργείται CSS εξόδου.

```cmd
sass --watch main.scss main.css
```

## Σύνταξη SCSS ##

Το SCSS υποστηρίζει μεταβλητές, ένθεση, μίξεις, εισαγωγές, κληρονομικότητα επιλογέα κ.λπ. Παρακάτω δίνονται παραδείγματα αυτών των δυνατοτήτων.

### Μεταβλητές ###

Με τη χρήση μεταβλητών, μπορείτε να ορίσετε επαναχρησιμοποιήσιμες πληροφορίες, όπως πρωτεύον χρώμα ή χρώμα φόντου για το κουμπί αποθήκευσης. Αυτό είναι χρήσιμο εάν πρέπει να αλλάξετε αυτές τις πληροφορίες, απλώς τις αλλάζετε σε μια τοποθεσία και ενημερώνεται όπου και αν χρησιμοποιείται.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Μπορείτε να τοποθετήσετε τους επιλογείς CSS παρόμοια με την ιεραρχία της HTML. Στο παράδειγμα που δίνεται παρακάτω, το διάστημα είναι ένθετο μέσα στο μπλοκ h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Τα μείγματα μπορούν να χρησιμοποιηθούν για την ομαδοποίηση παρόμοιων ιδιοτήτων που χρησιμοποιούνται μαζί σε πολλά μέρη. Μπορείτε επίσης να περάσετε παραμέτρους σε mixins.

**SCSS**

**Δήλωση μίξης**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Χρησιμοποιώντας ένα mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Το Extend/Inheritance είναι χρήσιμο σε περιπτώσεις όπου οι ιδιότητες ενός επιλογέα πρέπει να κοινοποιηθούν με έναν άλλο επιλογέα. Στο παρακάτω παράδειγμα, ο επιλογέας *.error-notice* λαμβάνει όλες τις ιδιότητες του επιλογέα *.error-text* και προσθέτει ιδιότητες περιγράμματος και συμπλήρωσης.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

Η εισαγωγή μπορεί να είναι χρήσιμη για τον διαχωρισμό των ανησυχιών. Μπορείτε να διαιρέσετε τα στυλ με τέτοιο τρόπο ώστε τα στυλ κεφαλίδας να βρίσκονται σε ξεχωριστό αρχείο, τα στυλ υποσέλιδου σε ξεχωριστό αρχείο, όλες οι μεταβλητές χρώματος που χρησιμοποιούνται στα στυλ μπορούν να βρίσκονται σε ξεχωριστό αρχείο κ.λπ. Χρησιμοποιώντας αυτήν την τεχνική, το τα στυλ παραμένουν οργανωμένα. Απλώς εισάγετε τα αρχεία στο κύριο αρχείο SCSS όπως φαίνεται στο παρακάτω παράδειγμα. Δεν χρειάζεται να καθορίσετε την επέκταση αρχείου στην οδηγία εισαγωγής. Το Sass μεταγλωττίζει απευθείας όλα τα αρχεία SCSS. Για να αποφύγετε την απευθείας μεταγλώττιση των αρχείων εισαγωγής, μπορείτε να τα κάνετε επιμέρους προσθέτοντας την υπογράμμιση(_) πριν από το όνομά τους. Μπορείτε να εισαγάγετε τμήματα παρόμοια με τα κανονικά αρχεία SCSS χωρίς την κάτω παύλα.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Το CSS εξόδου θα έχει τα στυλ από όλα τα εισαγόμενα αρχεία.

## Βιβλιογραφικές αναφορές ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

