---
date: 2019-10-11
keywords: js, .js, μορφή αρχείου js, πώς να ανοίξετε αρχεία js, αρχεία javascript
συγγραφέας:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Μορφή αρχείου JS
linktitle: JS
description: "Μάθετε για τη μορφή αρχείου JS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Τι είναι ένα αρχείο JS; ##

Τα JS (JavaScript) είναι αρχεία που περιέχουν κώδικα JavaScript για εκτέλεση σε ιστοσελίδες. Τα αρχεία JavaScript αποθηκεύονται με την επέκταση .js. Μέσα στο έγγραφο [HTML](/el/web/html/), μπορείτε είτε να ενσωματώσετε τον κώδικα JavaScript χρησιμοποιώντας το \ <script>\</script> ετικέτες ή συμπεριλάβετε ένα αρχείο JS. Παρόμοια με τα αρχεία [CSS](/el/web/css/), τα αρχεία JS μπορούν να συμπεριληφθούν σε πολλά έγγραφα HTML για επαναχρησιμοποίηση κώδικα. Η JavaScript μπορεί να χρησιμοποιηθεί για τον χειρισμό του HTML DOM.

## Σύντομη Ιστορία ##

Η JavaScript κυκλοφόρησε για πρώτη φορά ως μέρος του προγράμματος περιήγησης Navigator τον Σεπτέμβριο του 1995 με το όνομα LiveScript από τη Netscape. Τρεις μήνες αργότερα μετονομάστηκε σε JavaScript. Το 1996, η Microsoft αναμόρφωσε τον διερμηνέα του Navigator για τη δημιουργία JScript. Το JScript κυκλοφόρησε με τον Internet Explorer και ήταν πολύ διαφορετικό από το JavaScript.

Η Netscape υπέβαλε JavaScript στην ECMA International που οδήγησε στην επίσημη κυκλοφορία της πρώτης προδιαγραφής ECMAScript το 1997. Το ECMAScript 2 κυκλοφόρησε το 1998, το ECMAScript 3 το 1999 και οι εργασίες για το ECMAScript 4 ξεκίνησαν το 2000 αλλά δεν ολοκληρώθηκαν ποτέ.

Ο Jesse James Garrett το 2005 κυκλοφόρησε μια λευκή βίβλο όπου επινόησε τον όρο *Ajax*. Αυτό χρησιμοποίησε τη JavaScript ως βάση για τη δημιουργία εφαρμογών ιστού που φορτώνουν δεδομένα στο παρασκήνιο και αποφεύγουν τις επαναφορτώσεις πλήρους σελίδας. Αυτό είχε ως αποτέλεσμα τη δημιουργία βιβλιοθηκών όπως JQuery, Prototype, Dojo κ.λπ.

Η Google κυκλοφόρησε το πρόγραμμα περιήγησης Chrome με τη μηχανή JavaScript V8 το 2008. Στις αρχές του 2009, συνήφθη συμφωνία για τον συνδυασμό όλων των σχετικών εργασιών και την προώθηση της JavaScript. Αυτό είχε ως αποτέλεσμα την κυκλοφορία του προτύπου ECMAScript 5 τον Δεκέμβριο του 2009.

## Πώς να χρησιμοποιήσετε τα αρχεία JS ##

Για να χρησιμοποιήσετε ένα αρχείο JS, το συμπεριλάβετε στο έγγραφο HTML. Χρησιμοποιείτε την ετικέτα συνδέσμου για να συμπεριλάβετε το αρχείο όπως φαίνεται παρακάτω.

```html
<script src="site.js"></script>
```

Το χαρακτηριστικό *src* της ετικέτας *script* περιέχει τη διαδρομή προς το αρχείο JS. Με αυτόν τον τρόπο, η λειτουργικότητα JS προστίθεται στο έγγραφο HTML.

## Σύνταξη JS ##

Τα αρχεία JavaScript μπορεί να περιέχουν μεταβλητές, τελεστές, συναρτήσεις, συνθήκες, βρόχους, πίνακες, αντικείμενα κ.λπ. Παρακάτω δίνεται μια σύντομη επισκόπηση της σύνταξης της JavaScript.

- Κάθε εντολή τελειώνει με ερωτηματικό(;).
- Χρησιμοποιήστε τη λέξη-κλειδί *var* για να δηλώσετε μεταβλητές.
- Υποστηρίζει αριθμητικούς τελεστές ( + - * / ) για τον υπολογισμό τιμών.
- Τα σχόλια μιας γραμμής προστίθενται με // και τα σχόλια πολλαπλών γραμμών περιβάλλονται από /* και */.
- Όλα τα αναγνωριστικά έχουν διάκριση πεζών-κεφαλαίων, δηλαδή *modelNo* και *modelno* είναι δύο διαφορετικές μεταβλητές.
- Οι συναρτήσεις ορίζονται χρησιμοποιώντας τη λέξη-κλειδί *function*.
- Οι πίνακες μπορούν να οριστούν χρησιμοποιώντας αγκύλες [].
- Το JS υποστηρίζει τελεστές σύγκρισης όπως ==, != , >=, !==, κ.λπ.
- Οι τάξεις μπορούν να οριστούν χρησιμοποιώντας τη λέξη-κλειδί *class*.

## Παράδειγμα χρήσης JS ##

Το παρακάτω δείχνει ένα απλό παράδειγμα χρήσης αρχείου JavaScript.

### Έγγραφο HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Κωδικός JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Βιβλιογραφικές αναφορές ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

