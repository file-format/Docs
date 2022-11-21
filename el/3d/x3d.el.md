{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο x3d", "μορφή αρχείου x3d", "τι είναι ένα αρχείο x3d", "αρχείο", "παράδειγμα x3d", "επέκταση αρχείου x3d", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Αρχείο εικόνας 3D",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου X3D και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο X3D;
Το X3D είναι μια μορφή αρχείου τρισδιάστατων γραφικών που βασίζεται σε [XML](/el/web/xml/) για παρουσίαση τρισδιάστατων πληροφοριών. Είναι ένα αρθρωτό πρότυπο και ορίζεται μέσω πολλών προδιαγραφών ISO. Η μορφή υποστηρίζει διανυσματικά και ράστερ γραφικά, διαφάνεια, εφέ φωτισμού και ρυθμίσεις κινούμενων εικόνων, συμπεριλαμβανομένων περιστροφών, ξεθωριασμών και ταλαντώσεων. Έγινε διάδοχος της μορφής αρχείου [VRML](/el/3d/vrml/) το 2001. Το X3D έχει το πλεονέκτημα της κωδικοποίησης πληροφοριών χρώματος (σε αντίθεση με το [STL](/el/cad/stl/)) που χρησιμοποιείται κατά την εκτύπωση του μοντέλου σε ένα χρώμα τρισδιάστατος εκτυπωτής. Η μορφή διαθέτει επεκτάσεις στο VRML, παρέχοντας τη δυνατότητα κωδικοποίησης της σκηνής χρησιμοποιώντας μια σύνταξη XML καθώς και τη σύνταξη τύπου Open Inventor του VRML97 ή δυαδική μορφοποίηση.

Η αφηρημένη προδιαγραφή για το X3D (ISO/IEC 19775) εγκρίθηκε για πρώτη φορά από τον ISO το 2004. Οι κωδικοποιήσεις XML και ClassicVRML για το X3D (ISO/IEC 19776) εγκρίθηκαν για πρώτη φορά το 2005.

## Μορφή αρχείου X3D

Τα αρχεία σκηνής X3D έχουν μια κοινή δομή αρχείων:

* Κεφαλίδα αρχείου (είτε XML, ClassicVRML ή Συμπιεσμένο Δυαδικό)
* Έναρξη του ριζικού κόμβου X3D, συμπεριλαμβανομένων των χαρακτηριστικών έκδοσης και προφίλ
* Μια ενότητα κεφαλής με δηλώσεις Component και Meta (και οι δύο προαιρετικές)
* Το γράφημα σκηνής X3D και οι θυγατρικοί κόμβοι του
* Τέλος του ριζικού κόμβου X3D

## Παράδειγμα μορφής αρχείου X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## Βιβλιογραφικές αναφορές ##

* [X3D - Από τη Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Επίσημος ιστότοπος της Κοινοπραξίας Web3D](http://www.web3d.org/)
* [Επίσημος ιστότοπος X3D](http://www.web3d.org/x3d/what-x3d)

