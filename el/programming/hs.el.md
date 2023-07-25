{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Μορφή αρχείου σεναρίου Haskell",
  "description":"Μάθετε τι είναι μια μορφή αρχείου HS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Μορφή αρχείου HelpSet Java

## Τι είναι ένα αρχείο Java HS;

Ένα αρχείο με επέκταση .hs στη γλώσσα προγραμματισμού Java είναι ένα αρχείο τεκμηρίωσης βοήθειας που χρησιμοποιείται από το σύστημα JavaHelp όταν ενεργοποιείται από μια εφαρμογή. Ορίζει το σύνολο βοήθειας για τη συγκεκριμένη εφαρμογή που έχει εγκατασταθεί και αποτελείται από πολλαπλά υποσύνολα ως μέρος της βοήθειας συστήματος για την εφαρμογή. Το πρόγραμμα Java πρέπει να μπορεί να βρει το αρχείο συνόλου βοήθειας του οποίου το όνομα τελειώνει με την επέκταση .hs.

## Πληροφορίες συνόλου βοήθειας Java

Ένα αρχείο .hs μπορεί να περιέχει τις ακόλουθες πληροφορίες.

|Πληροφορίες|Περιγραφή|
---|---|
|Αρχείο χάρτη|Το αρχείο χάρτη χρησιμοποιείται για τη συσχέτιση των αναγνωριστικών θεμάτων με τον ενιαίο εντοπιστή πόρων ή το όνομα διαδρομής των θεματικών αρχείων γλώσσας σήμανσης υπερκειμένου.|
|Προβολή πληροφοριών|Πληροφορίες που περιγράφουν τους πλοηγούς που χρησιμοποιούνται στο σύνολο βοήθειας. οι ποιοτικοί πλοηγοί είναι: πίνακας περιεχομένων, ευρετήριο και αναζήτηση πλήρους κειμένου. Οι περαιτέρω πλοηγοί περιλαμβάνουν το gloss και επίσης τους αγαπημένους πλοηγούς. δεδομένα σχετικά με προσαρμοσμένους πλοηγούς εσωκλείονται εδώ περαιτέρω.|
<html>|Τίτλος σετ βοήθειας|Το \<title> περιγράφεται στο αρχείο Helpset (.hs). Αυτός ο τίτλος φαίνεται στο υψηλότερο από τα περισσότερα παράθυρα και τυχόν δευτερεύοντα παράθυρα που περιγράφονται στο αρχείο συνόλου βοήθειας.| </html>
|Αναγνωριστικό αρχικής σελίδας|Ο τίτλος του (προεπιλεγμένου) αναγνωριστικού που εμφανίζεται όταν καλείται ο βοηθός παρακολούθησης χωρίς να υποδεικνύεται αναγνωριστικό.|
|Παρουσίαση|Τα παράθυρα στα οποία εμφανίζονται τα θέματα βοήθειας. Αυτό μπορεί να είναι ένα σύγχρονο πρόγραμμα υπολογιστή JavaHelp 2 που απεικονίζεται με περισσότερες λεπτομέρειες κάτω από \<presentation> .|
|Υπο-βοήθεια|Αυτή η διακριτική περιοχή ενσωματώνει στατικά άλλα βοηθητικά σύνολα χρησιμοποιώντας την ετικέτα. Τα σύνολα βοήθειας που εμφανίζονται από αυτήν την ετικέτα συνδυάζονται φυσικά στο σύνολο βοήθειας που περιέχει την ετικέτα. Περισσότερα σημεία ενδιαφέροντος σχετικά με την ανάμειξη μπορούν να βρεθούν στα Σύνολα βοήθειας ανάμειξης.|
|Εφαρμογή|Αυτό το διακριτικό τμήμα δημιουργεί ένα μητρώο που παρέχει αντιστοίχιση βασικών πληροφοριών για τον χαρακτηρισμό της κλάσης HelpBroker για χρήση στη μέθοδο HelpSet.createHelpBroker. Επιπλέον, το μητρώο αποφασίζει την προβολή ουσιών σε πελάτη για μια δεδομένη κατηγορία Εξομοίωσης.|

## Μορφή αρχείου Java HS

Τα αρχεία Java HS είναι σε μορφή αρχείου XML και βασίζονται στην προτεινόμενη σύσταση του World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Αυτό σημαίνει ότι ένα αρχείο Java HS είναι σε μορφή αρχείου XML αναγνώσιμη από τον άνθρωπο που μπορεί να ανοίξει σε οποιαδήποτε εφαρμογή ανάγνωσης XML.

### Παράδειγμα μορφής αρχείου Java HS

Το παρακάτω είναι ένα παράδειγμα αρχείου συνόλου βοήθειας από το [Oracle Helpset documentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## βιβλιογραφικές αναφορές
* [Αρχείο Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Μορφή αρχείου σεναρίου Haskell

## Τι είναι ένα αρχείο HS;

Ένα αρχείο με επέκταση .hs είναι ένα αρχείο Haskell Script που είναι γραμμένο σε [Haskell](https://wiki.haskell.org/Haskell), μια προηγμένη καθαρά λειτουργική γλώσσα προγραμματισμού ανοιχτού κώδικα. Ο κώδικας που είναι γραμμένος σε αρχείο HS βασίζεται καθαρά σε λειτουργίες, σε αντίθεση με τα [C](/el/programming/c/), [C++](/el/programming/cpp/) και παρόμοια, που ακολουθούν τις αρχές της ταχείας ανάπτυξης ενός ισχυρού και συνοπτικού λογισμικού. Η Haskell παρέχει ενσωματωμένη ταυτοποίηση και παραλληλισμό μαζί με πλούσια API, profilers και προγράμματα εντοπισμού σφαλμάτων για την παραγωγή ευέλικτων και υψηλής ποιότητας εφαρμογών.

## Μορφή αρχείου HS

Όπως κάθε γλώσσα προγραμματισμού, τα αρχεία HS είναι γραμμένα σε μορφή απλού κειμένου που είναι αναγνώσιμα από τον άνθρωπο. Αυτά μπορούν να δημιουργηθούν, να επεξεργαστούν και να προβληθούν με οποιαδήποτε διαθέσιμα εργαλεία κειμένου. Το αρχείο πηγαίου κώδικα .hs μεταγλωττίζεται με έναν μεταγλωττιστή Haskell, δημιουργώντας το εκτελέσιμο δυαδικό αρχείο.

### Παράδειγμα μορφής αρχείου HS

Ο κώδικας μπορεί να γραφτεί σε ένα αρχείο .hs και να μεταγλωττιστεί χρησιμοποιώντας έναν μεταγλωττιστή Haskell όπως το [GHC](https://haskell.org/ghc). Η ακόλουθη γραμμή κώδικα αποθηκεύεται ως «HelloWorld.hs», όπως φαίνεται στο παρακάτω δείγμα.

```
main = putStrLn "Hello, World!"
```

Αυτό μεταγλωττίζεται χρησιμοποιώντας την εντολή:

```
$ ghc -o hello hello.hs
```
και το εκτελέσιμο αρχείο που προκύπτει μπορεί να εκτελεστεί ως:

```
$ ./hello
```
Αυτό τυπώνει το "Hello, World!" δήλωση στην έξοδο.

## βιβλιογραφικές αναφορές

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell σε 5 εύκολα βήματα](https://wiki.haskell.org/Haskell_in_5_steps)

