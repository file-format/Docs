{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 Certificate File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου P7C και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο P7B;

Ένα αρχείο P7B είναι ένα αρχείο πιστοποιητικού ασφαλείας που περιέχει ασφαλές ψηφιακό πιστοποιητικό για τον έλεγχο ταυτότητας ενός ατόμου ή μιας συσκευής. Παρόμοια με ένα αρχείο πιστοποιητικού [.cer](/el/web/cer/), ένα αρχείο P7B μπορεί να εγκατασταθεί χρησιμοποιώντας την επιλογή "Εγκατάσταση πιστοποιητικού" χρησιμοποιώντας την επιλογή δεξί κλικ στο αρχείο. Το P7B χρησιμοποιεί διαφορετική επιλογή μορφοποίησης από τη μορφή αρχείου CER. Περιέχει ένα ή περισσότερα αρχεία ψηφιακών πιστοποιητικών X.509 που χρησιμοποιούν κωδικοποίηση base64 (ASCII). Τα αρχεία P7B λαμβάνονται ως αρχείο [ZIP](/el/compression/zip/) ή λαμβάνονται από την Αρχή έκδοσης πιστοποιητικών.

## Μορφή αρχείου P7B

Τα αρχεία P7B αποθηκεύονται ως απλά αρχεία ASCII που μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Περιέχει το δημόσιο κλειδί που είναι μια κωδικοποιημένη συμβολοσειρά που δεν έχει νόημα από την άποψη της αναγνωσιμότητας.

### Παράδειγμα μορφής αρχείου P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Βιβλιογραφικές αναφορές ##

* [Κρυπτογραφία δημόσιου κλειδιού](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Πώς να δημιουργήσω αρχείο P7C;](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

