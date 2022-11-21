{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd file", "usd file format", "file format", "file", "extension", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Universal Scene Description Format",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου USD και τα API που μπορούν να ανοίξουν και να δημιουργήσουν αρχεία USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Τι είναι ένα αρχείο USD;

Ένα αρχείο με επέκταση .usd είναι μια μορφή αρχείου Universal Scene Description που κωδικοποιεί δεδομένα με σκοπό την ανταλλαγή και την αύξηση δεδομένων μεταξύ εφαρμογών δημιουργίας ψηφιακού περιεχομένου. Αναπτύχθηκε από την Pixar, το [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) παρέχει τη δυνατότητα ανταλλαγής στοιχειωδών στοιχείων (όπως μοντέλα) ή κινούμενων εικόνων.

## Μορφή αρχείου USD

Τα αρχεία USD μπορεί να έχουν δυαδική μορφή (γνωστά και ως αρχεία Crate) ή αρχεία με υποστήριξη ASCII. Και οι δύο αυτές μορφές αρχείων είναι εναλλάξιμες όπου οι αναφορές μπορούν να συνδεθούν με στοιχεία .usd χωρίς αλλαγή των πηγών. Η μορφή αρχείου USD αποτελείται από ένα σύνολο βιβλιοθηκών C++ με δεσμεύσεις Python για δέσμες ενεργειών. Επιτρέπει τη συναρμολόγηση και την οργάνωση οποιουδήποτε αριθμού στοιχείων τρισδιάστατης σκηνής, όπως εικονικά σκηνικά, σκηνές και λήψεις για τη μετάδοσή τους από εφαρμογή σε εφαρμογή.

### Τύποι δεδομένων USD

Οι βασικοί τύποι δεδομένων που υποστηρίζονται από τη μορφή αρχείου USD παρατίθενται στον παρακάτω πίνακα.

|Διακριτικό τύπου τιμής |Τύπος C++ |Περιγραφή|
---|---|---|
|μπουλ|μπουλ||
|uchar|uint8_t|8 bit ανυπόγραφος ακέραιος|
|int|int32_t|32 bit ακέραιος αριθμός|
|uint|uint32_t|32 bit ανυπόγραφος ακέραιος|
|int64|int64_t|64 bit ακέραιος αριθμός|
|uint64|uint64_t|64 bit ανυπόγραφος ακέραιος|
|μισό|GfHalf|16 bit κινητής υποδιαστολής|
|float|float|32 bit κινητής υποδιαστολής|
|διπλό|διπλό|64 bit κινητής υποδιαστολής|
|timecode|SdfTimeCode|διπλό που αντιπροσωπεύει έναν επιλύσιμο χρόνο|
|string|std::string|stl string|
|token|TfToken|ενσωματωμένη συμβολοσειρά με γρήγορη σύγκριση και κατακερματισμό|
|asset|SdfAssetPath|αντιπροσωπεύει μια επιλύσιμη διαδρομή προς ένα άλλο στοιχείο|
|matrix2d|GfMatrix2d|2x2 matrix των διπλών|
|matrix3d|GfMatrix3d|3x3 μήτρα διπλών|
|matrix4d|GfMatrix4d|4x4 μήτρα διπλών|
|quatd|GfQuatd|τεταρτοταγές διπλής ακρίβειας|
|quatf|GfQuatf|τεταρτοταγή απλής ακρίβειας|
|quath|GfQuath|τεταρτοταγή μισής ακρίβειας|
|double2|GfVec2d|διάνυσμα 2 διπλών|
|float2|GfVec2f|διάνυσμα 2 float|
|half2|GfVec2h|διάνυσμα 2 μισών|
|int2|GfVec2i|διάνυσμα 2 ιντσών|
|double3|GfVec3d|διάνυσμα 3 διπλών|
|float3|GfVec3f|διάνυσμα 3 float|
|half3|GfVec3h|διάνυσμα 3 μισών|
|int3|GfVec3i|διάνυσμα 3 ιντσών|
|double4|GfVec4d|διάνυσμα 4 διπλών|
|float4|GfVec4f|διάνυσμα 4 float|
|half4|GfVec4h|διάνυσμα 4 μισών|
|int4|GfVec4i|διάνυσμα 4 ιντσών|

## Παράδειγμα USD

Ένα παράδειγμα αρχείου USD σε απλή μορφή αρχείου ASCII είναι το ακόλουθο.

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## Βιβλιογραφικές αναφορές ##

* [Εισαγωγή στο USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Αναφορά API USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

