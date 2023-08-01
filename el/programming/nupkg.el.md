{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο NUPKG - Αρχείο πακέτου NuGet",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου NUPKG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Τι είναι ένα αρχείο NUPKG;

Ένα αρχείο NUPKG είναι ένα αρχείο πακέτου που περιέχει τον πηγαίο κώδικα που θα χρησιμοποιηθεί από το λογισμικό NuGet για τη δημιουργία πακέτων που θα χρησιμοποιηθούν σε έργα .NET. Το στοιχείο NuGet Package Manager είναι εγκατεστημένο ως μέρος του Microsoft Visual Studio για τη λήψη πακέτων από το διαδικτυακό αποθετήριο φιλοξενίας πακέτων. Τα αρχεία NUPKG βοηθούν τους προγραμματιστές να ανακτήσουν τα πιο πρόσφατα πακέτα από το [Nuget.org](https://nuget.org) χρησιμοποιώντας το NuGet Package Manager αντί για μη αυτόματη λήψη και εγκατάσταση των πακέτων ανάπτυξης. Τα αρχεία NUPKG δημιουργούνται από αρχεία NUSPEC και, όταν λαμβάνονται, εγκαθιστούν το πακέτο στο σύστημα χρήστη.

## Μορφή αρχείου NUPKG

Τα αρχεία NUPKG είναι αρχεία [ZIP](/el/compression/zip/) που περιέχουν τις συσκευασμένες βιβλιοθήκες μέσα σε αυτό. Όταν γίνει λήψη, μπορεί να μετονομαστεί σε .zip και να εξαχθεί με οποιαδήποτε τυπικά βοηθητικά προγράμματα zip όπως WinZIP, 7-Zip και Apple Archive Utility.

## Αναφορά

* [Nuget.org](https://nuget.org)
* [Γρήγορη εκκίνηση: Εγκαταστήστε και χρησιμοποιήστε ένα πακέτο στο Visual Studio (μόνο για Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [How to Create and Publish a Nuget Package](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

