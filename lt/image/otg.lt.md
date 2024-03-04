{
  "date": "2020-01-10",
  "keywords": [
"otg failą",
"otg failo formatas",
"kas yra otg failas",
"failą",
"otg pavyzdys",
"otg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG – „OpenDocument“ piešimo šablono failo formatas",
  "description": "Sužinokite apie OTG failo formatą ir API, kurios gali kurti ir atidaryti OTG failus.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-ltg"
}
},
  "lastmod": "2020-01-10"
}

## Kas yra OTG failas?

OTG failas yra piešimo šablonas, sukurtas naudojant OpenDocument standartą, kuris atitinka OASIS Office Applications [1.0 specification](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Tai yra numatytasis vektorinio vaizdo piešimo elementų organizavimas, kuris gali būti naudojamas toliau tobulinti failo turinį. OTF failai yra kaip ir bet kurie kiti OpenDocument formato failai, pagrįsti XML formatu, kad atspindėtų dokumento turinį. OTF failus galima peržiūrėti atidarius juos bet kuriame teksto arba standartiniame XML rengyklėje.

## OTG failo formato specifikacijos ##

OTG failo formatas yra pagrįstas OpenDocument XML formatu, turinčiu nusistovėjusią schemą. Kiekvieno OpenDocument formato komponento struktūra pavaizduota elementu, turinčiu susietų atributų ir yra bendras visiems dokumentų tipams, pvz., tekstiniam dokumentui, skaičiuoklei ar piešinio failui. OTG, kaip piešimo šablonas, plačiai naudoja grafinio turinio specifikacijas, kurios apima:

  * Patobulintos puslapio funkcijos grafinėms programoms
  * Formų piešimas
  * Rėmeliai
  * 3D formos
  * Pasirinktinė forma
  * Pristatymo formos
  * Pristatymo animacijos
  * SMIL pristatymo animacijos
  * Pristatymo renginiai
  * Pateikti teksto laukus
  * Pristatymo dokumento turinys

### Patobulintos puslapio funkcijos grafinėms programoms ###
#### Dalomoji medžiaga Meistras ####

Dalomosios medžiagos pagrindinio elementas yra šablonas, skirtas automatiškai generuoti dalomosios medžiagos puslapius programoms, kurios palaiko tokių puslapių spausdinimą.
Atributai, kurie gali būti susieti su `<style:handout-master> ` elementai yra:

|Išdėstymas|Atributas|Aprašymas
---|---|---|
|Pristatymo puslapio išdėstymas|pristatymas:pristatymo puslapio išdėstymo pavadinimas|Nuorodos į `<style:presentation-page-layout> ` atributas
|Puslapio išdėstymas|`stilius:puslapio išdėstymo pavadinimas` | Nurodo puslapio išdėstymą, kuriame yra dalomosios medžiagos pagrindinio puslapio dydžiai, kraštinė ir orientacija.
|Page Style|`draw:style-name`|Priskiria papildomus formatavimo atributus dalomajam puslapiui, priskirdamas piešinio puslapio stilių.|
|Antraštės deklaracija| `pristatymas:naudoti-antraštės-pavadinimas`| Nurodomas antraštės lauko deklaracijos pavadinimas, kuris naudojamas visiems antraštės laukams, kurie rodomi padalomosios medžiagos pagrindiniame puslapyje.
|Poraštės deklaracija| prezentacija:use-footer-name|Nurodo poraštės lauko deklaracijos pavadinimą, kuris naudojamas visiems poraštės laukams, kurie rodomi padalomosios medžiagos pagrindiniame puslapyje.
|Datos ir laiko deklaracija|use-date-time-name|Nurodo datos ir laiko lauko deklaracijos pavadinimą, kuris naudojamas visiems datos ir laiko laukams, kurie rodomi padalomosios medžiagos pagrindiniame puslapyje.

### Piešimo figūros ###
OpenDocument formatas palaiko kelias piešimo formas, kurias gali naudoti bet kokio tipo dokumentai.

|Forma|Susijusios savybės| elementai
---|---|---|
Stačiakampis – `<draw:rect> `|Pozicija, dydis, stilius, sluoksnis, Z indeksas, ID, antraštės ID, teksto inkaras, lentelės fonas, piešimo galinė padėtis, apvalūs kampai|Pavadinimas, ilgas aprašas, įvykių klausytojai, klijavimo taškai, tekstas
Linija `<draw:line> `|Stilius, sluoksnis, Z indeksas, ID, antraštės ID ir transformacija, teksto inkaras, lentelės fonas, piešimo galinė padėtis, pradžios taškas, pabaigos taškas|pavadinimas, ilgas aprašas, įvykių klausytojai, klijavimo taškai, tekstas
Poliline `<draw:polyline> `| Pozicija, dydis, rodinio laukelis, stilius, sluoksnis, Z indeksas, ID, antraštės ID ir transformacija, teksto inkaras, lentelės fonas, piešimo galinė padėtis, taškai| Pavadinimas, ilgas aprašymas, įvykių klausytojai, klijavimo taškai, tekstas
Daugiakampis `<draw:polygon> `|Pozicija, dydis, peržiūros laukelis, stilius, sluoksnis, Z indeksas, ID, antraštės ID ir transformacija, teksto inkaras, lentelės fonas, piešimo galinė padėtis, taškai | pavadinimas, ilgas aprašas, įvykių klausytojai, klijavimo taškai, tekstas
|Taisyklingas daugiakampis `<draw:regular-polygon> `|Pozicija, dydis, stilius, sluoksnis, Z indeksas, ID, antraštės ID ir transformacija, teksto inkaras, lentelės fonas, piešimo galinė padėtis, įgaubta, kampai, ryškumas | pavadinimas, ilgas aprašymas, įvykių klausytojai, klijavimo taškai, tekstas
|Paht `<draw:path> `|Pozicija, dydis, rodinio laukelis, stilius, sluoksnis, Z indeksas, ID, antraštės ID ir transformacija, teksto prieraišas, lentelės fonas, piešimo galinė padėtis, kelio duomenys| Pavadinimas, ilgas aprašymas, įvykių klausytojai, klijavimo taškai, tekstas

### Rėmeliai ###
Piešimo dokumento rėmelis yra stačiakampis konteineris, kuriame yra teksto laukeliai, vaizdai ar objektai. Rėmeliai palaiko papildomas funkcijas, tokias kaip kontūrai, vaizdų žemėlapiai ir hipersaitai. Rėmelyje gali būti objektas ir vaizdas, todėl objektą galima pateikti kelis kartus. Programos pateikia atitinkamą elementą pagal geriausią palaikymą.

Rėmeliuose gali būti:
  * Teksto laukeliai
  * Objektai, pateikti arba OpenDocument formatu, arba konkrečiam objektui skirtu dvejetainiu formatu
  * Vaizdai
  * Programėlės
  * Papildiniai
  * Plaukiojantys rėmeliai

Dokumente yra rėmelis, kaip parodyta toliau.

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

## Nuorodos Nr.
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)

* [OpenDocument formatas – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


