{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο mpkg", "μορφή αρχείου mpkg", "τι είναι αρχείο mpkg", "αρχείο", "παράδειγμα mpkg", "επέκταση αρχείου mpkg", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου MPKG - Αρχείο Meta Package",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MPKG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Τι είναι ένα αρχείο MPKG;

Ένα αρχείο με επέκταση .mpkg είναι ένα αρχείο εγκατάστασης αρχειοθέτησης, που βρίσκεται κυρίως σε λειτουργικά συστήματα MacOS. Περιέχει όλα τα απαιτούμενα αρχεία εγκατάστασης της εφαρμογής χωρίς την ανάγκη διατήρησης των συσχετισμένων αρχείων χωριστά. Ένα μεμονωμένο αρχείο MPKG μπορεί να περιέχει αρχεία πακέτου [PKG](/el/compression/pkg/) ως ένα από τα αρχεία εγκατάστασης εκτός από άλλα αρχεία. Τα αρχεία MPKG δεν μπορούν να ανοίξουν με κανένα γενικό λογισμικό και εκτελούνται αυτόματα σε MacOS χρησιμοποιώντας το Apple Installer.

## Μορφή αρχείου MPKG

Ένα αρχείο MPKG περιέχει διαφορετικούς τύπους αρχείων που απαιτούνται για την εγκατάσταση πολλαπλών πακέτων που περιέχει. Αυτό φαίνεται από την παρακάτω εικόνα, η οποία είναι η δομή δέντρου ενός δείγματος αρχείου MPKG. Αυτή η δομή δέντρου εξάγεται χρησιμοποιώντας την εντολή «δέντρο» στο τερματικό MacOS.

{{< figure src="../mpkg.png" alt="Μορφή αρχείου MPKG" >}}

Η περιγραφή των διαφορετικών στοιχείων στην εικόνα έχει ως εξής.

«Κατάλογος πακέτων» - αποθηκεύει μια λίστα αρχείων pkg, δηλαδή μια λίστα με υποπακέτα
"Κατάλογος πόρων" - αποθηκεύει πόρους που χρησιμοποιούνται από το pkg, όπως τοπικούς πόρους και εικόνες , έγγραφα Rtf, έγγραφα pdf κ.λπ.
`Αρχείο Distribution.dist` - Ένα έγγραφο xml που περιέχει πληροφορίες όπως υποπακέτα που πρόκειται να εγκατασταθούν και σενάρια χρόνου εκτέλεσης

Το δείγμα αρχείου XML για ένα αρχείο MPKG μπορεί να έχει την εξής μορφή, ανάλογα με τα συσχετισμένα υποπακέτα.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/el/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
«app.pkg» - είναι το υποπακέτο που θα εγκατασταθεί. Είναι ένας κατάλογος της δομής Bundle σε μορφή pkg. Περιέχει έναν υποκατάλογο Περιεχομένων.

## βιβλιογραφικές αναφορές

* [Πακέτα OSX Flat](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

