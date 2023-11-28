{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange File Format",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου OFX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Τι είναι ένα αρχείο OFX;

Ένα αρχείο OFX (Open Financial Exchange) είναι μια μορφή χρηματοοικονομικού αρχείου που χρησιμοποιείται για την ανταλλαγή οικονομικών πληροφοριών μεταξύ προγραμμάτων λογισμικού και χρηματοπιστωτικών ιδρυμάτων. Με την εξέλιξη των λύσεων λογισμικού για την εσωτερική χρηματοοικονομική λογιστική τήρηση βιβλίων, έχουν αναπτυχθεί προγράμματα λογισμικού που μπορούν να συνδεθούν με την τράπεζά σας και να εισάγουν ή να εξάγουν οικονομικά δεδομένα με τις τράπεζες. Αυτό περιλαμβάνει οικονομικά δεδομένα όπως συναλλαγές, πληροφορίες λογαριασμού και πληρωμές λογαριασμών. Προγράμματα λογισμικού όπως τα QuickBooks, Microsoft Money, Intuit και Quicken αποθηκεύουν τα εισαγόμενα δεδομένα ως αρχείο OFX.

Ο τύπος μέσων Διαδικτύου για τη μορφή αρχείου OFX είναι application/x-ofx.

## Μορφή αρχείου OFX

Τα αρχεία OFX αποθηκεύονται σε μορφή αρχείου XML (Extensible Markup Language) και χρησιμοποιούν ετικέτες για τη δομή των δεδομένων. Τα αρχεία [XML](/el/web/xml/) αποθηκεύονται σε μορφή αναγνώσιμη από τον άνθρωπο και μπορούν να ανοίξουν και να επεξεργαστούν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Notepad, το Notepad++ ή το Apple TextEdit. Τα δεδομένα που αποθηκεύονται στα αρχεία OFX βασίζονται στο πρότυπο **SGML (Τυπική Γενικευμένη Γλώσσα Σήμανσης)**. Τα δεδομένα που αποθηκεύονται σε αρχεία OFX περιλαμβάνουν συνήθως:

* Πληροφορίες σχετικά με τράπεζες
* Πληροφορίες πιστωτικής και χρεωστικής κάρτας
* Πληροφορίες για λογαριασμούς και επενδύσεις
* τυχόν άλλες οικονομικές συναλλαγές

### Παράδειγμα μορφής αρχείου OFX

Ακολουθεί η εσωτερική δομή δεδομένων και δείγμα δεδομένων ενός παραδείγματος αρχείου OFX.

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

Αυτό το παράδειγμα αρχείου OFX περιέχει τις ακόλουθες πληροφορίες:

* Πληροφορίες τραπεζικού λογαριασμού, όπως όνομα τράπεζας, αριθμός λογαριασμού και υπόλοιπο
* Λίστα συναλλαγών, συμπεριλαμβανομένης της ημερομηνίας, του τύπου και του ποσού κάθε συναλλαγής

Όλες αυτές οι πληροφορίες μπορούν να εισαχθούν σε ένα πρόγραμμα λογισμικού προσωπικής χρηματοδότησης για να παρακολουθείτε τις συναλλαγές και τα έξοδα λογαριασμού.

## Βιβλιογραφικές αναφορές ##

* [Open Financial Exchange - By Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Πρότυπο ISO για Ηλεκτρονική Ανταλλαγή Δεδομένων](https://en.wikipedia.org/wiki/ISO_20022)

