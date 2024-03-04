{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Dokumento formatas",
"Atviras",
"Skaityti",
"Sukurti",
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

## Kas yra DWF failas?

Dizaino žiniatinklio formatas (DWF) reiškia 2D/3D piešinį suspaustu formatu, skirtą dizaino failams peržiūrėti, peržiūrėti ar spausdinti. Jame yra grafika ir tekstas kaip dizaino duomenų dalis ir sumažina failo dydį dėl suglaudinto formato. Sumažintas failo dydis leidžia efektyviai platinti ir perduoti turtingus dizaino duomenis. DWF nereikalauja, kad gavėjas žinotų apie CAD programinės įrangos, sukūrusios originalų brėžinį, naudojimą. DWF failo formato turinys gali būti paprastas ir apimti tik vieną lapą arba pakankamai sudėtingas, kad būtų šriftų, spalvų ir vaizdų.

## Trumpa istorija ##

Autodesk pristatė DWF failo formatą 1995 m. kaip Netscape Navigation papildinio WHIP dalį. Formatas išsivystė iš tik 2D formato, kad įtrauktų 3D turinį su laiku. Daugelis trečiųjų šalių programų taip pat naudoja šį formatą.

## DWF failo formatas ##

DWF yra atviras, saugus formatas, specialiai sukurtas dalytis turtingais inžinerinio projektavimo duomenimis. Tai nepriklauso nuo originalios taikomosios programinės įrangos, aparatinės įrangos ir operacinės sistemos, naudojamos tiems dizaino duomenims sukurti. Tai leidžia komandos nariams, kurie nenaudoja CAD taikomųjų programų, dalyvauti skaitmeniniuose procesuose peržiūrint pastatų, GIS ar gaminių projektus. DWF failų archyvą sudaro keli XML ir dvejetainiai failai, kurie kartu supakuoti į suglaudintą archyvą, sukurtą naudojant [ZIP](/compression/zip/) glaudinimą. Galite pervardyti DWF failo plėtinį į ZIP ir peržiūrėti failo turinį. DWF pakete gali būti įvairių dizaino duomenų, tokių kaip 2D grafika, 3D grafika, paketų ir skyrių metaduomenys ir kiti išteklių failai.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Išteklių failai** – medijos ar kiti turinio failai, į kuriuos pateikiamos nuorodos iš paketo/skilties metaduomenų ir paprastai pateikiami įvairių formatų dizaino duomenys (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/) ir kt.)

### Išsami failo formato informacija ###

DWF failai yra suskirstyti į tris pagrindines dalis, kaip parodyta toliau.

* Failo identifikavimo antraštė

* Failų duomenų blokas

* Failo užbaigimo priekaba


#### Failo identifikatoriaus antraštė ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|Baitas|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Simbolis|(|D|W|F|(tarpas)|V|0|0|.|3|0|)

Štai šios lentelės santrauka:

* Pirmieji šeši antraštės baitai visada reiškia ASCII simbolius "(DWF V"

* Šiuose 5 baituose yra informacija apie versijos numerį, pvz., "00.30" su pagrindine ir šalutine formato versijos reikšmėmis


Programos, kuriančios DWF failą, turėtų nurodyti mažiausią įmanomą versijos numerį, kurį skaitytuvo programa turi palaikyti, kad galėtų tinkamai naudoti duomenis.

#### Failo duomenų blokas ####

Failo duomenų blokas prasideda nuo 13-ojo DWF failo baito ir yra operacinės kodo ir operandų porų serija, kaip nurodyta toliau pateiktoje lentelėje.

|1 laukas|2 laukas|3 laukas|4 laukas|5 laukas|5 laukas
--- | --- |--- | --- |--- | --- |
|opkodas|operandas|operandas|operandas|operandas|operandas

DWF faile gali būti opcode-operandų porų kaip skaitomų ASCII, taip pat dvejetainį kodą arba jų abiejų derinį. Visos DWF operacijos turi skaitomą ASCII opcode / operando formą, o dauguma operacijų taip pat turi užkoduotą dvejetainį opcode / operandą. Opkodai yra vieno baito, leidžiantys atlikti daugiau nei 200 operacijų. Išplėstinis ASCII ir išplėstinis dvejetainis yra išskirtiniai atvejai. Opcodes reikšmės gali svyruoti nuo 0 iki 255 su kai kuriomis išimtimis. Išskyrus du specialius išplėstinio ASCII ir išplėstinio dvejetainio opkodų tipus, failų skaitytuvas turi žinoti, kaip apskaičiuoti operando ilgį.

##### Draudžiami opkodai #####

Toliau nurodytų ASCII atvaizdų negalima naudoti kaip operacijų kodų:

Šie ASCII atvaizdai negali būti naudojami kaip opkodai:

* Tarpas (0x20)

* Skirtukas (0x09)

* Brūkšnelis (0x2D)

* ASCII skaitmenys nuo 0 iki 9 (0x30 - 0x39)

* Vežimas atgal (0x0D)

* Linijos padavimas (0x0A)

* Viena kabutė (0x27)

* Dvigubos kabutės (0x22)

* Laikotarpis (0x2E)

* Skliausteliuose (0x28 ir 0x29)

* Garbanoti skliaustai (0x7B ir 0x7D)

* Kvadratiniai skliaustai (0x5B ir 0x5D)

* Atgalinis pasvirasis brūkšnys (0x5C)


#### Failo nutraukimo anonsas ####

DWF failo užbaigimo anonsas yra tiesiog specialus opkodas, nurodantis failo pabaigą. Kai kurios programos gali saugoti ne DWF duomenis po užbaigimo operacijos kodo. Anonsas yra toks, kaip parodyta toliau:


|Baitas|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Simbolis|(|E|n|d|0|f|D|W|F|)

## Nuorodos Nr.

* [DWF – Vikipedija](https://en.wikipedia.org/wiki/Design_Web_Format)

* [WHIP duomenų formatas](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs /opc/adventures-in-packaging-episode-1)


