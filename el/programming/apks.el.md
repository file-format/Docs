
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο APKS - Αρχείο συνόλου APK",
  "description":"Μάθετε για το τι είναι ένα αρχείο APKS;",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Τι είναι ένα αρχείο APKS;

Ένα αρχείο με επέκταση .apks είναι ένα αρχείο αρχειοθέτησης που είναι μια συλλογή αρχείων πακέτου Android **APK**. Κάθε μεμονωμένο αρχείο APK στο αρχείο APKS δημιουργείται έχοντας υπόψη διάφορες πτυχές των συσκευών. Αυτά περιλαμβάνουν την αρχιτεκτονική, τη γλώσσα, την πυκνότητα οθόνης και άλλες λειτουργίες της συσκευής. Τα αρχεία APKS δημιουργούνται από το **bundletool**. Χρησιμοποιείται για τη δημιουργία του Android App Bundle και τη μετατροπή του πακέτου εφαρμογών σε διαφορετικά APK για ανάπτυξη σε συσκευές.

## Μορφή αρχείου APKS - Περισσότερες πληροφορίες

Τα αρχεία APKS αποθηκεύονται ως συμπιεσμένα αρχεία χρησιμοποιώντας τη μορφή αρχείου [ZIP](/el/compression/zip/).

## Πώς να δημιουργήσετε ένα αρχείο APKS;

Όταν το Android App Bundle (AAB) είναι έτοιμο, η συμπεριφορά του στο Google Play store μπορεί να δοκιμαστεί για ανάπτυξη σε μια συσκευή. Τα αρχεία APKS μπορούν να δημιουργηθούν, για το σκοπό αυτό, από αρχεία AAB και να εγκατασταθούν σε συσκευές δοκιμής χρησιμοποιώντας το [bundletool] της Google (https://developer.android.com/studio/command-line/bundletool). Παρέχει εργαλεία γραμμής εντολών για τη δημιουργία του αρχείου αρχειοθέτησης APKS από APK χρησιμοποιώντας την ακόλουθη εντολή.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Για την ανάπτυξη των APK σε μια συσκευή, το αρχείο APKS μπορεί να υπογραφεί με τις πληροφορίες υπογραφής συσκευής ως εξής.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## βιβλιογραφικές αναφορές

* [bundletool - commandline](https://developer.android.com/studio/command-line/bundletool)

