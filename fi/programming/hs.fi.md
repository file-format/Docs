{
  "date": "2021-04-21",
  "keywords": [
"mikä on HS-tiedosto",
"HS:n opetusohjelmat",
"HS tarkoittaa",
"HS",
"HS tiedostot",
"laajennus",
"muoto",
"HS opetusohjelma",
".hs",
"HS esimerkki",
"hs tiedostopääte",
"kuinka avata hs-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS - Haskell Script -tiedostomuoto",
  "description": "Opi HS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HS-tiedostoja.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-fis"
}
},
  "lastmod": "2021-06-15"
}

# HS - Java HelpSet -tiedostomuoto

## Mikä on Java HS -tiedosto?

Java-ohjelmointikielen tiedosto, jonka tarkenne on .hs, on ohjedokumentaatiotiedosto, jota JavaHelp-järjestelmä käyttää, kun sovellus aktivoi sen. Se määrittää ohjejoukon tietylle asennetulle sovellukselle ja koostuu useista osajoukoista osana sovelluksen järjestelmäapua. Java-ohjelman on pystyttävä löytämään helpet-tiedosto, jonka nimi päättyy .hs-tunnisteeseen.

## Java-ohjesarjan tiedot

.hs-tiedosto voi sisältää seuraavat tiedot.

|Tiedot|Kuvaus|
---|---|
|Karttatiedosto|Karttatiedostoa käytetään aihetunnusten yhdistämiseen hypertekstimerkintäkielen aihetiedostojen yhtenäiseen resurssin paikantimeen tai polun nimeen.|
|Näytä tiedot|Tiedot, jotka kuvaavat helpetissä käytettäviä navigaattoreita. laatunavigaattorit ovat: sisällysluettelo, hakemisto ja koko tekstihaku. muita navigaattoreita ovat kiilto ja myös suosikkinavigaattorit. mukautettuja navigaattoreita koskevat tiedot ovat tämän ohessa.|
|Ohjesarjan otsikko|<title> on kuvattu helpet (.hs) -tiedostossa. Tämä otsikko näyttää korkeimmalta helpet-tiedostossasi määritellyistä ikkunoista ja kaikista toissijaisista ikkunoista.|
|Kodin tunnus|Oletustunnuksen otsikko, joka näytetään, kun avustusvartijaa kutsutaan ilmoittamatta tunnusta.|
|Esitys|Ikkunat, joissa näytetään avun aiheet. Tämä voi olla moderni versio JavaHelp 2 -tietokoneohjelmasta, joka on kuvattu yksityiskohtaisemmin alla \<presentation> .|
|Ala-apujoukot|Tämä harkinnanvarainen alue sisältää staattisesti muita apusarjoja käyttämällä tunnistetta. Tämän tunnisteen osoittamat apujoukot yhdistetään luonnollisesti tunnisteen sisältäväksi helpetiksi. Lisää yhdistämiseen liittyviä kiinnostavia kohteita löytyy sekoitusohjeista.|
|Toteutus|Tämä harkinnanvarainen segmentti muodostaa rekisterin, joka antaa avaintietokartoituksen HelpBroker-luokan luonnehtimiseksi käytettäväksi HelpSet.createHelpBroker-menetelmässä. Rekisteri lisäksi päättää aineen katseluohjelmasta asiakkaalle tietylle emulointilajittelulle.|

## Java HS -tiedostomuoto

Java HS -tiedostot ovat XML-tiedostomuodossa ja perustuvat World Wide Web Consortium (W3C) Extended Markiup Language -ehdotukseen [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Tämä tarkoittaa, että Java HS -tiedosto on ihmisen luettavassa XML-tiedostomuodossa, joka voidaan avata missä tahansa XML-lukijasovelluksessa.

### Esimerkki Java HS -tiedostomuodosta

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

## Viitteet
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script -tiedostomuoto

## Mikä on HS-tiedosto?

Tiedosto, jonka tunniste on .hs, on Haskell Script -tiedosto, joka on kirjoitettu {{HYPERLINKKI}}, kehittyneellä puhtaasti toiminnallisella avoimen lähdekoodin ohjelmointikielellä. HS-tiedostoon kirjoitettu koodi perustuu puhtaasti funktioihin, toisin kuin [C](/programming/c/), [C++](/programming/cpp/) ja vastaavat, jotka noudattavat vankan ja tiiviin ohjelmiston nopean kehityksen periaatteita. Haskell tarjoaa sisäänrakennetun samanaikaisuuden ja rinnakkaisuuden sekä monipuoliset API:t, profiloijat ja virheenkorjausohjelmat joustavien ja laadukkaiden sovellusten tuottamiseksi.

## HS tiedostomuoto

Kuten kaikki ohjelmointikielet, HS-tiedostot on kirjoitettu pelkkätekstimuotoon, joka on ihmisen luettavissa. Niitä voidaan luoda, muokata ja tarkastella millä tahansa käytettävissä olevilla tekstityökaluilla. .hs-lähdekooditiedosto käännetään Haskell-kääntäjällä, joka luo suoritettavan binaaritiedoston.

### HS-tiedostomuodon esimerkki

Koodi voidaan kirjoittaa .hs-tiedostoon ja kääntää Haskell-kääntäjällä, kuten {{HYPERLINKKI}}. Seuraava koodirivi tallennetaan nimellä HelloWorld.hs, kuten seuraavassa esimerkissä näkyy.

```
main = putStrLn "Hello, World!"
```

Tämä käännetään komennolla:

```
$ ghc -o hello hello.hs
```
ja tuloksena oleva suoritettava tiedosto voidaan ajaa seuraavasti:

```
$ ./hello
```
Tämä tulostaa Hei, maailma! lausunto tulosteeseen.

## Viitteet

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell viidessä helpossa vaiheessa](https://wiki.haskell.org/Haskell_in_5_steps)

