{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο PEM - Μορφή αρχείου πιστοποιητικού αλληλογραφίας ενισχυμένου απορρήτου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PEM και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Τι είναι ένα αρχείο PEM;

Ένα αρχείο PEM είναι ένα αρχείο πιστοποιητικού ασφαλείας που χρησιμοποιείται για τη δημιουργία ενός ασφαλούς καναλιού επικοινωνίας μεταξύ ενός διακομιστή web και ενός προγράμματος περιήγησης. Έχει κωδικοποίηση Base64 και μπορεί να περιέχει ιδιωτικό κλειδί, πιστοποιητικό διακομιστή ή/και συνδυασμό άλλων πιστοποιητικών. Τα αρχεία PEM είναι παρόμοια με τα αρχεία πιστοποιητικού .der όσον αφορά τη χρήση, αλλά αποθηκεύονται ως κείμενο με κωδικοποίηση Base64 και όχι ως δυαδικά δεδομένα. Άλλες παρόμοιες μορφές αρχείων πιστοποιητικού περιλαμβάνουν αρχεία [.cer](/el/web/cer/) και [.crt](/el/web/crt/).

Οι εφαρμογές που μπορούν **να ανοίξουν αρχεία PEM** περιλαμβάνουν προγράμματα επεξεργασίας κειμένου όπως το Microsoft Notepad και το Apple TextEdit.

## Μορφή αρχείου PEM

Το PEM είναι μια μορφή αρχείου κοντέινερ που καθορίζει τη δομή και τον τύπο κωδικοποίησης του αρχείου που χρησιμοποιείται για την αποθήκευση των δεδομένων. Τα αρχεία PEM αποθηκεύονται σε δίσκο ως μορφή αρχείου με κωδικοποίηση Base64 που δεν είναι αναγνώσιμη από τον άνθρωπο. Το πρότυπο ορίζει ότι ένα αρχείο PEM ξεκινά με:

```
-----BEGIN <type>-----
```
και τελειώνει με:
```
-----END <type>-----
```

Όλο το άλλο περιεχόμενο σε αυτά είναι κωδικοποιημένο με βάση 64 (κεφαλαία και πεζά γράμματα, ψηφία, + και /). Ένα μόνο αρχείο PEM μπορεί να αποτελείται από πολλά μπλοκ τα οποία μπορούν να χρησιμοποιηθούν από άλλα προγράμματα. Εάν ένα αρχείο PEM περιέχει πολλά πιστοποιητικά, κάθε πιστοποιητικό διαχωρίζεται από μεμονωμένα μπλοκ ως εξής:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Παράδειγμα αρχείου PEM

Ένα αρχείο PEM με μπλοκ CERTIFICATE έχει συνήθως την εξής μορφή:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Ένα αρχείο PEM με RSA ξεκινά όπως ακολουθεί.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Βιβλιογραφικές αναφορές ##

* [Κρυπτογραφία δημόσιου κλειδιού](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Πώς να δημιουργήσω αρχείο P7C;](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

