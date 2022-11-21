{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","τι είναι ένα αρχείο xsd", "πώς να ανοίξετε αρχείο xsd", "επέκταση", "αρχείο", "αρχείο xsd", "μορφή αρχείου xsd", "επέκταση .xsd" ,"παράδειγμα αρχείου xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Μάθετε για τη μορφή αρχείου XSD και τα API που μπορούν να δημιουργήσουν και να ανοίξουν ένα αρχείο XSD.",
  "title" :"Μορφή αρχείου XSD - Αρχείο ορισμού σχήματος XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Τι είναι ένα αρχείο XSD Schema;

Ένα αρχείο XSD είναι ένα αρχείο ορισμού που καθορίζει τα στοιχεία και τα χαρακτηριστικά που μπορούν να αποτελούν μέρος ενός εγγράφου XML. Αυτό διασφαλίζει ότι τα δεδομένα ερμηνεύονται σωστά και εντοπίζονται σφάλματα, με αποτέλεσμα την κατάλληλη επικύρωση XML. Τα αρχεία XSD διασφαλίζουν ότι τα δεδομένα που εισάγονται ακολουθούν την ίδια δομή όπως ορίζεται στο αρχείο. Τα αρχεία XSD αποθηκεύονται σε μορφή αρχείου [XML](/el/web/xml/) και μπορούν να ανοίξουν ή να επεξεργαστούν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου όπως το Microsoft Notepad, το Notepad++ ή το [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Μορφή αρχείου XSD

Τα αρχεία XSD αποθηκεύονται σε δίσκο σε μορφή αρχείου απλού κειμένου που είναι αναγνώσιμη από τον άνθρωπο. Ένα XSD ορίζει τα στοιχεία που μπορούν να χρησιμοποιηθούν στα έγγραφα, σε σχέση με τα πραγματικά δεδομένα με τα οποία πρόκειται να κωδικοποιηθεί.

## Παράδειγμα αρχείου XSD

Ένα απλό αρχείο XSD με σχήμα παραγγελίας αγοράς ορίζει τα στοιχεία χρησιμοποιώντας ετικέτες όπως φαίνεται στο ακόλουθο [παράδειγμα XSD από τη Microsoft](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file -simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

Εδώ, χρησιμοποιούνται οι ακόλουθες ετικέτες.

* `xs:στοιχείο` - Καθορίζει ένα στοιχείο.
* `xs:sequence` - Δηλώνει τα θυγατρικά στοιχεία που εμφανίζονται μόνο με τη σειρά που αναφέρεται.
* `xs:complexType` - Υποδηλώνει ότι περιέχει άλλα στοιχεία.
* `xs:simpleType` - Δηλώνει ότι δεν περιέχουν άλλα στοιχεία.
* «τύπος» - συμβολοσειρά, δεκαδικός, ακέραιος, boolean, ημερομηνία, ώρα,

## Βιβλιογραφικές αναφορές ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Δείγμα XSD](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

