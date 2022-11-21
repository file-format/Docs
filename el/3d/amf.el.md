{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "αρχείο amf", "μορφή αρχείου amf", "μορφή αρχείου", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου AMF και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία AMF.",
  "title" :"AMF - Additive Manufacturing File",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο AMF;
Ένα αρχείο AMF αποτελείται από οδηγίες για την περιγραφή αντικειμένων προκειμένου να χρησιμοποιηθεί από διαδικασίες πρόσθετης κατασκευής. Περιέχει ένα άνοιγμα<amf> ετικέτα XML και τελειώνει με a</amf> στοιχείο. Προηγείται μια γραμμή δήλωσης XML που καθορίζει την έκδοση XML και την κωδικοποίηση του αρχείου. Οι δηλώσεις μπορούν να περιλαμβάνουν πληροφορίες για τις μονάδες μέτρησης και, ελλείψει τέτοιων πληροφοριών, τα χιλιοστά χρησιμοποιούνται ως προεπιλεγμένη μονάδα.


## Μορφή αρχείου AMF

Η μορφή αρχείου Additive Manufacturing (**AMF**) ορίζει ανοιχτά πρότυπα για την περιγραφή αντικειμένων, προκειμένου να χρησιμοποιηθούν από πρόσθετες διαδικασίες κατασκευής, όπως η 3D εκτύπωση. Τα προγράμματα CAD χρησιμοποιούν τη μορφή αρχείου AMF χρησιμοποιώντας πληροφορίες όπως η γεωμετρία, το χρώμα και το υλικό των αντικειμένων. Η AMF διαφέρει από τη μορφή STL καθώς η πλευρική δεν υποστηρίζει χρώμα, υλικά, πλέγματα και αστερισμούς.

### Στοιχεία ενός αρχείου AMF

Τα πέντε στοιχεία ανώτατου επιπέδου που ορίζονται με το<AMF> οι ετικέτες είναι όπως περιγράφονται παρακάτω. Η παρουσία ενός στοιχείου αντικειμένου είναι απαραίτητη για ένα πλήρως λειτουργικό αρχείο AMF.

`<object> ` - Το στοιχείο αντικειμένου ορίζει έναν όγκο ή όγκους υλικού, καθένας από τους οποίους σχετίζεται με ένα αναγνωριστικό υλικού για εκτύπωση. Τουλάχιστον ένα στοιχείο αντικειμένου πρέπει να υπάρχει στο αρχείο. Πρόσθετα αντικείμενα είναι προαιρετικά.

`<material> ` - Το προαιρετικό στοιχείο υλικού ορίζει ένα ή περισσότερα υλικά για εκτύπωση με σχετικό αναγνωριστικό υλικού. Εάν δεν περιλαμβάνεται κανένα υλικό στοιχείο, θεωρείται ένα μοναδικό προεπιλεγμένο υλικό.

`<texture> ` - Το προαιρετικό στοιχείο υφής ορίζει μία ή περισσότερες εικόνες ή υφές για αντιστοίχιση χρώματος ή υφής, καθεμία με ένα σχετικό αναγνωριστικό υφής.

`<constellation> ` - Το προαιρετικό στοιχείο αστερισμού συνδυάζει ιεραρχικά αντικείμενα και άλλους αστερισμούς σε ένα σχετικό μοτίβο για εκτύπωση.

`<metadata> ` - Το προαιρετικό στοιχείο μεταδεδομένων καθορίζει πρόσθετες πληροφορίες σχετικά με τα αντικείμενα και τα στοιχεία που περιέχονται στο αρχείο.

## Παράδειγμα AMF

Ακολουθεί ένα παράδειγμα αρχείου AMF που μπορεί να αντιγραφεί σε ένα αρχείο [text](/el/word-processing/txt/) και να αποθηκευτεί ως συμπιεσμένο αρχείο [zip](/el/compression/zip/) για άνοιγμα.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## βιβλιογραφικές αναφορές

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Προδιαγραφές AMF σε ISO](https://www.iso.org/standard/67472.html)

