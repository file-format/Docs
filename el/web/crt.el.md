{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "crt αρχείο", "μορφή αρχείου crt", "τύπος αρχείου crt", "αρχείο", "τύπος", "τι είναι ένα αρχείο crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Μορφή αρχείου πιστοποιητικού ασφαλείας",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CRT και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο CRT;

Ένα αρχείο με επέκταση .crt είναι ένα αρχείο πιστοποιητικού ασφαλείας που χρησιμοποιείται από ασφαλείς ιστότοπους για τη δημιουργία ασφαλών συνδέσεων από διακομιστή ιστού σε πρόγραμμα περιήγησης. Οι ασφαλείς ιστότοποι καθιστούν δυνατή την ασφάλεια των μεταφορών δεδομένων, των συνδέσεων, των συναλλαγών με κάρτες πληρωμών και την παροχή προστατευμένης περιήγησης στον ιστότοπο. Εάν ανοίξετε έναν ασφαλή ιστότοπο, θα δείτε ένα εικονίδιο "κλειδώματος" στη γραμμή διευθύνσεων. Εάν κάνετε κλικ σε αυτό, μπορείτε να δείτε τις λεπτομέρειες του εγκατεστημένου πιστοποιητικού. Διεθνείς εταιρείες όπως η Verisign και η Thawte διανέμουν αυτά τα πιστοποιητικά SSL.

## Μορφή αρχείου CRT

Τα αρχεία CRT είναι σε μορφή ASCII και μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου για να προβάλετε τα περιεχόμενα του αρχείου πιστοποιητικού. Ακολουθεί το πρότυπο πιστοποίησης X.509 που καθορίζει τη δομή του πιστοποιητικού. Καθορίζει τα πεδία δεδομένων που πρέπει να περιλαμβάνονται στο πιστοποιητικό SSL. Το CRT ανήκει στη μορφή PEM των πιστοποιητικών που είναι αρχεία με κωδικοποίηση ASCII Base64.

### Δομή αρχείου PEM

Ένα αρχείο PEM μπορεί να έχει πολλαπλά πιστοποιητικά. Σε μια τέτοια περίπτωση, κάθε πιστοποιητικό στο αρχείο PEM ακολουθεί την ακόλουθη δομή.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Παράδειγμα μορφής αρχείου CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Βιβλιογραφικές αναφορές ##

* [Δημόσια κλειδιά, ιδιωτικά κλειδιά και πιστοποιητικά](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

