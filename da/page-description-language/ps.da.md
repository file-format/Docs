{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PS filformat",
  "description": "Lær om PS-filformat og API'er, der kan oprette og åbne PS-filer.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en .PS-fil? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Kort historie ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Steve Jobs fra Apple besøgte dem og rådede dem til at tilpasse PostScript til at drive laserprintere.

I marts 1985 var den første printer med en indlejret PostScript-fortolker Apples LaserWriter, som revolutionerede desktop publishing (DTP). Den tekniske soliditet og udbredte tilgængelighed gjorde PostScript til et valgsprog til desktop og elektronisk udgivelse. I løbet af 1990 var en tolk til PostScript-sproget en væsentlig del af laserprinterne.

## Hovedtræk ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Former:** Vilkårlige af natur, kan bestå af lige linjer, kurver, firkanter og kubiske kurver, som kan være både selvgennemløbende og afbrudte (i sektioner og huller).

**Maleoperatorer:** tillader formkontur af enhver tykkelse, farve, fyld eller tillad, at formen tegnes som et udklip for at tillade beskæring af enhver anden grafik.

**Farver:** har forskellighed som gråtoner, RGB, CMYK og CIE. Særlige slags farver er modelleret som forskellige egenskaber: staffagefarver, farvekortlægning, jævn skygge og gentagne mønstre.

**Tekst:** fuldt integreret med grafik. Desuden tillader adobe billedbehandlingsmodel, at teksttegn vises som grafiske former, der kan betjenes af alle normale grafikoperatører.

**Samplede billeder**: Udtrukket fra originale kilder (scannede fotografier) eller kan være fremstillet syntetisk. PostScript-sproget tilbyder forskellige måder at regenerere billeder ved enhver opløsning og i overensstemmelse med forskellige farvemodeller på en outputenhed.

Et programmeringssprog til generelle formål kan drage fordel af grafiske muligheder PostScript-sprog ved at indlejre P'er i dets ramme. De primitive datatyper, såsom tal, tegn, arrays og strenge; kontrolprimitiver, såsom sløjfer, procedurer og betingelser; og nogle ukonventionelle funktioner, såsom ordbøger, er specificeret i sproget. Disse funktioner gør det lettere for programmører at skrive kommandoer for at påkalde operationer på højere niveau. Disse operationer på højt niveau opfylder behovene for komplekse applikationer. En sådan praksis er mere kompakt og effektiv i stedet for at bruge et fast sæt af grundlæggende operationer.

Programmer skrevet i PostScript kan produceres, kommunikeres og fortolkes i form af ASCII-kildetekst. Hele sproget kan defineres i form af printbare tegn og hvidt mellemrum. Denne repræsentation understøtter programmører til nemt at skabe, manipulere og forstå sproget. Desuden blev fillagring og -transmission mellem forskellige computere og operativsystemer bekvemt gennem maskinuafhængighed.

Binært kodede former for sproget er muligt, når programmet er garanteret en fuldstændig gennemsigtig kommunikationssti til PostScript-fortolkeren. Streng sammenhæng i ASCII-repræsentationen af PS-programmer anbefales fra Adobe til dokumentudveksling eller arkivlagring.

## Versioner ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Hver version definerer vigtige strukturerende kommentarer. Encapsulated PostScript File (EPS) er en speciel undertype af PostScript-fil, der anvender sproget til at angive en rektangulær grafik. PostScript Language Reference Manual beskriver en EPS som: En indkapslet PostScript-fil (EPS) er et PostScript-program, der højst beskriver en enkelt side i en form, der kan importeres af andre programmer til indlejring i et indeholdende dokument. En PostScript-dokumentfil kan indkapsle en EPS-fil i den. En ekstra brug af PostScript nævnes som Display PostScript (DPS). DPS genererer grafik på skærmen gennem en grafikmotor, der gør brug af PostScript-billeddannelsesmodel og sprog.

## Referencer ##

* [PostScript-formatfamilie](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


