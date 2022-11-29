{
  "date" : "2019-10-11",
  "keywords" :[ "dicom-fil", "dicom-filformat", "vad är en dicom-fil", "fil", "dicom-exempel", "dicom-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Digital Imaging and Communications File Format",
  "description":"Läs mer om DICOM-filformat och API:er som kan skapa och öppna DICOM-filer.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DICOM fil?

DICOM är akronymen för Digital Imaging and Communications in Medicine och hänför sig till området medicinsk informatik. DICOM används för integrering av medicinska bildbehandlingsenheter som skrivare, servrar, skannrar etc från olika leverantörer och innehåller även identifieringsdata för varje patient för att vara unik. DICOM-filer kan delas mellan två parter om de kan ta emot bilddata i DICOM-format. Kommunikationsdelen av DICOM är applikationslagerprotokoll och använder TCP/IP för att kommunicera mellan enheter. Versioner som stöds av webbtjänster är 1.0, 1.1, 2 eller senare.

## Historik ##

DICOM utvecklades gemensamt av American College of Radiology (ACR) och National Electrical Manufacturers Association (NEMA) för utbyte och visning av medicinska bilder som MRI, datortomografi och ultraljudsbilder. Till en början var det svårt att avkoda bilderna som maskinerna producerade. Därför bildade ACR och NEMA tillsammans ett team 1983 som släppte sin första standard, ACR/NEMA 300 1985. Den andra versionen släpptes 1988 som var mer populär bland leverantörer, men snart insåg man att den andra versionen också behöver förbättras. Den tredje versionen av standarden släpptes 1993 som "DICOM". 3.0 är fortfarande den senaste versionen men den har uppdaterats kontinuerligt sedan 1993.

## DICOM-filformat ##

DICOM är kombinationen av filformatsdefinition och ett nätverkskommunikationsprotokoll. DICOM använder tillägget .DCM. .DCM finns i två olika format, dvs format 1.x och format 2.x. DCM Format 1.x finns dessutom i två versioner normal och utökad. HTTP- och HTTPS-protokollen används för DICOMs webbtjänster.

### Filhuvud ###

Filhuvudet innehåller 128 byte File Preamble och 4 byte DICOM-prefix.

**Ingress # 128 byte**|**Prefix # 4 byte “D, I, C, M**

**Ingress** används för att komma åt bilderna och andra data i DICOM-filen, vilket ger kompatibilitet med vanliga bildfilformat.

**Prefix** innehåller strängen "DICM" som versaler.

### Datauppsättning ###

Varje fil måste innehålla en enda datamängd som representerar SOP-instans och SOP-klass med tillhörande IOD. Datauppsättning är representationen av information från den verkliga världen. Datauppsättning innehåller dataelement och dataelement innehåller värden för objektets attribut. Attributens struktur specificeras i IODs. Ett DICOM-dataobjekt består av ett antal attribut, inklusive poster som namn, ID, etc., och även ett speciellt attribut som innehåller bildpixeldata.

### Dataelement ###

Dataelement består av dataelement Tag, Value length och värde för dataelementet. Det finns 5 typer av dataelement, nämligen typ 1 obligatoriska dataelement, typ 1C villkorliga dataelement, typ 2 obligatoriska dataelement, typ 2C villkorliga dataelement och typ 3 valfria dataelement. Grundläggande Tre typer av dataelementstrukturer är följande.

**Dataelement med en explicit VR**

|Gruppnummer|Elementnummer|Värdepresentation|Reserverad|Värdelängd|Värdefält
---|---|---|---|---|---|
|2 byte|2 byte|2 byte|2 byte # 0x00, 0x00|4 byte|"Värdelängd byte"

**Dataelement med en explicit VR**

|Gruppnummer|Elementnummer|Värdepresentation|Värdelängd|Värdefält
---|---|---|---|---|
|2 Byte|2 Byte|2 Byte|2 Byte|"Value Length Bytes"

**Dataelement med en implicit VR**


|Gruppnummer|Elementnummer|Värdelängd|Värdefält
---|---|---|---|
|2 Byte|2 Byte|4 Byte|"Värdelängd Byte"

1. **Dataelementtagg**: Ett ordnat heltal som representerar gruppnumret och elementnumret
1. **Värdepresentation VR**: VR är en teckensträng som representerar VR för dataelementet.
1. **Värdelängd**: är det heltal utan tecken som representerar värdefältets explicita längd.
1. **Värdefält**: Beskriver värdena för dataelementen.

## Överför syntax ##

Överföringssyntax är en uppsättning regler för kodning för att entydigt representera mer abstrakta syntaxer. Med hjälp av överföringssyntax förhandlar kommunicerande enheter om vanliga kodningstekniker som de stöder.

## SOP ##

Union of IOD and DIMSE definierar en SOP-klass. SOP-klassdefinitionen innehåller regler och semantik som kan begränsa användningen av tjänsterna i DIMSE-tjänstgruppen eller IOD:s attribut. Exempel på Service Elements är Store, Get, Find, Move etc. Exempel på Objekt är CT-bilder, MR-bilder men inkluderar även schemalistor, utskriftsköer m.m.

## Tjänster ##

DICOM tillhandahåller olika tjänster, mestadels relaterade till kommunikation av data. Var och en beskrivs kortfattat nedan:


**Store:** DICOM Store-tjänsten skickar bilder eller andra objekt till ett bildarkiverings- och kommunikationssystem (PACS) eller server.


**Lagringsåtagande:** Lagringsförbindelsetjänst används för att bekräfta att en bild har lagrats permanent på enheten på någon typ av media.


**Fråga/hämta:** Denna tjänst gör det möjligt för en arbetsstation att hitta listor med bilder eller andra objekt och sedan hämta dem från PACS.


**Modalitetsarbetslista:** Modalitetsarbetslisttjänsten ger en lista över bildbehandlingsprocedurer som har schemalagts för prestanda av en bildinsamlingsenhet.


**Skriv ut:** Den här tjänsten skickar bilder till skrivaren.

## Portnummer över IP ##

DICOM använder följande TCP- och UDP-portar:

1. 104
1. 2761
1. 2762
1. 11112

## Referenser ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

