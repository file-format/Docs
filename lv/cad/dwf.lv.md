{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Faila formāts",
"Atvērt",
"Lasīt",
"Izveidot",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Learn about DWF file format and APIs that can create and open DWF files.",
  "title": "DWF File Format",
  "linktitle": "DWF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dwf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DWF fails?

Design Web Format (DWF) attēlo 2D/3D zīmējumu saspiestā formātā, lai skatītu, pārskatītu vai drukātu dizaina failus. Tajā ir grafika un teksts kā daļa no dizaina datiem, un tas samazina faila lielumu tā saspiestā formāta dēļ. Samazinātais faila lielums padara bagātīgu dizaina datu izplatīšanu un saziņu efektīvu. DWF neprasa, lai saņēmējs zinātu par CAD programmatūras izmantošanu, kas izveidoja sākotnējo zīmējumu. DWF faila formāta saturs var būt vienkāršs un ietvert tikai vienu lapu vai pietiekami sarežģīts, lai tajā būtu fonti, krāsas un attēli.

## Īsa vēsture ##

Autodesk ieviesa DWF faila formātu 1995. gadā kā daļu no Netscape navigācijas spraudņa WHIP. Formāts attīstījās no tikai 2D formāta, lai iekļautu 3D saturu laika gaitā. Šo formātu izmanto arī daudzas trešo pušu lietojumprogrammas.

## DWF faila formāts ##

DWF ir atvērts, drošs formāts, kas īpaši izstrādāts bagātīgu inženiertehnisko projektu datu kopīgošanai. Tas nav atkarīgs no sākotnējās lietojumprogrammatūras, aparatūras un operētājsistēmas, kas izmantota šo dizaina datu izveidei. Tas ļauj komandas locekļiem, kuri neizmanto CAD lietojumprogrammas, piedalīties digitālajos procesos, apskatot ēku, ĢIS vai produktu projektus. DWF failu arhīvs sastāv no vairākiem XML un bināriem failiem, kas ir iesaiņoti kopā saspiestā arhīvā, kas izveidots ar [ZIP](/compression/zip/) saspiešanu. Varat pārdēvēt DWF faila paplašinājumu uz ZIP un skatīt faila saturu. DWF pakotnē var būt dažāda veida dizaina dati, piemēram, 2D grafikas, 3D grafikas, pakotņu un sadaļu metadati un citi resursu faili.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Resursu faili** — multivides vai citi satura faili, uz kuriem ir atsauces no pakotnes/sadaļas metadatiem un kas parasti ir dizaina datu prezentācijas dažādos formātos (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/) utt.)

### Faila formāta informācija ###

DWF faili ir sakārtoti trīs galvenajās sadaļās, kā parādīts tālāk.

* Faila identifikācijas galvene

* Failu datu bloks

* Failu izbeigšanas piekabe


#### Faila identifikatora galvene ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|Baits|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Rakstzīme|(|D|W|F|(atstarpe)|V|0|0|.|3|0|)

Šeit ir šīs tabulas kopsavilkums:

* Galvenes pirmie seši baiti vienmēr ir ASCII rakstzīmes "(DWF V"

* Šie 5 baiti satur informāciju par versijas numuru, piemēram, "00.30" ar formāta galvenās un mazās versijas vērtību


Lietojumprogrammām, kas veido DWF failu, ir jānorāda mazākais iespējamais versijas numurs, kas jāatbalsta lasītāja lietojumprogrammai, lai pareizi izmantotu datus.

#### Faila datu bloks ####

Faila datu bloks sākas ar DWF faila 13. baitu, un tas ir opkoda un operandu pāru sērija, kā parādīts nākamajā tabulā.

| 1. lauks | 2. lauks | 3. lauks | 4. lauks | 5. lauks | 5. lauks
--- | --- |--- | --- |--- | --- |
|operands|operands|operands|operands|operands

DWF fails var saturēt opkoda-operandu pārus kā lasāmu ASCII, kā arī bināro kodu vai abu to kombināciju. Visām DWF operācijām ir lasāma ASCII opkoda/operanda forma, un lielākajai daļai operāciju ir arī kodēta binārā opkoda/operanda forma. Opkodi ir vienā baitā, kas ļauj veikt vairāk nekā 200 darbības. Paplašināts ASCII un paplašinātais binārais ir izņēmuma gadījumi. Opcodes vērtības var būt no 0 līdz 255 ar dažiem izņēmumiem. Izņemot divus īpašos opkodu veidus, paplašināto ASCII un paplašināto bināro kodu, failu lasītājam ir jāzina, kā aprēķināt operanda garumu.

##### Aizliegtie opkodi #####

ASCII attēlojumus nevar izmantot kā operācijas kodus:

Kā operācijas kodus nevar izmantot šādus ASCII attēlojumus:

* Atstarpe (0x20)

* Cilne (0x09)

* Defise (0x2D)

* ASCII cipari 0–9 (0 x 30 – 0 x 39)

* Vagona atgriešana (0x0D)

* Līnijas padeve (0x0A)

* Viena pēdiņa (0x27)

* Dubultās pēdiņas (0x22)

* Periods (0x2E)

* Iekavas (0x28 un 0x29)

* Cirtainas iekavas (0x7B un 0x7D)

* Kvadrātiekavas (0x5B un 0x5D)

* Slīpssvītra (0 x 5 C)


#### Faila pārtraukšanas reklāmkadri ####

DWF faila beigu reklāmkadri ir vienkārši īpašs opkods, kas norāda faila beigas. Dažas lietojumprogrammas var saglabāt datus, kas nav DWF, pēc beigu darbības koda. Reklāmkadri ir šādi:


|Baits|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Rakstzīme|(|E|n|d|0|f|D|W|F|)

## Atsauces Nr.

* [DWF — Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)

* [WHIP datu formāts](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs /opc/adventures-in-packaging-episode-1)


