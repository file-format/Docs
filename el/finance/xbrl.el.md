{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "αρχείο xbrl", "μορφή αρχείου xbrl", "τύπος αρχείου xbrl", "αρχείο", "τύπος", "τι είναι ένα αρχείο xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Μορφή αρχείου επιχειρηματικής και χρηματοοικονομικής αναφοράς",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XBRL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Τι είναι ένα αρχείο XBRL;

Ένα αρχείο με επέκταση .xbrl (eXtensible Business Reporting Language) είναι ένα ελεύθερα διαθέσιμο και παγκόσμιο πλαίσιο για την ανταλλαγή επιχειρηματικών πληροφοριών. Χρησιμοποιείται πλέον ευρέως ως μία από τις τυποποιημένες μορφές που έχει αντικαταστήσει τις παλαιότερες αναφορές που βασίζονται σε χαρτί με πιο χρήσιμες και ακριβείς ψηφιακές εγγραφές. Τα δεδομένα που ανταλλάσσονται χρησιμοποιώντας τα αρχεία XBRL περιλαμβάνουν λογιστικά βιβλία, οικονομικές λεπτομέρειες και ισολογισμούς. Υποστηρίζει ετικέτες δεδομένων που επιτρέπουν την επεξεργασία δεδομένων από την προετοιμασία μέχρι το στάδιο της ανάλυσης όλων των ειδών επιχειρηματικών πληροφοριών. Τα αρχεία XBRL μπορούν να ανοίξουν χρησιμοποιώντας λογισμικό όπως το Rivet Software Dragon View XBRL Viewer και API όπως το [Aspose.Finance](https://products.aspose.com/finance/).

## Μορφή αρχείου XBRL

Το XBRL είναι ένα ανοιχτό διεθνές πρότυπο για την ψηφιακή επιχειρηματική αναφορά που χρησιμοποιείται ευρέως παγκοσμίως. Είναι μια γλώσσα που βασίζεται σε [XML](/el/web/xml/) που χρησιμοποιεί στοιχεία XBRL, γνωστά ως ετικέτες, για να περιγράψει κάθε στοιχείο επιχειρηματικών δεδομένων για τη διαμόρφωση δεδομένων για ταξινόμηση και ανάλυση αναφορών. Οι προδιαγραφές μορφής αρχείου XBRL αναπτύσσονται και δημοσιεύονται από την XBRL International, Inc, με [XBRL έκδοση 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) επί του παρόντος διαθέσιμο στους χρήστες.

### Δομή εγγράφου XBRL

Πλήρεις πληροφορίες σχετικά με τις [ετικέτες XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) μπορεί να παραπεμφθεί από προγραμματιστές για τη σύνταξη εφαρμογών για την επεξεργασία αυτής της μορφής αρχείου. Ένα XBRL αποτελείται από μια παρουσία XBRL και μια συλλογή ταξινομιών.

**`Παράδειγμα XBRL`** - Η παρουσία XBRL ξεκινά με το<xbrl> ριζικό στοιχείο. Ένα μεγάλο έγγραφο XML μπορεί να περιέχει περισσότερες από μία παρουσίες XBRL ενσωματωμένες σε αυτό.

**`XBRL Taxonomy`** - Η [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 Το +corrected-errata-2013-02-20.html#_5) ορίζεται ως δομές σχήματος XML και σύνολο στοιχείων εξωτερικών συνδέσμων που αναφέρονται απευθείας. Ένα κλιμακούμενο σχήμα ταξινόμησης που δείχνει τις αναφορές της βάσης συνδέσεων είναι το ακόλουθο.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Βιβλιογραφικές αναφορές ##

* [XBRL - Από τη Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

