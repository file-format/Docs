{
  "date": "2020-03-16",
  "keywords": [
"DXF failas",
"Dokumento formatas",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DXF failo formatą ir API, kurios gali kurti ir atidaryti DXF failus.",
  "title": "DXF failo formatas",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DXF failas?

DXF, Drawing Interchange Format arba Drawing Exchange Format, yra pažymėtas AutoCAD piešinio failo duomenų atvaizdas. Kiekvienas failo elementas turi sveikojo skaičiaus priešdėlį, vadinamą grupės kodu. Šis grupės kodas iš tikrųjų reiškia elementą, kuris seka ir nurodo duomenų elemento reikšmę tam tikram objekto tipui. DXF leidžia brėžinio faile pateikti beveik visą vartotojo nurodytą informaciją.

DXF failo formatą Autodesk sukūrė kaip CAD duomenų failo formatą, skirtą duomenų sąveikai tarp AutoCAD ir kitų programų. Taigi duomenis galima importuoti iš kitų formatų į DXF į AutoCAD pagal DXF failų formato sąveikos specifikacijas.

## Trumpa istorija ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. Pradinės AutoCAD versijos palaiko tik DXF ASCII failo formatą. 1988 m. išleidus 10 AutoCAD (ir naujesnę versiją), AutoCAD buvo pristatytas ASCII ir dvejetainio DXF failo formato palaikymas. Ankstesniuose etapuose Autodesk nesidalino jokiomis failo formato specifikacijomis, todėl teisingai importuoti DXF failus nebuvo lengva. Tačiau Autodesk dabar skelbia DXF specifikacijas ir prieinamas plačiajai visuomenei.

## Failo formato specifikacijos ##

DXF failo formatas naudoja grupės kodo ir reikšmių poras, kad suskirstytų turinį į skyrius. Kiekviena sekcija susideda iš įrašų, kur kiekvieną įrašą sudaro grupės kodas ir duomenų elementas. Kiekvienos grupės kodas ir reikšmė yra atskiroje DXF failo eilutėje. Kiekviena sekcija prasideda grupės kodu 0, po kurio seka eilutė SECTION. Po to yra grupės kodas 2 ir eilutė, nurodanti skyriaus pavadinimą (pavyzdžiui, SECTION1). Kiekviena sekcija sudaryta iš grupės kodų ir reikšmių, apibrėžiančių jos elementus. Skyrius baigiasi 0, po kurio seka eilutė ENDSEC.

DXF failo formatu objektai skiriasi nuo objektų. Objektai čia neturi grafinio atvaizdo, bet subjektai jį turi. Taigi DXF įrašai vadinami grafiniais objektais, o objektų objektai – negrafiniais objektais. DXF failo skyriuose BLOCK ir ENTITIES yra objektai, o grupių kodų naudojimas šiose dviejose dalyse yra identiškas. Objekto pabaigą žymi kita 0 grupė, kuri pradeda kitą objektą arba nurodo skyriaus pabaigą.

### Failo struktūra ###

DXF failo skyriai yra išdėstyti tokia tvarka:

|Section|Basic description
---|---|
|Antraštė|Šiame skyriuje pateikiama bendra informacija apie piešinį. Tai panašu į telefono nustatymų funkciją, kurioje yra įvairūs su piešiniu susiję kintamieji ir su juo susijusios reikšmės. Pavyzdžiui, antraštės skiltyje bus nustatyta, kurią AutoCAD versiją naudoja DXF failas (kintamasis $ACADVER) arba vienetą, naudojamą kampams matuoti faile (kintamasis $AUNITS).
|Klasės|Skiltyje KLASĖS yra informacija apie programos apibrėžtas klases, kurių egzemplioriai rodomi duomenų bazės skyriuose BLOKAI, SUBJEKTAI ir OBJEKTAI.
|Lentelės|Šiame skyriuje pateikiami kelių skirtingų lentelių apibrėžimai, kurių kiekvienoje yra keletas skirtingų simbolių įrašų. Pavyzdžiui, lentelė [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) apibrėžia brūkšnelių, taškų, teksto ir simbolių šabloną DXF faile ir kaip jie keičiami. Čia yra visas šiame skyriuje esančių lentelių sąrašas:<ul><li> Programos ID (APPID) lentelė</li><li> Blokų įrašų (BLOCK_RECORD) lentelė</li><li> Matmenų stiliaus (DIMSTYPE) lentelė</li><li> Sluoksnio (SLUOKSNIO) lentelė</li><li> Linijų tipo (LTYPE) lentelė</li><li> Teksto stiliaus (STILIUS) lentelė</li><li> Vartotojo koordinačių sistemos (UCS) lentelė</li><li> Žiūrėti (ŽIŪRĖTI) lentelę</li><li> Viewport konfigūracijos (VPORT) lentelė</li></ul>
|Blocks|Šiame skyriuje yra grafiniai objektai ir piešimo objektai, kurie sudaro kiekvieną bloko nuorodą brėžinyje.
|Subjektai|Šiame skyriuje pateikiami faktiniai objekto duomenys ir brėžinio grafiniai objektai. Tai gali apimti neapdorotus duomenis – pavyzdžiui, apskritimo objektą apibrėžia jo storis, centrinis taškas, spindulys ir ekstruzijos kryptis.
|Objektai|Čia rasite negrafines piešinio dalis. Pavyzdžiui, čia saugomi AutoCAD žodynai.

## Nuorodos Nr.

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF by Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)


