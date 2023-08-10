{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο dae", "μορφή αρχείου dae", "τι είναι αρχείο dae", "αρχείο", "παράδειγμα dae", "επέκταση αρχείου dae", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου DAE και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία DAE.",
  "title" :"DAE - Μορφή αρχείου ανταλλαγής ψηφιακών στοιχείων",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο DAE;

Ένα αρχείο DAE είναι μια μορφή αρχείου Digital Asset Exchange που χρησιμοποιείται για την ανταλλαγή δεδομένων μεταξύ διαδραστικών τρισδιάστατων εφαρμογών. Αυτή η μορφή αρχείου βασίζεται στο σχήμα XML COLLADA (COLLAborative Design Activity), το οποίο είναι ένα ανοιχτό πρότυπο σχήμα XML για την ανταλλαγή ψηφιακών στοιχείων μεταξύ εφαρμογών λογισμικού γραφικών. Έχει υιοθετηθεί από το ISO ως δημόσια διαθέσιμη προδιαγραφή, ISO/pAS 17506. Τα αρχεία DAE μπορούν να ανοίξουν σε εφαρμογές όπως το Adobe Photoshop, το AutoDesk Maya, το AutoDesk AutoCAD και API όπως το [Aspose.CAD](https://products.aspose.com/cad/).

## Μορφή αρχείου DAE

Η μορφή αρχείου DAE βασίζεται στο [σχήμα COLLADA XML](https://www.khronos.org/files/collada_spec_1_5.pdf) όπου όλα τα στοιχεία ορίζονται ως ετικέτες XML. Επιτρέπει τη σύνδεση διαφορετικών εργαλείων επεξεργασίας DCC και 3D σε έναν αγωγό παραγωγής για τρισδιάστατα στοιχεία. Διαθέτει ολοκληρωμένη κωδικοποίηση οπτικών σκηνών, όπως γεωμετρία, κινούμενα σχέδια, σκίαστρες και φυσική. Η μορφή είναι ανοιχτή, βαθμού αρχειοθέτησης και διατηρεί μετα-πληροφορίες.

### Ετικέτες COLLADA

Η ετικέτα σχήματος COLLADA είναι όπως φαίνεται παρακάτω.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Ετικέτα περιουσιακού στοιχείου

Η ετικέτα περιουσιακού στοιχείου περιγράφει τον συγγραφέα και το περιβάλλον του αρχείου

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Βιβλιοθήκη κάμερας

Τα στοιχεία COLLADA περιέχονται σε βιβλιοθήκες. Η βιβλιοθήκη φωτογραφικών μηχανών περιέχει αναπάντεχα κάμερες. Οι συνηθισμένες κάμερες είναι προοπτικές ή ορθογραφικές. Η ετικέτα βιβλιοθήκης κάμερας ορίζεται ως εξής.
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### Φώτα

Τα κοινά φώτα είναι σημειακά, σημειακά ή κατευθυντικά
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### Περίπτωση Υλικών

Τα εφέ της παρουσίας Υλικών ορίζονται ως εξής.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Κοινά εφέ

Τα κοινά εφέ λειτουργούν όπως η κατάσταση OpenGL 1 και μπορούν να οριστούν ως εξής.

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### Γεωμετρία Ιδιότητες

Η γεωμετρία περιγράφει τα χαρακτηριστικά OpenGL και ορίζεται ως εξής.
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### Οπτικές σκηνές

Οι οπτικές σκηνές είναι σαν σκηνές ενότητας και περιέχουν μια ιεραρχία κόμβων ως εξής.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## βιβλιογραφικές αναφορές
* [Προδιαγραφές COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

