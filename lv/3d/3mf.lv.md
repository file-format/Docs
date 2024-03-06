{
  "date": "2019-12-09",
  "keywords": [
"3mf fails",
"3mf faila formāts",
"kas ir 3mf fails",
"failu",
"3mf piemērs",
"3mf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "Uzziniet par 3MF failu formātu un API, kas var atvērt un izveidot 3MF failus.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-lvf"
}
},
  "lastmod": "2019-12-09"
}

## Kas ir 3MF fails?

3MF, 3D ražošanas formāts, lietojumprogrammas izmanto, lai atveidotu 3D objektu modeļus dažādām citām lietojumprogrammām, platformām, pakalpojumiem un printeriem. Tas tika izveidots, lai izvairītos no ierobežojumiem un problēmām citos 3D failu formātos, piemēram, [STL](/cad/stl/), darbam ar jaunākajām 3D printeru versijām. 3MF ir salīdzinoši jauns faila formāts, ko ir izstrādājis un publicējis 3MF konsorcijs. Tas ir pietiekami bagāts, lai pilnībā aprakstītu modeli, saglabājot iekšējo informāciju, krāsu un citas īpašības, kas padara to paplašināmu, lai atbalstītu jaunas inovācijas 3D drukāšanā. Formāts ir paplašināms, to var plaši izmantot, un tas nav saistīts ar citiem plaši izmantotiem failu formātiem.

## Īsa 3MF faila formāta vēsture

Esošie ierobežojumi pieejamos modeļu aprakstošo failu formātos, piemēram, STL un citos, liek vadošajiem zīmoliem sanākt kopā un formulēt paplašināmāku faila formātu 3D drukāšanai. Svarīgs apsvērums bija par to, kā lietojumprogrammām būtu jānodod modeļa dati 3D printeriem. Tādējādi 3MF konsorcijs tika izveidots, lai atbalstītu jaunu 3D faila formātu, ko sauc par 3MF, ar mērķi padarīt to pietiekami paplašināmu, lai apmierinātu 3D drukāšanas vajadzības. Šajā konsorcijā bija vairāki uzņēmumi, tostarp Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP un citi. Microsoft ziedoja savu 3D faila formāta nepabeigto darbu kā sākumpunktu 3MF konsorcija turpmākajai specifikācijas izstrādei.

## 3MF faila formāts — vairāk informācijas

3MF ir uz XML balstīts datu formāts — cilvēka lasāms saspiests XML —, kas ietver definīcijas datiem, kas saistīti ar 3D ražošanu, tostarp trešo pušu paplašināmību pielāgotiem datiem. 3MF faila formāts tika izstrādāts, paturot prātā ierobežojumus un problēmas, ar kurām saskaras citi 3D failu formāti. Tā rezultātā tika izveidots 3MF faila formāts, kas ir:

* **Pilnīgs:** satur visu nepieciešamo informāciju par modeli, materiāliem un īpašumiem vienā arhīvā

* **Cilvēkam lasāms:** tādu izplatītu struktūru kā OPC, [ZIP](/compression/zip/) un XML izmantošana, lai atvieglotu izstrādi.

* **Vienkāršs:** īsa, skaidra specifikācija, kas atvieglo izstrādi un ātru validāciju

* **Paplašināms:** XML nosaukumvietu izmantošana ļauj izmantot gan publiskus, gan privātus paplašinājumus, vienlaikus saglabājot saderību.

* **Viennozīmīgs:** skaidras valodas un atbilstības testi nodrošina, ka fails vienmēr ir konsekvents no digitālā līdz fiziskajam

* **Bezmaksas:** piekļuve 3MF specifikācijai un tās ieviešana ir un vienmēr būs bez autoratlīdzības, patentiem un licencēm.


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF faila formāta specifikācijas

3MF faila formāts savam fiziskajam modelim izmanto Open Packaging specifikācijas ZIP arhīva veidā. Tas ietver labi definētu daļu un attiecību kopu, kas atbilst konkrētajam dokumenta mērķim. Tādējādi formāts atbilst pakotnes funkcijai, tostarp digitālajiem parakstiem un sīktēliem.

### 3MF dokuments — pārskats

Tipisks 3MF dokuments izskatās šādi:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Nosaukums**|**Apraksts**|**Attiecību avots**|**Obligāts/neobligāts**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Pamatrekvizīti|OPC daļa, kas satur dažādus dokumenta rekvizītus.|Package|OPCIONAL
|Digitālā paraksta izcelsme|OPC daļa, kas ir pakotnes ciparparakstu sakne.|Package|OPCIONAL
|Digitālais paraksts|OPC daļas, no kurām katra satur ciparparakstu.|Digitālā paraksta izcelsme|IZVĒLES
|Digitālā paraksta sertifikāts|OPC daļas, kas satur ciparparaksta sertifikātu.|Digitālais paraksts|IZVĒLES
|PrintTicket|Nodrošina iestatījumus, kas jāizmanto, izvadot 3D objektu(-us) 3D modeļa daļā.|3D modelis|IZVĒLES
|Sīktēls|Ietver nelielu JPEG vai PNG attēlu, kas attēlo 3D objektus pakotnē vai pakotnē kopumā.|Pakotne|IZVĒLES
|3D tekstūra|Ietver tekstūru, ko izmanto, lai 3D modeļa daļā pievienotu krāsu 3D objektam (pieejams paplašinājumiem)|3D modelis|IZVĒLES
|Pielāgotas daļas|OPC daļas, kas ir saistītas ar metadatiem|Pakotne|IZVĒLES

Specifikāciju dokumenta sadaļās [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) un [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) ir sniegta detalizēta informācija par 3MF dokumentu.

## Atsauces Nr.

* [3MF faila formāta specifikācijas](https://github.com/3MFConsortium/spec_core)

* [3MF — Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


