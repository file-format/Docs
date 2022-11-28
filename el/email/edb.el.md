{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου EDB - Αρχείο βάσης δεδομένων αλληλογραφίας Exchange",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου EDB και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Τι είναι ένα αρχείο EDB;

Ένα αρχείο με επέκταση αρχείου .edb είναι μια βάση δεδομένων γραμματοκιβωτίου που δημιουργήθηκε από τον Microsoft Exchange Server για την αποθήκευση δεδομένων που σχετίζονται με την αλληλογραφία. Το EDB, Exchange Database, αποθηκεύει μηνύματα που είναι υπό επεξεργασία και μη SMTP. Τα EDB είναι επίσης γνωστά ως αρχεία βάσης δεδομένων Extensible Storage Engine (ESE) και αποθηκεύουν αρχεία χρησιμοποιώντας δομή b-tree. Ως αρχεία αποθήκευσης, τα αρχεία EDB μπορούν να μετατραπούν σε άλλες μορφές αρχείων αποθήκευσης αλληλογραφίας, όπως [PST](/el/email/pst/) και [OST](/el/email/ost/).

## Μορφή αρχείου EDB

Δεν υπάρχουν διαθέσιμες επίσημες/ανοιχτές προδιαγραφές μορφής αρχείου EDB που να μπορούν να αναφέρονται. Έχει σημειωθεί κάποια πρόοδος για την αντίστροφη μηχανική της μορφής αρχείου, με αποτέλεσμα την αποκωδικοποίηση μερικών προδιαγραφών. Σύμφωνα με αυτά, ένα αρχείο EDB αποτελείται από:
* File Header - Περιέχει πληροφορίες κεφαλίδας αρχείου βάσης δεδομένων
* Σελίδες σταθερού μεγέθους - Περιέχει τη βάση δεδομένων που αποτελείται από πίνακες και ευρετήρια

### Κεφαλίδα αρχείου βάσης δεδομένων
Η κεφαλίδα του αρχείου βάσης δεδομένων βρίσκεται στην πρώτη σελίδα βάσης δεδομένων και είναι τουλάχιστον 668 byte. Η κεφαλίδα αρχείου περιέχει «Έκδοση Μορφής αρχείου» και «Τύπος αρχείου» εκτός από άλλα πεδία.

#### Τύποι αρχείων
|Τύπος|Περιγραφή
---|---|
|0| Βάση δεδομένων|
|1| Ροή|

`Σημείωση:` Τα αναγνωριστικά για αυτούς τους τύπους δεν είναι γνωστά.

#### Έκδοση μορφής αρχείου
Η αρχική μορφή του EDB ξεκίνησε τον Απρίλιο του 1997 και συνέχισε να εξελίσσεται για αλλαγές στη συνέχεια.

|Ημερομηνία έκδοσης|Έκδοση|Αναθεώρηση|περιγραφή
---|---|---|---|
|Απρ. 1997| 0x00000620|0x00000000| Αρχικό λειτουργικό σύστημα μορφή Beta.|
|Μάιος 1997 |0x00000620|0x00000001| Προσθέστε στήλες στον κατάλογο για ευρετηρίαση υπό όρους και OLD.|
|Ιούνιος 1997|0x00000620|0x00000002|Προσθέστε τη σημαία fLocalizedText στο IDB.|
|Οκτώβριος 1997|0x00000620|0x00000003|Προσθήκη SPLIT_BUFFER σε σελίδες ρίζας δέντρου διαστήματος.|
|Ιαν 1998|0x00000620|0x00000002|Επαναφορά της αναθεώρησης προκειμένου το ESE97 να παραμείνει συμβατό προς τα εμπρός.|
||0x00000620|0x00000003|Προσθήκη νέων στηλών με ετικέτα στον κατάλογο ("CallbackData" και "CallbackDependencies").|
|Μάιος 1998|0x00000620|0x00000004|Υποστήριξη Super Long Value (SLV): signSLV, fSLVE υπάρχει στο dbheader.|
|Μάιος 1998|0x00000620|0x00000005|Νέο διαστημικό δέντρο SLV.|
|Οκτώβριος 1998|0x00000620|0x00000006|Χάρτης χώρου SLV.|
|Δεκ 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Ιαν 1999|0x00000620|0x00000008|Μορφή στήλης νέας προτύπου.|
|Ιούνιος 1999|0x00000620|0x00000009|Ταξινομημένες στήλες προτύπων. Χρησιμοποιείται σε Windows XP SP3|
||0x00000620|0x0000000b|Περιέχει την κεφαλίδα της σελίδας με το άθροισμα ελέγχου ECCUsed in Exchange|
||0x00000620|0x0000000c|Χρησιμοποιείται σε Windows Vista (SP0)|
||0x00000620|0x00000011|Υποστήριξη για σελίδες 2 KiB, 16 KiB και 32 KiB. Εκτεταμένη κεφαλίδα σελίδας με πρόσθετα αθροίσματα ελέγχου ECC. Συμπίεση στηλών. Συμβουλές διαστήματος. Χρησιμοποιείται στα Windows 7 (SP0)|
|Μάιος 1999|0x00000623|0x00000000|New Space Manager.|

### Αρχεία βάσης δεδομένων

Το αρχείο βάσης δεδομένων EDB περιέχει το σχήμα για όλους τους πίνακες της βάσης δεδομένων. Επιπλέον, περιλαμβάνει επίσης εγγραφές για όλους τους πίνακες βάσεων δεδομένων και ευρετήρια για τους πίνακες. Η θέση του καθορίζεται από τα ακόλουθα αναγνωριστικά.

* JetCreateDatabase
* JetCreateDatabase2
* Βάση δεδομένων JetAttach
* JetAttachDatabase2

Με βάση αυτά, η κατάσταση της βάσης δεδομένων μπορεί να εκτιμηθεί ως εξής.

|Τιμή|Αναγνωριστικό|Περιγραφή
---|---|---|
|1|JET_dbstateJustCreated|Η βάση δεδομένων μόλις δημιουργήθηκε.|
|2|JET_dbstateDirtyShutdown|Η βάση δεδομένων απαιτεί σκληρή ή μαλακή ανάκτηση για να γίνει χρησιμοποιήσιμη ή κινητή. Δεν πρέπει να προσπαθήσουμε να μετακινήσουμε βάσεις δεδομένων σε αυτήν την κατάσταση.|
|3|JET_dbstateCleanShutdown|Η βάση δεδομένων είναι σε καθαρή κατάσταση. Η βάση δεδομένων μπορεί να επισυναφθεί χωρίς κανένα αρχείο καταγραφής.|
|4|JET_dbstateBeingConverted|Η βάση δεδομένων αναβαθμίζεται.|
|5|JET_dbstateForceDetachInternal|Αυτή η τιμή εισάγεται στα WindowsXP|
 

## βιβλιογραφικές αναφορές
* [Προδιαγραφές αρχείου βάσης δεδομένων (EDB) Extensible Storage Engine (ESE)](https://github.com/libyal/libesedb/tree/master/documentation)
