{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 Certificate File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου P7C και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο P7C;

Ένα αρχείο P7C, όπως και άλλα αρχεία πιστοποιητικού ασφαλείας, είναι ένα ψηφιακό πιστοποιητικό που χρησιμοποιείται για τον έλεγχο ταυτότητας μέσω του δικτύου. Οι εφαρμογές που χρησιμοποιούν πιστοποιητικά ελέγχουν ταυτότητα χρησιμοποιώντας το δημόσιο κλειδί που περιλαμβάνεται σε αυτά τα αρχεία πιστοποιητικών. Η κρυπτογραφία δημόσιου κλειδιού, ή η ασύμμετρη κρυπτογραφία, χρησιμοποιεί ζεύγος κλειδιών από τα οποία το ένα είναι το δημόσιο κλειδί και το άλλο είναι γνωστό ως ιδιωτικό κλειδί. Το ιδιωτικό κλειδί διατηρείται ασφαλές για αποτελεσματική ασφάλεια, ενώ το δημόσιο κλειδί μπορεί να μοιραστεί με άλλους. Άλλες κοινές μορφές αρχείων πιστοποιητικού περιλαμβάνουν [CRT](/el/web/crt/), DER και PEM.

## Μορφή αρχείου P7C - Περισσότερες πληροφορίες

Τα αρχεία P7C αποθηκεύονται σε δίσκο ως δυαδικά αρχεία και περιλαμβάνουν τις πληροφορίες του δημόσιου κλειδιού που δημιουργούνται με χρήση κρυπτογραφικών αλγορίθμων που βασίζονται σε μαθηματικά προβλήματα. Αυτά μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου, αλλά το περιεχόμενό τους δεν είναι σε μορφή αναγνώσιμη από τον άνθρωπο. Μερικές από τις εφαρμογές που μπορούν να ανοίξουν αρχεία P7C περιλαμβάνουν Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager και Microsoft Windows Contacts.

### Παράδειγμα μορφής αρχείου P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Βιβλιογραφικές αναφορές ##

* [Κρυπτογραφία δημόσιου κλειδιού](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Πώς να δημιουργήσω αρχείο P7C;](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

