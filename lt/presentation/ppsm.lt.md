{
  "date": "2019-10-11",
  "keywords": [
"ppsm failą",
"ppsm failo formatas",
"kas yra ppsm failas",
"failą",
"ppsm pavyzdys",
"ppsm failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPSM – „PowerPoint“ pristatymo failas su makrokomandomis",
  "description": "Sužinokite apie PPSM failo formatą ir API, kurios gali kurti ir atidaryti PPSM failus.",
  "linktitle": "PPSM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pps-ltm"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PPSM failas?

Failai su PPSM plėtiniu atspindi makrokomandą įgalintą skaidrių demonstravimo failo formatą, sukurtą naudojant Microsoft PowerPoint 2007 ar naujesnę versiją. Kitas panašus failo formatas yra [PPTM](/presentation/pptm/), kuris skiriasi tuo, kad atidaromas naudojant Microsoft PowerPoint redaguojamu formatu, o ne kaip skaidrių demonstravimas. Kai paleidžiama kaip skaidrių demonstracija, PPSM faile rodomos pristatymo skaidrės su nepažeistu turiniu ir pagal numatytuosius nustatymus veikia tik skaitymo režimas. PPSM failus vis tiek galima redaguoti Microsoft PowerPoint atidarius juos PowerPoint.

## Dokumento formatas ##

PPSM failo formatas buvo pristatytas kartu su PowerPoint 2007 ir yra pagrįstas OpenXML failo formatu, kurio turiniui saugoti naudojamas XML ir [ZIP](/compression/zip/) derinys. Failai, sukurti naudojant Office Open XML failo formatą, yra XML failų rinkinys kartu su kitais failais, kuriuose pateikiamos nuorodos tarp visų sudedamųjų failų. Ši kolekcija iš tikrųjų yra suspaustas archyvas, kurį galima išgauti norint peržiūrėti jo turinį. Norėdami tai padaryti, tiesiog pervardykite PPSM failo plėtinį su zip ir ištraukite jį, kad galėtumėte stebėti jo turinį.

Tolesni skyriai šiek tiek paaiškina kiekvieną iš jų.

### [Content_Types].xml ###

Tai vienintelis failas, kuris randamas pagrindiniame lygyje, kai ištraukiamas ZIP failas. Jame pateikiami paketo dalių turinio tipai. Visos nuorodos į pakete esančius XML failus yra pateiktos šiame XML faile. Toliau pateikiamas skaidrės dalies turinio tipas:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jei prie paketo reikia pridėti naujų dalių, tai galima padaryti pridedant naują dalį ir atnaujinant bet kokius ryšius .rels failuose. Reikia turėti omenyje, kad norint atlikti tokį pakeitimą, taip pat turi būti atnaujintas Content_Types.xml.

### \_rels (aplankas) ###

Ryšius tarp kitų dalių ir išteklių už paketo ribų palaiko ryšių dalis. Aplanke Ryšiai yra vienas XML failas, kuriame saugomi paketo lygio ryšiai. Nuorodos į pagrindines pristatymo failų dalis yra šiame faile kaip URI. Šie URI nustato kiekvienos pagrindinės dalies ryšio su paketu tipą. Tai apima ryšį su pagrindiniu biuro dokumentu, esančiu kaip ppt/presentation.xml, ir kitas docProps dalis kaip pagrindines ir išplėstines ypatybes.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Kiekviena dokumento dalis, kuri yra vieno ar kelių ryšių šaltinis, turės savo santykių dalį, kur kiekviena tokia santykių dalis yra \_rels dalies poaplanke ir yra pavadinta pridedant .rels prie failo pavadinimo. dalis. Pagrindinė turinio dalis (presentation.xml) turi savo santykių dalį (presentation.xml.rels). Jame yra ryšių su kitomis turinio dalimis, pvz., slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, taip pat išorinių nuorodų URI.

#### Aiškūs santykiai ####

Aiškiam ryšiui išteklius nurodomas naudojant a atributą Id<Relationship> elementas. Tai reiškia, kad šaltinio ID tiesiogiai susiejamas su ryšio elemento ID su aiškia nuoroda į tikslą.

Pavyzdžiui, skaidrėje gali būti toks hipersaitas:
```
<a:hlinkClick r:id#"rId2">
```
R:id#rId2 nurodo šiuos santykius skaidrės santykių dalyje (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Netiesioginis ryšys ####

Numanomiems santykiams tokios tiesioginės nuorodos į  nėra<Relationship> Id`. Vietoj to nuoroda suprantama.

### ppt aplankas ###

Tai pagrindinis aplankas, kuriame yra visa informacija apie pristatymo turinį. Pagal numatytuosius nustatymus jame yra šie aplankai:

* \_rels

*tema

* skaidrės

* skaidrių išdėstymai

* slideMasters


ir šiuos xml failus:

* pristatymas.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## Nuorodos Nr.

* [OpenXML pristatymo failo formatas](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


