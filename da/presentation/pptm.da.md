{
  "date": "2019-10-11",
  "keywords": [
"pptm fil",
"pptm filformat",
"hvad er en pptm-fil",
"fil",
"pptm eksempel",
"pptm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPTM - Makroaktiveret PowerPoint-præsentationsfilformat",
  "description": "Lær om PPTM-filformat og API'er, der kan oprette og åbne PPTM-filer.",
  "linktitle": "PPTM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ppt-dam"
}
},
  "lastmod": "2019-09-10"
}

Filer med PPTM-udvidelse er makroaktiverede præsentationsfiler, der er oprettet med Microsoft PowerPoint 2007 eller nyere versioner. De ligner [PPTX](/presentation/pptx/) filer med den forskel, at lateralen ikke kan udføre makroer, selvom de kan indeholde makroer. PPTM-filer kan redigeres ved at åbne dem i Microsoft PowerPoint og opdatere indholdet. Et andet lignende format er PPSM, men det er skrivebeskyttet som standard og starter diasshowet, når det åbnes. PPTM indeholder ligesom PPTX slides til forskellige præsentationselementer som tekst, billeder, videoer, grafer og andet relateret materiale.

## Kort historie ##

PPTM file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Den nye filtype har tilføjet fordele ved små filstørrelser, færre ændringer af korruption og velformaterede billeder. Det var i begyndelsen af 2000, da Microsoft besluttede at gå efter ændringen for at imødekomme standarden for **Office Open XML**. I 2007 blev dette nye filformat en del af Office 2007 og videreføres også i de nye versioner af Microsoft Office.

## Filformatspecifikationer ##

Filer genereret med office Open XML-filformat er en samling af XML-filer sammen med andre filer, der giver links mellem alle de indgående filer. Denne samling er faktisk et komprimeret arkiv, der kan udtrækkes for at se dets indhold. For at gøre det skal du blot omdøbe PPTM-filtypen med zip og udpakke den for at observere dens indhold.

De følgende afsnit kaster lidt lys over hver enkelt af disse.

### [Content_Types].xml ###

Dette er den eneste fil, der findes på basisniveauet, når zip-filen udpakkes. Den viser indholdstyperne for dele i pakken. Alle referencer til XML-filerne inkluderet i pakken er refereret i denne XML-fil. Følgende er en indholdstype for en diasdel:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Hvis der skal tilføjes nye dele til pakken, kan det gøres ved at tilføje den nye del og opdatere eventuelle relationer i .rels-filerne. Det skal huskes, at for en sådan ændring skal Content_Types.xml også opdateres.

### \_rels (mappe) ###

Relationer mellem de andre dele og ressourcer uden for pakken vedligeholdes af relationsdelen. Mappen Relationer indeholder en enkelt XML-fil, der gemmer relationerne på pakkeniveau. Links til de vigtigste dele af præsentationsfilerne er indeholdt i denne fil som URI'er. Disse URI'er identificerer typen af relation mellem hver nøgledel til pakken. Dette inkluderer forholdet til primært kontordokument placeret som ppt/presentation.xml og andre dele i docProps som kerneegenskaber og udvidede egenskaber.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Hver del af dokumentet, der er kilden til en eller flere relationer, vil have sin egen relationsdel, hvor hver sådan relationsdel findes i en \_rels-undermappe af delen og er navngivet ved at tilføje '.rels' til navnet på delen en del. Hovedindholdsdelen (presentation.xml) har sin egen relationsdel (presentation.xml.rels). Den indeholder relationer til andre andre dele af indholdet såsom slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, samt URI'erne til eksterne links.

#### Eksplicit forhold ####

For en eksplicit relation henvises der til en ressource ved hjælp af Id-attributten for en<Relationship> element. Det vil sige, at id'et i kilden er knyttet direkte til et id for et relationselement med en eksplicit reference til målet.

For eksempel kan et dias indeholde et hyperlink som dette:
```
<a:hlinkClick r:id#"rId2">
```
r:id#rId2 refererer til følgende relation inden for relationsdelen for diaset (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implicit forhold ####

For et implicit forhold er der ingen sådan direkte henvisning til en `<Relationship> Id`. I stedet forstås referencen.

### ppt-mappe ###

Dette er hovedmappen, der indeholder alle detaljer om indholdet af præsentationen. Som standard har den følgende mapper:

* \_rels

* tema

* dias

* slideLayouts

* slideMasters


og følgende xml-filer:

* præsentation.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## Referencer ##

* [[MS-PPTX] - PPTX-filformat](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


