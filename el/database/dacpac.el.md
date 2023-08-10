{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "Πακέτο εφαρμογής επιπέδου δεδομένων" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου DACPAC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DACPAC.",
  "title" :"DACPAC - Πακέτο Εφαρμογής Επιπέδου Δεδομένων",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Τι είναι ένα αρχείο DACPAC;

Ένα αρχείο με επέκταση .dacpac (αντιπροσωπεύει Data Tier AppliCation Package) είναι ένα αρχείο βάσης δεδομένων, που δημιουργήθηκε με την εφαρμογή επιπέδου δεδομένων του Microsoft SQL Server, το οποίο περιέχει το μοντέλο βάσης δεδομένων για την αναπαράσταση αντικειμένων βάσης δεδομένων. Καθώς περιέχει το πλήρες μοντέλο της βάσης δεδομένων, χρησιμοποιείται για την επαναφορά μιας βάσης δεδομένων από τις λεπτομέρειες που είναι διαθέσιμες στο μοντέλο. Τα αρχεία DACPAC συνήθως παραδίδονται σε ομάδες ανάπτυξης για εγκατάσταση στις εγκαταστάσεις του πελάτη για επαναφορά της βάσης δεδομένων. Αυτά μπορούν να ανοίξουν με
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Μορφή αρχείου DACPAC - Περισσότερες πληροφορίες

Τα αρχεία πακέτου δεδομένων DACPAC είναι στην πραγματικότητα συμπιεσμένα αρχεία ZIP που περιέχουν πολλά αρχεία [XML](/el/web/xml/) που περιέχουν πληροφορίες σχετικά με το μοντέλο της βάσης δεδομένων, όπως πίνακες και προβολές, που χρησιμοποιούνται για την επαναφορά μιας βάσης δεδομένων. Για να δείτε τα περιεχόμενα των αρχείων DACPAC, μετονομάστε τα αρχεία από .dacpac σε [.zip](/el/compression/zip/) και εξαγάγετε το αρχείο zip χρησιμοποιώντας οποιοδήποτε βοηθητικό πρόγραμμα αποσυμπίεσης.

Ακολουθούν μερικά αρχεία που βρίσκονται μέσα σε ένα αρχείο DACPAC.

* [Τύποι_Περιεχομένου].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* model.xml

Πρέπει να σημειωθεί ότι το DACPAC δεν περιέχει DATA και άλλα αντικείμενα σε επίπεδο διακομιστή. Το αρχείο μπορεί να περιέχει όλους τους τύπους αντικειμένων που μπορεί να διατηρηθούν στο έργο SSDT.

## βιβλιογραφικές αναφορές

* [Εφαρμογές επιπέδου δεδομένων - Οφέλη](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Ανάπτυξη εφαρμογής επιπέδου δεδομένων - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Πώς να δημιουργήσω αρχείο DACPAC;](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

