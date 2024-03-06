{
  "date": "2020-01-10",
  "keywords": [
"otg failu",
"otg faila formātā",
"kas ir otg fails",
"failu",
"otg piemērs",
"otg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG — OpenDocument zīmēšanas veidnes faila formāts",
  "description": "Uzziniet par OTG faila formātu un API, kas var izveidot un atvērt OTG failus.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-lvg"
}
},
  "lastmod": "2020-01-10"
}

## Kas ir OTG fails?

OTG fails ir zīmēšanas veidne, kas izveidota, izmantojot OpenDocument standartu, kas seko OASIS Office lietojumprogrammām [1.0 specification](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Tas attēlo vektora attēla zīmēšanas elementu noklusējuma organizāciju, ko var izmantot, lai vēl vairāk uzlabotu faila saturu. OTF faili ir tāpat kā visi citi OpenDocument formāta faili, kuru pamatā ir XML formāts, lai attēlotu dokumenta saturu. OTF failus var apskatīt, atverot tos jebkurā teksta vai standarta XML redaktorā.

## OTG faila formāta specifikācijas ##

OTG faila formāts ir balstīts uz OpenDocument XML formātu, kuram ir labi izveidota shēma. Katra OpenDocument formāta komponenta struktūra ir attēlota ar elementu, kuram ir saistīti atribūti un kas ir kopīgs visiem dokumentu veidiem, piemēram, teksta dokumentam, izklājlapai vai zīmējuma failam. OTG, kas ir zīmēšanas veidne, plaši izmanto grafikas satura specifikācijas, kas ietver:

  * Uzlabotas lapu funkcijas grafiskām lietojumprogrammām
  * Formu zīmēšana
  * Rāmji
  * 3D formas
  * Pielāgota forma
  * Prezentācijas formas
  * Prezentāciju animācijas
  * SMIL prezentāciju animācijas
  * Prezentācijas pasākumi
  * Prezentēt teksta laukus
  * Prezentācijas dokumenta saturs

### Uzlabotas lapu funkcijas grafiskām lietojumprogrammām ###
#### Izdales materiāla meistars ####

Izdales materiāla pamatelements ir veidne automātiskai izdales materiālu lapu ģenerēšanai lietojumprogrammām, kas atbalsta šādu lapu drukāšanu.
Atribūti, kas var būt saistīti ar `<style:handout-master> ` elementi ir:

|Izkārtojums|Atribūts|Apraksts
---|---|---|
|Prezentācijas lapas izkārtojums|presentation:presentation-page-layout-name|Saites uz `<style:presentation-page-layout> ` atribūts
|Lapas izkārtojums|`stils:lapas izkārtojuma nosaukums` | Norāda lapas izkārtojumu, kurā ir izdales materiāla šablona lapas izmēri, apmale un orientācija.
|Lapas stils|`draw:style-name`|Piešķir izdales materiāla šablonam papildu formatējuma atribūtus, piešķirot zīmējuma lapas stilu.|
|Galvenes deklarācija| `presentation:use-header-name`| Norāda galvenes lauka deklarācijas nosaukumu, kas tiek izmantots visiem galvenes laukiem, kas tiek parādīti izdales materiāla šablona lapā.
|Kājenes deklarācija| prezentācija:use-footer-name|Norāda kājenes lauka deklarācijas nosaukumu, kas tiek izmantots visiem kājenes laukiem, kas tiek parādīti izdales materiāla šablona lapā.
|Datuma un laika deklarācija|use-date-time-name|Norāda datuma un laika lauka deklarācijas nosaukumu, kas tiek izmantots visiem datuma un laika laukiem, kas tiek parādīti izdales materiāla šablona lapā.

### Formu zīmēšana ###
OpenDocument formāts atbalsta vairākas zīmēšanas formas, kuras var izmantot jebkura veida dokumentos.

|Forma|Saistītie atribūti| elementi
---|---|---|
Taisnstūris — `<draw:rect> `|Pozīcija, izmērs, stils, slānis, Z-indekss, ID, paraksta ID, teksta enkurs, tabulas fons, zīmēšanas beigu pozīcija, apaļie stūri|nosaukums, garš apraksts, notikumu uztvērēji, līmes punkti, teksts
Līnija `<draw:line> `|Stils, slānis, Z-indekss, ID, paraksta ID un transformācija, teksta enkurs, tabulas fons, zīmēšanas beigu pozīcija, sākuma punkts, beigu punkts|nosaukums, garš apraksts, notikumu uztvērēji, līmes punkti, teksts
Polyline `<draw:polyline> `| Pozīcija, izmērs, skata lodziņš, stils, slānis, Z-indekss, ID, paraksta ID un transformācija, teksta enkurs, tabulas fons, zīmēšanas gala pozīcija, punkti| Virsraksts, garš apraksts, notikumu klausītāji, līmes punkti, teksts
Daudzstūris `<draw:polygon> `|Pozīcija, izmērs, skata lodziņš, stils, slānis, Z-indekss, ID, paraksta ID un transformācija, teksta enkurs, tabulas fons, zīmēšanas beigu pozīcija, punkti|nosaukums, garš apraksts, notikumu uztvērēji, līmes punkti, teksts
|Regulārais daudzstūris `<draw:regular-polygon> `|Pozīcija, izmērs, stils, slānis, Z-indekss, ID, paraksta ID un transformācija, teksta enkurs, tabulas fons, zīmēšanas beigu pozīcija, ieliekts, stūri, asums|nosaukums, garš apraksts, notikumu uztvērēji, līmes punkti, teksts
|Paht `<draw:path> `|Pozīcija, izmērs, skata lodziņš, stils, slānis, Z-indekss, ID, paraksta ID un transformācija, teksta enkurs, tabulas fons, zīmēšanas beigu pozīcija, ceļa dati| Virsraksts, garš apraksts, notikumu uztvērēji, līmes punkti, teksts

### Rāmji ###
Rāmis rasējuma dokumentā ir taisnstūrveida konteiners, kurā ir tekstlodziņi, attēli vai objekti. Rāmji atbalsta papildu funkcijas, piemēram, kontūras, attēlu kartes un hipersaites. Rāmī var būt gan objekts, gan attēls, tādējādi ļaujot izmantot vairākus objekta atveidojumus. Lietojumprogrammas atveido attiecīgo elementu, pamatojoties uz labāko atbalstu.

Rāmji var saturēt:
  * Tekstlodziņi
  * Objekti, kas attēloti OpenDocument formātā vai objektam specifiskā binārajā formātā
  * Attēli
  * Sīklietotnes
  * Spraudņi
  * Peldošie rāmji

Rāmis ir ietverts dokumentā, kā parādīts tālāk.

```
<define name=draw-frame>
<element name=draw:frame>
<ref name=common-draw-shape-with-text-and-styles-attlist/>
<ref name=common-draw-position-attlist/>
<ref name=common-draw-rel-size-attlist/>
<ref name=common-draw-caption-id-attlist/>
<ref name=presentation-shape-attlist/>
<ref name=draw-frame-attlist/>
<zeroOrMore>
<choice>
<ref name=draw-text-box/>
<ref name=draw-image/>
<ref name=draw-object/>
<ref name=draw-object-ole/>
<ref name=draw-applet/>
<ref name=draw-floating-frame/><ref name=draw-plugin/>
</choice>
</zeroOrMore>
<optional>
<ref name=office-event-listeners/>
</optional>
<zeroOrMore>
<ref name=draw-glue-point/>
</zeroOrMore>
<optional>
<ref name=draw-image-map/>
</optional>
<optional>
<ref name=svg-title/>
</optional>
<optional>
<ref name=svg-desc/>
</optional>
<optional>
<choice>
<ref name=draw-contour-polygon/><ref name=draw-contour-path/>
</choice>
</optional>
</element>
</define>
```

## Atsauces Nr.
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)

* [OpenDocument formāts — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


