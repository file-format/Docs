{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Filformat", "CAD", "Öppna", "Skapa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DWG-filformat och API:er som kan skapa och öppna DWG-filer.",
  "title" :"DWG-filformat",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DWG fil?

Filer med DWG-tillägg representerar proprietära binära filer som används för att innehålla 2D- och 3D-designdata. Liksom DXF, som är ASCII-filer, representerar DWG det binära filformatet för CAD-ritningar (Computer Aided Design). Den innehåller vektorbilder och metadata för representation av innehållet i CAD-filer. Det finns gratis visningsprogram tillgängliga för att visa DWG-filer på Windows operativsystem, som Autodesks gratis DWG TrueView. Det finns också andra tredjepartsprogram som stöder att nå DWG-filer. DWG-filer innehåller användarskapad information och inkluderar:

* Designar
* Geometriska data
* Kartor och foton

Detta format används ofta av arkitekter, ingenjörer och designers för olika designsyften.

## Kortfattad bakgrund ##

DWG-filformatet har utvecklats med tiden sedan dess formella introduktion 1982. En kort översikt över tidigare händelser ur ett historiskt perspektiv är följande.

**1982:** Autodesk licensierade DWG-filformatet , som utvecklades av Mike Riddle 1970, som grund för AutoCAD.

**1998:** Med lanseringen av AutoCAD R14.01 lade Autodesk till filverifiering genom en funktion som heter DWGCHECK som bäddade in en krypterad kontrollsumma och produktkod, kallad WaterMark av Autodesk, i DWG-filer skapade av programmet.

**2006:** Autodesk modifierade AutoCAD 2007 för att inkludera "TrustedDWG technology" för att bädda in textsträngen "Autodesk DWG. Den här filen är en Trusted DWG som senast sparades av en Autodesk-applikation eller Autodesk-licensierad applikation" i DWG-filerna. Syftet med detta var att hjälpa Autodesks mjukvaruanvändare att säkerställa att dessa filer skapades av en Autodesk- eller RealDWG-applikation, vilket definitivt borde bidra till att minska risken för inkompatibiliteter.

## Filstruktur ##

DWG har varit ett av de mycket använda filformaten av en rad applikationer och har en robust filstruktur. Eftersom DWG är ett binärt filformat är det inte läsbart för människor som det vanliga ASCII [DXF](/sv/cad/dxf/) filformatet. DWG-filer innehåller vanligtvis information om bildkoordinaterna och eventuella metadata som är associerade med dem. Fullständiga [specifikationer](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) av DWG-filformat finns tillgängliga för nedladdning av OpenDesign. Filstrukturen för DWG-filformatet sammanfattas enligt följande.

**Header**: Filhuvudet består av DWG Header-variabler och information om Cyclic Redundancy Check (CRC) som används för feldetektering. Varje undersektion är en specialiserad vektor där olika bitlängder används för att representera olika etiketter. Till exempel står de första 6 bitarna av variabeln DWG Header för versionssträngen.

**Klassdefinitioner:** En DWG-fil kan innehålla flera klasser beroende på det specifika .dwg-filens syfte. Information såsom klassmetadatastorlek på klassdataområde, klassnummer och kontrollsumma förutom andra.

**Mall**: Detta är valfritt och för R15- och R15-versioner är det här avsnittet under avsnittet Objekt Ledigt utrymme.

**Utfyllning**: Metadata suffixas och efterfixas med ett specifikt antal byte, vilket gör att de äldre AutoCAD-programvaruversionerna är vidarekompatibla med det nya DWG-filformatet.

**Bilddata**: Metadata för detta avsnitt beror på den specifika .dwg-typen. För R14- och R15-användare är detta avsnitt valfritt.

**Objektdata**: Objektdatan består av en komplett lista med tabellenheter, ordboksposter etc. som motsvarar den befintliga listan med objekt.

**Objektkarta**: Platsen för varje objekt i filen anges i den här delen av filen. De flesta metadata i det här avsnittet är filhandtag som spelar en roll vid identifiering och omrendering av objektet.

**Fritt utrymme för objekt**: Det här avsnittet är valfritt för alla användare

**Andra rubrik**: En dubblett av filhuvudet mot slutet av DWG-filen

## Referenser ##

* [DWG-filformatsspecifikationer](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [DWG-filspecifikationen](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - av Wikipedia](https://en.wikipedia.org/wiki/.dwg)

