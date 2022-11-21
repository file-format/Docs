{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο kml", "τι είναι αρχείο kml", "αρχείο", "παράδειγμα kml", "επέκταση αρχείου kml", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου KML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο KML;

KML, Keyhole Markup Language) περιέχει γεωχωρικές πληροφορίες σε σημειογραφία XML. Τα αρχεία που είναι αποθηκευμένα ως KML μπορούν να ανοίξουν σε εφαρμογές Συστήματος Γεωγραφικών Πληροφοριών (GIS) με την προϋπόθεση ότι το υποστηρίζουν. Πολλές εφαρμογές έχουν αρχίσει να παρέχουν υποστήριξη για τη μορφή αρχείου KML μετά την υιοθέτησή της ως διεθνές πρότυπο. Το KML χρησιμοποιεί μια δομή που βασίζεται σε ετικέτες με ένθετα στοιχεία και χαρακτηριστικά. Όλες οι ετικέτες κάνουν διάκριση πεζών-κεφαλαίων και είναι σημαντικό να ακολουθήσετε τη σειρά αυτών των ετικετών, σύμφωνα με την αναφορά [KML](https://developers.google.com/kml/documentation/kmlreference).

## Σύντομη Ιστορία ##

Το KML αναπτύχθηκε αρχικά για χρήση με το Google Earth το οποίο ήταν αρχικά γνωστό ως Keyhole Earth Viewer. Το KLM υιοθετήθηκε ως διεθνές πρότυπο το 2008 από την Open Geospatial Consortium το 2008. Δεδομένου ότι η μορφή αναπτύχθηκε για χρήση με το Google Earth, έχει τη διάκριση να είναι η πρώτη που βλέπει και επεξεργάζεται αρχεία KML. Με το πέρασμα του χρόνου, υπάρχουν πλέον όλο και περισσότερα έργα που παρέχουν υποστήριξη για μορφές αρχείων KML, συμπεριλαμβανομένων πολλών API σε διαφορετικές γλώσσες.

## Προδιαγραφές μορφής αρχείου KML ##

Η Αναφορά KML είναι ένας πλήρης οδηγός αναφοράς προκειμένου να έχετε τις πλήρεις προδιαγραφές μορφής αρχείου. Ένα τυπικό αρχείο KML αποτελείται από:

* Σήμανση μέρους
* Περιγραφικά HTMLin Placemarks
* Επικαλύψεις εδάφους
* Μονοπάτια
* Πολύγωνα

Εκτός από αυτά, μια προηγμένη έκδοση του αρχείου KML μπορεί να έχει:

* Στυλ για τη Γεωμετρία
* Στυλ για επισημασμένα εικονίδια
* Επικαλύψεις οθόνης
* Σύνδεσμοι δικτύου

Κάθε στοιχείο KML έχει lat-long πληροφορίες που εντοπίζουν γεωγραφικά τις πληροφορίες που υπάρχουν στο αρχείο. Ωστόσο, μπορεί να υπάρχουν πρόσθετες παράμετροι όπως η κατεύθυνση, το υψόμετρο και η κλίση.

### Σημάδια μέρους ###

Χρησιμοποιείται για να αναπαραστήσει μια θέση στην επιφάνεια της Γης και προσδιορίζεται από το<Point> στοιχείο. Ακολουθεί ένα παράδειγμα πώς αναπαρίσταται μια σήμανση μέρους σε αρχείο KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Περιγραφικό HTML στις σημάνσεις μέρους ###

Πρόσθετες πληροφορίες μπορούν να συσχετιστούν με μια σήμανση μέρους που βελτιώνει περαιτέρω την αναπαράσταση της σήμανσης μέρους. Τέτοιες πληροφορίες περιλαμβάνουν συνδέσμους, μεγέθη γραμματοσειρών, στυλ και χρώματα. Επιπλέον, περιλαμβάνει επίσης τη στοίχιση κειμένου και τους πίνακες που αποτελούν μέρος της σήμανσης μέρους.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Επικαλύψεις εδάφους ###

Αυτά αντιπροσωπεύουν τη στρωματοποίηση μιας εικόνας στην επιφάνεια της Γης. ο<icon> Το στοιχείο περιέχει το σύνδεσμο προς το αρχείο εικόνας επικάλυψης.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Μονοπάτια ###

Τα μονοπάτια αντιπροσωπεύονται από<LineString> στοιχείο που είναι μια συλλογή από lat-long ζεύγη. Χρησιμοποιώντας αυτά, μπορούν να δημιουργηθούν πολλοί διαφορετικοί τύποι μονοπατιών στο Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Χωρική αναφορά στο αρχείο KML ##

Οι πληροφορίες που περιέχονται σε οποιοδήποτε Γεωχωρικό αρχείο σχετικά με τις Γεω-Τοποθεσίες μπορούν να έχουν διαφορετικές σημασίες χωρίς πληροφορίες χωρικής αναφοράς. Από προεπιλογή, η χωρική αναφορά του αρχείου KML ορίζεται από το Παγκόσμιο Γεωδαιτικό Σύστημα του 1984, WGS84.

## Βιβλιογραφικές αναφορές ##

* [Αναφορά KML](https://developers.google.com/kml/documentation/kmlreference)
* [Οδηγός προγραμματιστή Google για KML](https://developers.google.com/kml/documentation/kml_tut)
* [Μορφή αρχείου KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

