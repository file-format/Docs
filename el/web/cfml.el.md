{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion Markup Language File",
  "description" :"Μάθετε για το τι είναι ένα αρχείο CFML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Τι είναι ένα αρχείο CFML;

Ένα αρχείο με επέκταση .cfml είναι ένα αρχείο ColdFusion Markup Language που χρησιμοποιείται για τη δημιουργία ιστοσελίδας. Αναφέρεται σε ένα σύνολο κανόνων που χρησιμοποιούνται για τον καθορισμό του τρόπου με τον οποίο θα αναπτυχθεί η εφαρμογή ColdFusion από τον προγραμματιστή. Η ColdFusion είναι μια γλώσσα προγραμματισμού που χρησιμοποιείται για τη δημιουργία εφαρμογών ιστού γρήγορα και με λιγότερες από άλλες τεχνολογίες όπως [ASP](/el/web/asp/), [PHP](/el/programming/php/), κ.λπ. από τις εφαρμογές που μπορούν να ανοίξουν αρχεία CML περιλαμβάνουν το Adobe ColdFusion 2018, το Adobe ColdFusion Builder και το Adobe Dreamweaver.

## Μορφή αρχείου CFML - Περισσότερες πληροφορίες

Τα αρχεία CFML είναι αρχεία σήμανσης και περιέχουν στοιχεία ιστού με τη μορφή ετικετών. Αυτά είναι αρχεία κειμένου που μπορούν να ανοίξουν και να επεξεργαστούν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Τα αρχεία CFML αποτελούνται από πολλές ετικέτες που είναι παρόμοιες με [HTML](/el/web/html/) και συνήθως αποτελούνται από μια ετικέτα ανοίγματος και μια ετικέτα κλεισίματος. Αυτές οι ετικέτες μπορούν επίσης να περιέχουν ένα ή περισσότερα χαρακτηριστικά.

### Ετικέτες Σύνταξη

Ακολουθεί η γενικευμένη σύνταξη των ετικετών CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Οι περισσότερες ετικέτες δέχονται χαρακτηριστικά και ορίζονται ως εξής.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Ορισμένες από αυτές τις ετικέτες δέχονται επίσης πολλαπλά χαρακτηριστικά με την ακόλουθη σύνταξη.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Παράδειγμα κώδικα CFML

Ακολουθεί ένα παράδειγμα που χρησιμοποιεί μια πραγματική ετικέτα CFML - την ετικέτα "cfoutput":

```
<cfoutput>
  #firstname#
</cfoutput>
```

## βιβλιογραφικές αναφορές

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

