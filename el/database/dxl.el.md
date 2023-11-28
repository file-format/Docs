{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου DXL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DTSX.",
  "title" :"Μορφή αρχείου DXL - Μορφή αρχείου γλώσσας Domino XML",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Τι είναι ένα αρχείο DXL;

Ένα αρχείο DXL είναι ένα αρχείο αποθήκευσης δεδομένων βασισμένο σε XML που δημιουργήθηκε για το λογισμικό επιχειρηματικής συνεργασίας σε επίπεδο επιχείρησης, Lotus Domino. Περιέχει δεδομένα που σχετίζονται με μια βάση δεδομένων Lotus Domino, όπως σχήματα, στοιχεία σχεδίασης, προβολή, φόρμες, έγγραφα και τα ίδια τα δεδομένα της βάσης δεδομένων. Το [XML](/el/web/xml/) είναι μια καθολική μορφή αρχείου που μπορεί να διαβαστεί από εφαρμογές λογισμικού γραμμένες σε οποιαδήποτε γλώσσα προγραμματισμού. Είναι επίσης αναγνώσιμο από τον άνθρωπο και μπορεί να ανοίξει με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Αυτός είναι ο λόγος για τον οποίο τα αρχεία DXL παρέχουν τη δυνατότητα εξαγωγής δεδομένων σε εναλλάξιμη μορφή αρχείου.

## Μορφή αρχείου DXL

Τα αρχεία DXL αποθηκεύονται σε μορφή αρχείου XML και είναι εύκολα αναγνώσιμα από εφαρμογές γραμμένες σε οποιαδήποτε γλώσσα προγραμματισμού. Αυτά τα αρχεία αποθηκεύουν δεδομένα και ρυθμίσεις σε ετικέτες XML που κατηγοριοποιούν τα δεδομένα καθώς και τα ταξινομούν με τη σωστή σειρά

### Παράδειγμα εξόδου DXL

Ακολουθεί η έξοδος αποσπάσματος κειμένου για ένα έγγραφο Notes.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## βιβλιογραφικές αναφορές

* [Μορφή DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

