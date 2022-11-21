{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο HTX - Μορφή αρχείου επέκτασης HTML",
  "description" :"Ο οδηγός μορφής αρχείου σας για να μάθετε τι είναι ένα αρχείο HTX και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχείο HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο HTX;

Ένα αρχείο HTX είναι στην πραγματικότητα ένα αρχείο HTML που περιέχει μεταβλητές δεδομένων για την εμφάνιση των αποτελεσμάτων ερωτήματος της βάσης δεδομένων ως ιστοσελίδα. Τα αρχεία HTX που δημιουργούνται κυρίως με λογισμικό ανάπτυξης Web Microsoft FrontPage αποθηκεύονται για να αποθηκευτούν στον ίδιο φάκελο με το αντίστοιχο αρχείο Internet Database Connector (.IDC).

Τα αρχεία HTX μπορούν να ανοίξουν με εφαρμογές όπως το Microsoft FrontPage και οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Σημειωματάριο, το TextEdit ή το Atom.

## Μορφή αρχείου HTX

Τα αρχεία HTX αποθηκεύονται ως αρχείο απλού κειμένου με κώδικα για την ανάκτηση δεδομένων από μια βάση δεδομένων και την αποθήκευση σε μεταβλητές για εμφάνιση.


### Παράδειγμα αρχείου HTX

Ένα παράδειγμα αρχείου HTX είναι το ακόλουθο που ορίζει μια κεφαλίδα σελίδας για την εμφάνιση του περιορισμού ερωτήματος και τα έγγραφα που εμφανίζονται στη σελίδα για εμφάνιση στον χρήστη.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Η έξοδος αυτού του δείγματος κώδικα είναι η εξής.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Όπως φαίνεται, το αρχείο HTX είναι ένα πρότυπο που διαμορφώνει τον τρόπο με τον οποίο επιστρέφονται και εμφανίζονται τα αποτελέσματα στους τελικούς χρήστες. Είναι γραμμένο σε μορφή HTML με ορισμένες επεκτάσεις IIS και υπηρεσία ευρετηρίου. Αυτές οι επεκτάσεις περιλαμβάνουν ονόματα μεταβλητών και άλλους κωδικούς για την επεξεργασία των αποτελεσμάτων.

## βιβλιογραφικές αναφορές

* [Μορφοποίηση των αποτελεσμάτων σε αρχείο .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

