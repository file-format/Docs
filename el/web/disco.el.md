{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο DISCO - Μορφή αρχείου εγγράφου εντοπισμού",
  "description":"Μάθετε τι είναι ένα αρχείο DISCO και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Τι είναι ένα αρχείο DISCO;

Ένα αρχείο DISCO είναι μια μορφή αρχείου Microsoft Discovery που χρησιμοποιείται για τη δημοσίευση και την ανακάλυψη Υπηρεσιών Ιστού. Αποθηκεύεται σε μορφή αρχείου XML και επιτρέπει στα εργαλεία Web Services Discovery να εντοπίσουν ή να ανακαλύψουν ένα ή περισσότερα σχετικά έγγραφα για την περιγραφή των διαθέσιμων υπηρεσιών [XML](/el/web/xml/). Το αρχείο DISCO αποθηκεύει πληροφορίες όπως έγγραφα εντοπισμού, σχήματα [XSD](https://docs.fileformat.com/programming/xsd/) και περιγραφές υπηρεσιών. Οι υπηρεσίες Ιστού XML χρησιμοποιούν αυτές τις πληροφορίες για να μεταβούν στις διαθέσιμες υπηρεσίες ιστού XML σε μια δεδομένη διεύθυνση URL.

## Μορφή αρχείου DISCO - Περισσότερες πληροφορίες

Τα αρχεία DISCO αποθηκεύονται σε μορφή αρχείου XML. Το Microsoft Discovery Tool (DISCO.exe), το οποίο συνοδεύεται από λογισμικό ανάπτυξης Microsoft ASP.NET, όπως το Microsoft Studio, χρησιμοποιεί τα αρχεία DISCO για να ανακαλύψει τις λεπτομέρειες σχετικά με τις υπηρεσίες Web XML που παρατίθενται σε ένα DiscoveryDocument σε μια συγκεκριμένη διεύθυνση URL. Η Microsoft έχει παράσχει την υποστήριξη ανάγνωσης αρχείων εντοπισμού στο πλαίσιο .NET.

## βιβλιογραφικές αναφορές

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894?tab=Overview)
* [Ανακάλυψη Υπηρεσιών Ιστού](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Παράδειγμα C# της κλάσης DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

