{
  "date": "2021-04-21",
  "keywords": [
"kas ir HS fails",
"pamācības par HS",
"HS nozīmē",
"HS",
"HS faili",
"pagarinājumu",
"formātā",
"HS apmācība",
".hs",
"HS piemērs",
"hs faila paplašinājums",
"kā atvērt hs failu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS — Haskell skripta faila formāts",
  "description": "Uzziniet, kas ir HS faila formāts un API, kas var izveidot un atvērt HS failus.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-lvs"
}
},
  "lastmod": "2021-06-15"
}

# HS — Java HelpSet faila formāts

## Kas ir Java HS fails?

Fails ar paplašinājumu .hs Java programmēšanas valodā ir palīdzības dokumentācijas fails, ko JavaHelp sistēma izmanto, kad to aktivizē lietojumprogramma. Tas nosaka palīdzības kopu konkrētai instalētajai lietojumprogrammai un sastāv no vairākām apakškopām kā daļu no lietojumprogrammas sistēmas palīdzības. Java programmai jāspēj atrast helpet failu, kura nosaukums beidzas ar paplašinājumu .hs.

## Java palīdzības komplekta informācija

.hs failā var būt šāda informācija.

|Informācija|Apraksts|
---|---|
|Kartes fails|Kartes fails tiek izmantots, lai saistītu tēmu ID ar vienotu resursu lokatoru vai hiperteksta iezīmēšanas valodas tēmu failu ceļa nosaukumu.|
|Skatīt informāciju|Informācija, kas apraksta palīdzības komplektā izmantotos navigatorus. kvalitātes navigatori ir: satura rādītājs, rādītājs un pilna teksta meklēšana. turpmākie navigatori ietver spīdumu un arī iecienītākos navigatorus. dati par pielāgotajiem navigatoriem ir pievienoti šeit tālāk.|
|Palīdzības kopas virsraksts|<title> ir izklāstīts helpet (.hs) failā. Šķiet, ka šis nosaukums ir augstākais no lielākajiem logiem un visiem sekundārajiem logiem, kas norādīti jūsu palīdzības kopas failā.|
|Mājas ID|(noklusējuma) ID nosaukums, kas tiek parādīts, kad tiek izsaukts palīdzības novērotājs, nenorādot ID.|
|Prezentācija|Logi, kuros parādīt palīdzības priekšmetus. Tas var būt mūsdienīgs JavaHelp 2 datorprogrammas iekļaušana, kas ir detalizētāk attēlota zem \<presentation> .|
|Apakšpalīdzības kopas|Šajā izvēles apgabalā ir statiski iekļautas citas palīdzības kopas, izmantojot tagu. Palīdzības komplekti, kas parādīti ar šo tagu, tiek dabiski apvienoti palīdzības komplektā, kurā ir atzīme. Vairāk interešu punktu par sajaukšanu var atrast sajaukšanas palīdzības komplektos.|
|Ieviešana|Šis diskrecionārais segments veido reģistru, kas nodrošina galvenās informācijas kartēšanu, lai raksturotu HelpBroker klasi, ko izmantot HelpSet.createHelpBroker metodē. Turklāt reģistrs nosaka vielas skatītāju klientam konkrētam emulācijas veidam.|

## Java HS faila formāts

Java HS faili ir XML faila formātā un ir balstīti uz World Wide Web Consortium (W3C) Extended Markiup Language ierosināto ieteikumu [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Tas nozīmē, ka Java HS fails ir cilvēkam lasāmā XML faila formātā, ko var atvērt jebkurā XML lasītāja lietojumprogrammā.

### Java HS faila formāta piemērs

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

## Atsauces
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS — Haskell skripta faila formāts

## Kas ir HS fails?

Fails ar paplašinājumu .hs ir Haskell skripta fails, kas ir rakstīts [Haskell](https://wiki.haskell.org/Haskell) — uzlabotā, tīri funkcionālā atvērtā koda programmēšanas valodā. HS failā ierakstītais kods ir balstīts tikai uz funkcijām, atšķirībā no [C](/programming/c/), [C++](/programming/cpp/) un tamlīdzīgām funkcijām, kas atbilst spēcīgas un kodolīgas programmatūras ātras izstrādes principiem. Haskell nodrošina iebūvētu vienlaicīgumu un paralēlismu, kā arī bagātīgas API, profilētājus un atkļūdotājus, lai izveidotu elastīgas un augstas kvalitātes lietojumprogrammas.

## HS faila formāts

Tāpat kā jebkura programmēšanas valoda, HS faili ir rakstīti vienkārša teksta formātā, kas ir cilvēkiem lasāms. Tos var izveidot, rediģēt un skatīt, izmantojot jebkurus pieejamos teksta rīkus. .hs pirmkoda fails tiek kompilēts ar Haskell kompilatoru, ģenerējot izpildāmo bināro failu.

### HS faila formāta piemērs

Kodu var ierakstīt .hs failā un kompilēt, izmantojot Haskell kompilatoru, piemēram, [GHC](https://haskell.org/ghc). Nākamā koda rindiņa tiek saglabāta kā HelloWorld.hs, kā parādīts nākamajā paraugā.

```
main = putStrLn "Hello, World!"
```

Tas tiek apkopots, izmantojot komandu:

```
$ ghc -o hello hello.hs
```
un iegūto izpildāmo failu var palaist kā:

```
$ ./hello
```
Tas izdrukā Sveika, pasaule! paziņojums izvadei.

## Atsauces

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskels 5 vienkāršos soļos](https://wiki.haskell.org/Haskell_in_5_steps)

