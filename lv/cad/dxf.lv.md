{
  "date": "2020-03-16",
  "keywords": [
"DXF fails",
"Faila formāts",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DXF failu formātu un API, kas var izveidot un atvērt DXF failus.",
  "title": "DXF faila formāts",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DXF fails?

DXF, Drawing Interchange Format vai Drawing Exchange Format, ir AutoCAD rasējuma faila ar marķētu datu attēlojums. Katram faila elementam ir prefikss vesels skaitlis, ko sauc par grupas kodu. Šis grupas kods faktiski apzīmē elementu, kas seko, un norāda datu elementa nozīmi konkrētam objekta tipam. DXF ļauj attēlot gandrīz visu lietotāja norādīto informāciju zīmējuma failā.

DXF faila formātu Autodesk izstrādāja kā CAD datu faila formātu datu savietojamībai starp AutoCAD un citām lietojumprogrammām. Tādējādi datus var importēt no citiem formātiem uz DXF uz AutoCAD saskaņā ar DXF failu formātu savietojamības specifikācijām.

## Īsa vēsture ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. AutoCAD sākotnējās versijas atbalsta tikai DXF ASCII faila formātu. Līdz ar AutoCAD 10. izlaidumu (un jaunāku versiju) 1988. gadā programmā AutoCAD tika ieviests gan ASCII, gan binārā DXF faila formāta atbalsts. Iepriekšējos posmos Autodesk nekopīgoja nekādas faila formāta specifikācijas, un tāpēc pareiza DXF failu importēšana nebija vienkārša. Tomēr Autodesk tagad publicē DXF specifikācijas un ir pieejamas plašai sabiedrībai.

## Faila formāta specifikācijas ##

DXF faila formāts izmanto grupas kodu un vērtību pārus, lai sakārtotu saturu sadaļās. Katra sadaļa sastāv no ierakstiem, kur katrs ieraksts sastāv no grupas koda un datu vienības. Katrs grupas kods un vērtība atrodas savā DXF faila rindā. Katra sadaļa sākas ar grupas kodu 0, kam seko virkne SECTION. Tam seko grupas kods 2 un virkne, kas norāda sadaļas nosaukumu (piemēram, SECTION1). Katra sadaļa sastāv no grupu kodiem un vērtībām, kas nosaka tās elementus. Sadaļa beidzas ar 0, kam seko virkne ENDSEC.

DXF faila formāts ņem vērā objektus, kas atšķiras no entītijām. Objektiem šeit nav grafiskā attēlojuma, bet entītijām tas ir. Tādējādi DXF ieraksti tiek saukti par grafiskiem objektiem, savukārt objektu objekti tiek saukti par negrafiskiem objektiem. DXF faila sadaļās BLOCK un ENTITIES ir ietvertas entītijas, un grupu kodu izmantošana šajās divās sadaļās ir identiska. Entītijas beigas norāda nākamā 0 grupa, kas sāk nākamo entītiju vai norāda sadaļas beigas.

### Faila struktūra ###

Sadaļas DXF failā ir sakārtotas šādā secībā:

|Section|Basic description
---|---|
|Header|Šajā sadaļā ir ietverta vispārīga informācija par zīmējumu. Tas ir kā jūsu tālruņa funkcionalitāte Iestatījumi, kurā ir dažādi mainīgie, kas saistīti ar zīmējumu un ar to saistītās vērtības. Piemēram, sadaļā Header tiks noteikts, kuru AutoCAD versiju izmanto DXF fails (mainīgais $ACADVER) vai vienību, ko izmanto leņķu mērīšanai failā (mainīgais $AUNITS).
|Classes|Sadaļā KLASES ir informācija par lietojumprogrammu definētām klasēm, kuru gadījumi tiek rādīti datu bāzes sadaļās BLOCKS, ENTITIES un OBJECTS.
|Tabulas|Šajā sadaļā ir definīcijas vairākām dažādām tabulām, no kurām katra satur dažādus simbolu ierakstus. Piemēram, tabula [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) nosaka domuzīmju, punktu, teksta un simbolu modeli DXF failā un to mērogošanu. Šeit ir pilns šajā sadaļā atrodamo tabulu saraksts:<ul><li> Lietojumprogrammas ID (APPID) tabula</li><li> Bloku ierakstu (BLOCK_RECORD) tabula</li><li> Dimension Style (DIMSTYPE) tabula</li><li> Slāņu (LAYER) tabula</li><li> Līnijas tipa (LTYPE) tabula</li><li> Teksta stila (STYLE) tabula</li><li> Lietotāja koordinātu sistēmas (UCS) tabula</li><li> Skatīt (SKATĪT) tabulu</li><li> Viewport konfigurācijas (VPORT) tabula</li></ul>
|Bloki|Šajā sadaļā ir ietverti grafiskie objekti un zīmēšanas entītijas, kas veido katra bloka atsauci zīmējumā.
|Entities|Šī sadaļa satur faktiskos objekta datus un zīmējuma grafiskās entītijas. Tas var ietvert neapstrādātus datus, piemēram, apļa entītiju nosaka tā biezums, centra punkts, rādiuss un ekstrūzijas virziens.
|Objekti|Šeit jūs atradīsiet zīmējuma negrafiskās daļas. Piemēram, šeit tiek glabātas AutoCAD vārdnīcas.

## Atsauces Nr.

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF by Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)


