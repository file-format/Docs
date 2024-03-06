{
  "date": "2019-12-12",
  "keywords": [
"JT",
"failu",
"pagarinājumu",
"formātā",
"3D fbx",
""
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par JT faila formātu un API, kas var izveidot un atvērt JT failus.",
  "title": "JT — Jupitera Tesselācijas faila formāts",
  "linktitle": "JT",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-j-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir JT fails?

**JT** (Jupiter Tessellation) ir efektīvs, uz nozari vērsts un elastīgs ISO standartizēts 3D datu formāts, ko izstrādājusi Siemens PLM Software. Aviācijas un kosmosa, automobiļu rūpniecības un smago iekārtu mehāniskie CAD domēni izmanto JT kā vadošo 3D vizualizācijas formātu.

JT formāts ir ainas grafiks, kas atbalsta CAD specifiskus atribūtus un mezglus. Fasetes datu (trīsstūru) glabāšanai tiek izmantotas sarežģītas saspiešanas metodes. Šis formāts ir strukturēts, lai atbalstītu vizuālos atribūtus, informāciju par produktu un ražošanu (PMI) un metadatus. Ir labs atbalsts asinhronai satura straumēšanai. Smagajā mehāniskajā rūpniecībā profesionāļi izmanto JT failu savos CAD risinājumos un produktu dzīves cikla pārvaldības (PLM) programmatūras programmās, lai pārbaudītu sarežģītu preču ģeometriju.

As JT supports nearly all important 3D CAD formats its assembly can deal with a variety of combination which is known as "multi-CAD". This multi-CAD assembly is always well managed and up-to-date because synchronization among native CAD product description files with their associated JT files takes place automatically. JT files are originally lightweight, so considered to be suitable for internet collaborations. Companies Collaborate through sending 3D visualizations over the media much more easily as compared to “heavy" original CAD files. In addition, JT files ensures many security feature that make intellectual property sharing more secure.

## Īsa JT faila formāta vēsture

Engineering Animation, Inc. un Hewlett Packard bija sākotnējie JT dizaineri, kuri izstrādāja šo formātu kā tiešā modeļa rīkkopu. Pēc tam, kad UGS Corp iegādājās EAI, JT kļuva par UGS komplekta daļu. 2007. gada sākumā UGS paziņoja par JT kā savu galveno 3D formātu. Tajā pašā gadā Siemens AG iegādājās UGS un izrādījās Siemens PLM programmatūra. Siemens izmanto JT kā kopējo sadarbspējas formātu un datu arhīva formātu. 2009. gadā ISO akceptēja JT specifikāciju publicēšanai kā ISO publiski pieejamu specifikāciju (PAS). 2010. gada vidū ProSTEP iViP paziņoja, ka rūpnieciskā līmenī JT un STEP AP 242 XML var izmantot kopā, lai sasniegtu maksimālu datu priekšrocību. apmaiņas scenāriji. 2012. gadā JT ir oficiāli pasludināts par ISO standartizētu (ISO 14306:2012 (ISO JT V1)) 3D vizualizācijas formātu.

## JT faila formāts ##

Visi objekti JT formātā tiek attēloti, izmantojot objekta identifikatoru, un atsauces starp objektiem tiek apstrādātas, izmantojot atsauces objekta identifikatoru. Šo objektu atsauču integritāti var uzturēt, izmantojot norādes unswizzling/swizzling.

JT fails ir sakārtots kā bloku sērija, un galvenes bloks vienmēr ir pirmais datu bloks failā. Virkne datu segmentu un TOC segmentu uzreiz seko galvenes blokam. Vienam datu segmentam (6 LSG segmentam) vienmēr ir atsauces saderīgs JT fails. TOC segments satur visu pārējo šī faila datu segmentu atrašanās vietas informāciju.

!["JT File Format"](../3d/JT-1.png "JT File Format")

### Faila galvene ###

Faila galvene ir pirmais bloks JT faila datu hierarhijā. Versiju informācija un TOC atrašanās vietas informācija ir iekļauta galvenē, kas atvieglo ielādētāju failu lasīšanu. Faila galvenes saturs ir sakārtots šādi.

### TOC segments ###

TOC segmentam ir jābūt failā, un tajā jāiekļauj visu pārējo datu segmentu identifikācijas un atrašanās vietas informācija. TOC segmenta faktisko atrašanās vietu nosaka faila galvenes lauks TOC Offset. Katrs atsevišķi adresējams datu segments tiek attēlots ar TOC ierakstu TOC segmentā.

### Datu segments ###

JT fails definē visus datu segmentā saglabātos datus. Daži datu segmenti var saspiest visus segmentā palikušās informācijas datu baitus. Datu segmentiem ir šāda struktūra:

![JT Data Segment](../3d/JT-2.png "JT Data Segment")

Šajā tabulā ir aprakstīti dažāda veida datu segmenti.

|Vārds|Apraksts
---|---|
|LSG segments|Ietver objektu kolekciju, kas ir saistītas, izmantojot vērstas atsauces, lai izveidotu LSG (virzīta acikliska grafika struktūra)
|Shape LOD segments|satur ģeometrisko formu definējošos datus (piemēram, virsotnes, normas, daudzstūri utt.)
|JT B-Rep segments|Datu elements, kas attēlo precīzu ģeometrisko robežu atsevišķai daļai JT B-Rep formātā.
|XT B-Rep segments|Ar elementu datiem, kas attēlo precīzu ģeometrisko robežu atsevišķai daļai robežas attēlojuma formātā
|Wireframe segment|Dati atspoguļo precīzu 3D karkasu konkrētai daļai, ko nosaka šajā segmentā ietvertais elements.
|Meta datu segments|Ļauj saglabāt metadatus atšķirīgos adresējamos segmentos.
|JT ULP segments|Ar elementu datiem, kas attēlo daļēji precīzu ģeometrisko robežu atsevišķai daļai JT ULP formātā.
|JT LWPA segments|Satur elementu, kas nosaka analītiskos datus konkrētai daļai. LWPA iekļauj analītisko virsmu kolekciju detaļas b-rep definīcijā.

## Saspiešana ##

3D modeļu pārraides un uzglabāšanas prasības ir augstākas, tāpēc JT faili var izmantot saspiešanas priekšrocības. JT datu modelis var sastāvēt no dažādiem failiem, izmantojot dažādus saspiešanas paņēmienus, bet saspiešanas process ir pārredzams JT datu lietotājam.

Līdz šim JT Open Toolkit (kā standarts) un uzlabotā saspiešana ir divas saspiešanas metodes, ko izmanto JT faili. JT Open Toolkit izmanto vienkāršu, bezzudumu saspiešanas algoritmu, savukārt uzlabotā saspiešana izmanto pilnveidotu, domēnam raksturīgu saspiešanas paņēmienu, kas rada zudumu ģeometrijas saspiešanu. Klientu lietojumprogrammas dod priekšroku uzlabotai saspiešanai, nevis standarta saspiešanai, jo uzlabotā saspiešana nodrošina diezgan augstu saspiešanas pakāpi. Atgriezeniskā saderība ar parastajām JT failu skatīšanas lietojumprogrammām tiek uzturēta, nodrošinot standarta saspiešanu. Saspiešanas formai jābūt saderīgai ar JT faila formāta versiju, ko var redzēt, kad JT fails tiek atvērts, izmantojot teksta redaktoru, un iekļauts ASCII galvenes informācijā.

## Atsauces Nr.

* [JT faila formāta atsauce](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)

* [JT (vizualizācijas formāts)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)


