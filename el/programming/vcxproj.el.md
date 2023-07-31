{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "αρχείο", "επέκταση", "μορφή αρχείου", "Visual C++ Project", "Οδηγός προγραμματισμού" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου VCXPROJ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Τι είναι ένα αρχείο VCXPROJ;

Ένα αρχείο με επέκταση .vcxproj είναι ένα αρχείο έργου της Microsoft Visual C++ που αποθηκεύει τις πληροφορίες έργου [C++](/el/programming/cpp/). Περιέχει πληροφορίες που χρησιμοποιούνται από το σύστημα έργου MSBuild για τη μεταγλώττιση και τη δημιουργία του τελικού αποτελέσματος. Το VCXPROJ των έργων Visual C++ είναι το ίδιο με αυτό του [CSPROJ](/el/programming/csproj/) για έργα .NET. Τα αρχεία VCXPROJ δεν περιέχουν κανέναν κώδικα, αλλά αναφέρονται σε όλες τις κλάσεις, τους στόχους και τις ιδιότητες που έχουν οριστεί για το έργο για τη δημιουργία του έργου. Αυτά μπορούν να ανοίξουν σε προγράμματα επεξεργασίας απλού κειμένου ή κατά προτίμηση στο Microsoft Visual Studio IDE.


## Μορφή αρχείου VCXPROJ - Περισσότερες πληροφορίες

Τα αρχεία VCXPROJ είναι αρχεία κειμένου που δημιουργούνται σε μορφή αρχείου [XML](/el/web/xml/). Αυτά μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου, αλλά συνιστάται ιδιαίτερα η χρήση του Microsoft Visual Studio IDE για το άνοιγμα και την επεξεργασία αυτών των αρχείων. Αυτά δεν σχεδιάστηκαν για χειροκίνητη επεξεργασία. Τα λάθη μπορεί να προκαλέσουν πτώση του IDE ή να συμπεριφέρεται με απροσδόκητους τρόπους.

Τα περιεχόμενα ενός δείγματος αρχείου VCXPROJ είναι τα ακόλουθα.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Στοιχεία αρχείου VCXPROJ

Ένα τυπικό αρχείο VCXPROJ περιέχει έναν αριθμό στοιχείων όπως φαίνεται στο παραπάνω παράδειγμα XML. Η [δομή VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) από τη Microsoft εξηγεί κάθε στοιχείο αρχείου λεπτομερώς και μπορεί να παραπεμφθεί από την πλευρά του προγραμματιστή.

#### Στοιχείο έργου

Αυτός είναι ο ριζικός κόμβος του αρχείου VCXPROJ. Το MSBuild χρησιμοποιεί αυτό το στοιχείο για να διαβάσει την έκδοση έκδοσης και τον προεπιλεγμένο στόχο για μεταγλώττιση.

#### ProjectConfigurations ItemGroup Element

Περιέχει τις πληροφορίες διαμόρφωσης του έργου που μπορεί να περιλαμβάνουν τη μέθοδο κατασκευής (Εντοπισμός σφαλμάτων ή έκδοση), συλλογή 32 ή 64-bit, επιλογές βελτιστοποίησης και άλλα. Οι πληροφορίες αυτής της ομάδας χρησιμοποιούνται από το IDE για τη φόρτωση του έργου.

#### Στοιχεία διαμόρφωσης έργου

Τα στοιχεία ProjectConfiguration σε ένα αρχείο VCXPROJ περιέχουν πληροφορίες σχετικά με την έκδοση και την πλατφόρμα για την οποία φορτώνεται το έργο. Το όνομά του θα πρέπει να έχει τη μορφή «$(Διαμόρφωση)|$(Πλατφόρμα)».

#### Globals PropertyGroup Element

Αυτή η ενότητα περιέχει ρυθμίσεις που παρέχουν πληροφορίες για το επίπεδο του έργου, όπως:

* ProjectGuid
* Χώρος ονομάτων ρίζας
* ApplicationType ή ApplicationTypeRevision


## βιβλιογραφικές αναφορές

* [Δομή VCXPROJ - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Αρχεία έργου C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

