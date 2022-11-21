{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο CSR - Μορφή αρχείου αιτήματος υπογραφής πιστοποιητικού",
  "description" :"Μάθετε τι είναι ένα αρχείο CSR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Τι είναι ένα αρχείο ΕΚΕ;

Ένα αρχείο CSR είναι ένα αρχείο **Αίτημα Υπογραφής Πιστοποιητικού** που χρησιμοποιείται για την αίτηση για πιστοποιητικό SSL/TLS. Όταν χρειάζεται να έχετε το πιστοποιητικό SSL/TLS, δημιουργείτε το CSR στον ίδιο διακομιστή όπου τελικά θα εγκατασταθεί. Αυτό το αρχείο CSR είναι κοινόχρηστο με την Αρχή έκδοσης πιστοποιητικών (CA) για τη δημιουργία του πιστοποιητικού. Περιέχει πληροφορίες όπως κοινό όνομα, οργανισμό, χώρα και, πιο σημαντικό, το **δημόσιο κλειδί** που είναι ενσωματωμένο στο αρχείο πιστοποιητικού σας και υπογράφεται με το αντίστοιχο ιδιωτικό κλειδί.

Οι εφαρμογές που μπορούν **να ανοίξουν αρχεία CSR** περιλαμβάνουν το OpenSSL και το Microsoft IIS.

## Μορφή αρχείου αιτήματος υπογραφής πιστοποιητικού

Δημιουργείται ένα αρχείο CSR σε μορφή PEM Base-64 που μπορεί να ανοίξει και να προβληθεί σε ένα απλό πρόγραμμα επεξεργασίας κειμένου όπως το Microsoft Notepad. Περιλαμβάνει μια κεφαλίδα **-----START ΑΙΤΗΣΗ ΝΕΟΥ ΠΙΣΤΟΠΟΙΗΤΙΚΟΥ-----** στην αρχή του αρχείου και ένα υποσέλιδο **-----ΤΕΛΟΣ ΑΙΤΗΣΗΣ ΝΕΟΥ ΠΙΣΤΟΠΟΙΗΣΗΣ-----** στο το τέλος του αρχείου.

### Πώς μοιάζει ένα αρχείο CSR;

Ένα απλό παράδειγμα αρχείου CSR είναι το ακόλουθο.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## Ποιες πληροφορίες περιλαμβάνονται σε μια ΕΚΕ;

Ένα αρχείο CSR περιέχει τις ακόλουθες πληροφορίες.

1. «Πληροφορίες σχετικά με την επιχείρηση και τον ιστότοπο» - Περιλαμβάνει πληροφορίες όπως Κοινό όνομα, Οργανισμός, Οργανωτική Μονάδα, Πόλη/Τοποθεσία, Πολιτεία/Κομητεία/Περιοχή (S), Χώρα και διεύθυνση ηλεκτρονικού ταχυδρομείου
1. «Δημόσιο κλειδί» - Περιλαμβάνεται στο πιστοποιητικό και χρησιμοποιείται για την κρυπτογράφηση μεταδιδόμενων δεδομένων τα οποία αποκρυπτογραφούνται χρησιμοποιώντας το αντίστοιχο ιδιωτικό κλειδί
1. "Πληροφορίες σχετικά με τον τύπο και το μήκος κλειδιού" - Αυτό είναι συνήθως RSA 2048 αλλά μπορεί επίσης να διατίθεται σε μεγαλύτερα μεγέθη όπως RSA 4096+

## βιβλιογραφικές αναφορές

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

