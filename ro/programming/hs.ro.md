{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS – Format de fișier script Haskell",
  "description":"Aflați despre ce este un format de fișier HS și API-urile care pot crea și deschide fișiere HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet File Format

## Ce este un fișier Java HS?

Un fișier cu extensia .hs în limbajul de programare Java este un fișier de documentație de ajutor care este utilizat de sistemul JavaHelp atunci când este activat de o aplicație. Acesta definește setul de ajutor pentru aplicația particulară instalată și cuprinde mai multe subseturi ca parte a ajutorului de sistem pentru aplicație. Programul Java trebuie să poată găsi fișierul helpset al cărui nume se termină cu extensia .hs.

## Informații Java Helpset

Un fișier .hs poate conține următoarele informații.

|Informații|Descriere|
---|---|
|Fișier de hartă|Fișierul de hartă este utilizat pentru a asocia ID-urile subiectelor cu localizatorul uniform de resurse sau cu numele căii fișierelor de subiecte cu limbajul de marcare hipertext.|
|Vizualizați informații|Informații care descriu navigatorii care sunt angajați în setul de ajutor. navigatorii de calitate sunt: cuprins, index și căutare full-text. Alte navigatoare includ gloss și, de asemenea, navigatoarele favorite. datele referitoare la navigatoarele personalizate sunt incluse aici în continuare.|
<html>|Titlul setului de ajutor|The \<title> este subliniat în fișierul helpset (.hs). Acest titlu pare la cea mai înaltă dintre cele mai multe ferestre și orice ferestre secundare subliniate în fișierul helpset.| </html>
|ID de acasă|Titlul ID-ului (implicit) care este afișat atunci când observatorul de asistență este apelat fără a indica un ID.|
|Prezentare|Ferestrele în care să se arate subiectele de asistență. Aceasta poate fi o includere modernă a programului de calculator JavaHelp 2, care este prezentată mai detaliat dedesubt \<presentation> .|
|Sub-seturi de ajutor|Această zonă discreționară încorporează static alte seturi de ajutor prin utilizarea etichetei. Seturile de ajutor afișate de această etichetă sunt combinate în mod natural în setul de ajutor care conține eticheta. Mai multe puncte de interes în jurul amestecului pot fi găsite în Blending Helpsets.|
|Implementare|Acest segment discreționar realizează un registru care oferă mapare a informațiilor cheie pentru a caracteriza clasa HelpBroker de utilizat în cadrul metodei HelpSet.createHelpBroker. În plus, registrul decide vizualizatorul de substanțe să client pentru un anumit sort Emulate.|

## Format de fișier Java HS

Fișierele Java HS sunt în format de fișier XML și se bazează pe recomandarea propusă de World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Aceasta înseamnă că un fișier Java HS este în format de fișier XML care poate fi citit de om, care poate fi deschis în orice aplicație de citire XML.

### Exemplu de format de fișier Java HS

Următorul este un exemplu de fișier helpset din [documentația Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Referințe
* [Fișier Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script File Format

## Ce este un fișier HS?

Un fișier cu extensia .hs este un fișier Haskell Script care este scris în [Haskell](https://wiki.haskell.org/Haskell), un limbaj de programare open-source, pur funcțional, avansat. Codul scris în fișierul HS se bazează exclusiv pe funcții, spre deosebire de [C](/ro/programming/c/), [C++](/ro/programming/cpp/) și altele asemenea, care urmează principiile dezvoltării rapide a unui software robust și concis. Haskell oferă concurență și paralelism încorporate împreună cu API-uri bogate, profilere și depanare pentru a produce aplicații flexibile și de înaltă calitate.

## Format de fișier HS

Ca orice limbaj de programare, fișierele HS sunt scrise în format text simplu, care pot fi citite de om. Acestea pot fi create, editate și vizualizate cu orice instrumente de text disponibile. Fișierul codului sursă .hs este compilat cu un compilator Haskell, generând fișierul binar executabil.

### Exemplu de format de fișier HS

Codul poate fi scris într-un fișier .hs și compilat folosind un compilator Haskell, cum ar fi [GHC](https://haskell.org/ghc). Următoarea linie de cod este salvată ca „HelloWorld.hs”, așa cum se arată în exemplul următor.

```
main = putStrLn "Hello, World!"
```

Acesta este compilat folosind comanda:

```
$ ghc -o hello hello.hs
```
și fișierul executabil rezultat poate fi rulat ca:

```
$ ./hello
```
Aceasta afișează mesajul „Hello, World!” declarație la ieșire.

## Referințe

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell în 5 pași simpli](https://wiki.haskell.org/Haskell_in_5_steps)

