{
  "date": "2021-04-21",
  "keywords": [
"cad is comhad HS ann",
"Teagaisc ar HS",
"Ciallaíonn HS",
"HS",
"Comhaid HS",
"síneadh",
"formáid",
"Teagaisc HS",
".hs",
"Sampla HS",
"síneadh comhad hs",
"Conas comhad hs a oscailt"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS - Formáid Chomhaid Script Haskell",
  "description": "Foghlaim faoi cad is formáid comhaid HS ann agus APIanna ar féidir comhaid HS a chruthú agus a oscailt.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-gas"
}
},
  "lastmod": "2021-06-15"
}

# HS - Java HelpSet Formáid Chomhaid

## Cad is comhad Java HS ann?

Is comhad doiciméadaithe cabhrach é comhad le síneadh .hs i dteanga ríomhchlárúcháin Java a úsáideann an córas JavaHelp nuair a ghníomhaíonn feidhmchlár é. Sainmhíníonn sé an tacar cabhrach don fheidhmchlár ar leith atá suiteáilte agus cuimsíonn sé fo-thacair iolracha mar chuid den chabhair chórais don fheidhmchlár. Caithfidh an clár Java a bheith in ann an comhad tacair chabhrach a aimsiú a chríochnaíonn a ainm leis an síneadh .hs.

## Eolas faoi Thacar Cabhrach Java

Féadfaidh an fhaisnéis seo a leanas a bheith i gcomhad .hs.

|Faisnéis|Cur Síos|
---|---|
|Comhad Léarscáileanna|Úsáidtear an comhad léarscáile chun aitheantais topaicí a cheangal leis an aimsitheoir acmhainne aonfhoirmeach nó le hainm cosáin na gcomhad topaicí teanga marcála hipirtéacs.|
|Féach ar an bhfaisnéis|Faisnéis a chuireann síos ar na loingseoirí atá á bhfostú laistigh den tacar cabhrach. Is iad na loingseoireachtaí cáilíochta ná: clár na n-ábhar, innéacs, agus cuardach téacs iomlán. I measc na n-loingseoireachtaí eile tá an snas agus na loingseoireachtaí is ansa leat. tá sonraí maidir le loingseoirí saincheaptha faoi iamh anseo a thuilleadh.|
|Teideal cabhrach|An \<title> leagtha amach sa chomhad tacair chabhrach (.hs). Is cosúil go bhfuil an teideal seo ag an gceann is airde den fhuinneog is mó agus ar aon fhuinneoga tánaisteacha atá leagtha amach i do chomhad tacair chabhrach.|
|Aitheantas baile|Teideal an aitheantais (réamhshocraithe) a thaispeánfar nuair a ghlaotar ar an bhfaireadóir cúnaimh gan aitheantas a thabhairt.|
|Cur i láthair|Na fuinneoga inar féidir na hábhair chúnaimh a thaispeáint. Féadfaidh sé seo a bheith ina áireamh nua-aimseartha den ríomhchlár JavaHelp 2 a léirítear níos mine thíos faoi \<presentation> .|
|Fo-thacairí|Comhchorpraíonn an réimse roghnach seo tacair chabhracha eile go statach trí úsáid a bhaint as an gclib. Comhcheanglaítear na tacair cabhrach a thaispeánann an chlib seo go nádúrtha isteach sa tacar cabhrach ina bhfuil an chlib. Tá níos mó pointí spéise maidir le cumasc le fáil i gCeisteanna Cabhracha Cumaisc.|
|Cur i bhFeidhm|Déanann an mhír roghnach seo clárlann a thugann mapáil faisnéise bunriachtanaí chun an aicme HelpBroker a thréithriú le húsáid laistigh den mhodh HelpSet.createHelpBroker. Ina theannta sin déanann an chlár a chinneadh an t-amharcóir substaintí don chliant le haghaidh saghas áirithe Emulate.|

## Java HS Formáid Comhaid

Tá na comhaid Java HS i bhformáid comhaid XML agus tá siad bunaithe ar mholadh molta Teanga Marcáil Leathnaithe Cuibhreannas an Ghréasáin Dhomhanda (W3C) [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Ciallaíonn sé seo go bhfuil comhad Java HS i bhformáid comhaid XML inléite ag an duine ar féidir a oscailt in aon fheidhmchlár léitheora XML.

### Sampla Formáid Comhaid Java HS

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

## Tagairtí
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Formáid Chomhaid Script Haskell

## Cad is comhad HS ann?

Is comhad Script Haskell é comhad a bhfuil iarmhír .hs air agus scríobhtar i [Haskell](https://wiki.haskell.org/Haskell), ardtheanga ríomhchláraithe foinse oscailte atá ag feidhmiú go hiomlán. Tá an cód scríofa i gcomhad HS bunaithe go hiomlán ar fheidhmeanna, murab ionann agus [C](/programming/c/), [C++](/programming/cpp/) agus araon, a leanann na prionsabail a bhaineann le forbairt tapa bogearraí stóinsithe agus beacht. Soláthraíonn Haskell comhairgeadra agus comhthreomhaireacht ionsuite mar aon le API saibhir, próifíleoirí agus dífhabhtóirí chun feidhmchláir sholúbtha agus ardcháilíochta a tháirgeadh.

## Formáid Chomhaid HS

Cosúil le haon teanga ríomhchlárúcháin, scríobhtar comhaid HS i bhformáid gnáth-théacs atá inléite ag daoine. Is féidir iad seo a chruthú, a chur in eagar agus a fheiceáil le haon uirlisí téacs atá ar fáil. Tiomsaítear an comhad cód foinse .hs le tiomsaitheoir Haskell, a ghineann an comhad dénártha inrite.

### HS Sampla Formáid Comhaid

Is féidir cód a scríobh i gcomhad .hs agus é a chur le chéile le tiomsaitheoir Haskell mar [GHC](https://haskell.org/ghc). Sábháiltear an líne cód seo a leanas mar `HelloWorld.hs` mar a thaispeántar sa sampla seo a leanas.

```
main = putStrLn "Hello, World!"
```

Déantar é seo a thiomsú leis an ordú:

```
$ ghc -o hello hello.hs
```
agus is féidir an comhad inrite mar thoradh air a rith mar:

```
$ ./hello
```
Priontálann sé seo an Dia duit, Domhanda! ráiteas don aschur.

## Tagairtí

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell In 5 Easy Steps](https://wiki.haskell.org/Haskell_in_5_steps)

