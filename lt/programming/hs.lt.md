{
  "date": "2021-04-21",
  "keywords": [
"kas yra HS failas",
"HS vadovėliai",
"HS reiškia",
"HS",
"HS failai",
"pratęsimas",
"formatu",
"HS pamoka",
".hs",
"HS pavyzdys",
"hs failo plėtinys",
"kaip atidaryti hs failą"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS – Haskell scenarijaus failo formatas",
  "description": "Sužinokite, kas yra HS failo formatas ir API, kuriomis galima kurti ir atidaryti HS failus.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-lts"
}
},
  "lastmod": "2021-06-15"
}

# HS – Java HelpSet failo formatas

## Kas yra Java HS failas?

Failas su plėtiniu .hs Java programavimo kalba yra žinyno dokumentacijos failas, kurį naudoja JavaHelp sistema, kai ją suaktyvina programa. Jis apibrėžia konkrečios įdiegtos programos pagalbos rinkinį ir susideda iš kelių pogrupių kaip programos sistemos pagalbos dalis. Java programa turi sugebėti rasti helpet failą, kurio pavadinimas baigiasi .hs plėtiniu.

## Java pagalbos rinkinio informacija

.hs faile gali būti ši informacija.

|Informacija|Aprašymas|
---|---|
|Žemėlapio failas|Žemėlapio failas naudojamas susieti temų ID su vienodu šaltinio ieškikliu arba hiperteksto žymėjimo kalbos temų failų kelio pavadinimu.|
|Žiūrėti informaciją|Informacija, apibūdinanti pagalbiniame rinkinyje naudojamus navigatorius. kokybės navigatoriai yra: turinys, rodyklė ir viso teksto paieška. Kiti navigatoriai apima blizgesį ir mėgstamiausius navigatorius. duomenys apie pasirinktinius navigatorius pateikiami čia toliau.|
|Pagalbos rinkinio pavadinimas|<title> yra aprašyta helpet (.hs) faile. Šis pavadinimas atrodo aukščiausias iš didžiausių langų ir visų antrinių langų, nurodytų jūsų pagalbos rinkinyje.|
|Namų ID|(numatytasis) ID, kuris rodomas, kai iškviečiamas pagalbos stebėtojas, nenurodant ID, pavadinimas.|
|Pristatymas|Langai, kuriuose rodomi pagalbos subjektai. Tai gali būti modernus JavaHelp 2 kompiuterinės programos, kuri išsamiau pavaizduota žemiau \<presentation> .|
|Pagalbiniai rinkiniai|Ši pasirinktinė sritis statiškai įtraukia kitus pagalbinius rinkinius, naudodama žymą. Šios žymos rodomi pagalbos rinkiniai natūraliai sujungiami į žinyną, kuriame yra žyma. Daugiau įdomių vietų, susijusių su maišymu, rasite maišymo pagalbos rinkiniuose.|
|Įdiegimas|Šis pasirenkamas segmentas sudaro registrą, kuriame pateikiama pagrindinė informacija, apibūdinanti HelpBroker klasę, kurią galima naudoti naudojant HelpSet.createHelpBroker metodą. Be to, registras nusprendžia, ar cheminės medžiagos peržiūros priemonė bus teikiama klientui tam tikram emuliatoriaus rūšiavimui.|

## Java HS failo formatas

Java HS failai yra XML failo formatu ir yra pagrįsti World Wide Web Consortium (W3C) Extended Markiup Language pasiūlyta rekomendacija [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Tai reiškia, kad Java HS failas yra žmogaus skaitomo XML failo formatu, kurį galima atidaryti bet kurioje XML skaitytuvo programoje.

### Java HS failo formato pavyzdys

The following is an example of a helpset file as from [Oracle Helpset documentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Nuorodos
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS – Haskell scenarijaus failo formatas

## Kas yra HS failas?

Failas su plėtiniu .hs yra Haskell scenarijaus failas, parašytas [Haskell](https://wiki.haskell.org/Haskell), pažangia grynai funkcine atvirojo kodo programavimo kalba. HS faile parašytas kodas yra pagrįstas funkcijomis, skirtingai nei [C](/programming/c/), [C++](/programming/cpp/) ir panašiai, kurios vadovaujasi greito tvirtos ir glaustos programinės įrangos kūrimo principais. Haskell teikia integruotą lygiagretumą ir lygiagretumą kartu su turtingomis API, profiliavimo ir derinimo priemonėmis, kad sukurtų lanksčias ir aukštos kokybės programas.

## HS failo formatas

Kaip ir bet kuri programavimo kalba, HS failai yra parašyti paprasto teksto formatu, kuris yra suprantamas žmonėms. Juos galima kurti, redaguoti ir peržiūrėti naudojant bet kokius turimus teksto įrankius. Šaltinio kodo failas .hs kompiliuojamas naudojant Haskell kompiliatorių, generuojantį vykdomąjį dvejetainį failą.

### HS failo formato pavyzdys

Kodą galima įrašyti į .hs failą ir sukompiliuoti naudojant Haskell kompiliatorių, pvz., [GHC](https://haskell.org/ghc). Ši kodo eilutė išsaugoma kaip HelloWorld.hs, kaip parodyta kitame pavyzdyje.

```
main = putStrLn "Hello, World!"
```

Tai sukompiliuojama naudojant komandą:

```
$ ghc -o hello hello.hs
```
ir gautą vykdomąjį failą galima paleisti kaip:

```
$ ./hello
```
Tai išspausdina Sveikas, pasauli! pareiškimas prie išvesties.

## Nuorodos

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell 5 paprastais žingsniais](https://wiki.haskell.org/Haskell_in_5_steps)

