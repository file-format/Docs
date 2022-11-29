{
  "date" : "2019-12-13",
  "keywords" :[ "ppt-fil", "ppt-filformat", "vad är en ppt-fil", "fil", "ppt-exempel", "ppt-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om PPT-filformat och API:er som kan skapa och öppna PPT-filer.",
  "title" :"PPT - PowerPoint-filformat",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PPT fil?

En fil med PPT-tillägg representerar en PowerPoint-fil som består av en samling bilder för visning som SlideShow. Den anger det binära filformatet som används av Microsoft PowerPoint 97-2003. En PPT-fil kan innehålla flera olika typer av information som text, punktpunkter, bilder, multimedia och andra inbäddade OLE-objekt. Microsoft kom med nyare filformat för PowerPoint, känt som [PPTX](/sv/presentation/pptx/), från 2007 och framåt som är baserat på Office OpenXML och skiljer sig från detta binära filformat. Flera andra applikationsprogram som OpenOffice Impress och Apple Keynote kan också skapa PPT-filer.

## Kortfattad bakgrund ##

Microsoft introducerade PPT-filformatet med lanseringen av PowerPoint 1987. Det stabila binära formatet delades som standard i PowerPoint 97-2003 för Windows. Det binära filformatet stöds för läsning och skrivning av de senaste versionerna av PowerPoint, inklusive PowerPoint 2016.

## Filformatspecifikationer ##

Sedan introduktionen har PPT-filformatet gått igenom flera revisioner för tillägg av nya funktioner och förbättringar. De senaste tillgängliga versionsspecifikationerna är version 6.0 som publicerades i augusti 2018, som inte bör blandas med det verkliga produktnumret för PPT-filformatet eftersom Microsoft inte längre tillhandahåller ändringar för detta format.

### Filformatöversikt ###

Några av nyckelkomponenterna i ett PPT-filformat är följande:

#### Slides ####

Användardata som former, text, animationer och media läggs till i en presentation i en bild. En presentation kan innehålla en eller flera bilder som visas som bildspel när en presentation körs. En presentation innehåller masterbilder och titelmasterbilder som fungerar som mallar för de vanliga visuella egenskaperna hos presentationsbilder. Det finns också en huvudbild för anteckningar och en huvudbild för åhörarkopior som tjänar ett liknande syfte och ger gemensamma visuella egenskaper för alla anteckningsbilder och alla utskrivna åhörarkopior.

#### Former ####

Former är objekt som tillåter användare att lägga till en mängd olika innehåll till en bild i form av platshållarformer, bilder och grafer. Former på en mallbild definierar vanliga data för grupper av former.

#### Platshållare Former ####

Dessa är speciella platshållare som fungerar som behållare för en mängd olika objekt. Olika platshållarformer kan användas för att ge ledtrådar för att infoga specifika typer av former som tabeller eller diagram. Inuti en bild anpassas en platshållarform till de visuella egenskaperna från en huvudbild, titelbild eller anteckningsbild.

#### Externa objekt ####

Externa objekt som inbäddat och länkat ljud, länkad video, inbäddade och länkade OLE-objekt och hyperlänkar kan bäddas in i en bild. Dessa objekt kan användas för att aktivera länkade objekt för åtkomst till externa resurser under ett bildspel.

### Filformatstrukturer ###

PowerPoint binära filformat består av följande strömmar för att representera den övergripande dokumentstrukturen och data.

* Aktuell användarström
* PowerPoint-dokumentström
* Bildström
* Sammanfattningsinformation och dokumentsammanfattningsinformation (valfritt)

De fullständiga specifikationerna för DOC-filformat finns som tillhandahålls av [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) och bör konsulteras med hänvisning till avsnitt som nämns i följande detaljer.

#### Aktuell användarström ####

Den håller register över den senaste användaren som öppnade dokumentet och dess namn måste vara "Current User".

#### PowerPoint-dokumentström ####

Håller register över all information om en PowerPoint-presentation och förklarar dess layout och innehåll. Det är en obligatorisk ström vars namn MÅSTE vara "PowerPoint-dokument". Innehållet i denna ström specificeras av en sekvens av toppnivåposter. Begränsningar för partiell ordning av postsekvensen anges i PersistDirectoryAtom- och UserEditAtom-posterna.

Som containerposter är DocumentContainer, MainMasterContainer (avsnitt 2.5.3), HandoutContainer (avsnitt 2.5.8), SlideContainer (avsnitt 2.5.1) och NotesContainer (avsnitt 2.5.6) var och en roten till ett träd av containerposter och atomrekord. Inuti alla behållarposter kan det finnas andra poster som inte är explicit listade som underordnade poster. Okända poster identifieras när recType-fältet i RecordHeader-strukturen (avsnitt 2.3.1) innehåller ett värde som inte anges av RecordType-uppräkningen (avsnitt 2.13.24). Dessa okända poster, om de påträffas, MÅSTE ignoreras och KAN<1> bevaras. Okända poster kan ignoreras genom att söka framåt recLen-bytes från slutet av RecordHeader-strukturen.

Varje gång den här strömmen skrivs kan nya toppnivåposter, en användarredigering, läggas till den befintliga strömmen, eller så kan hela ströminnehållet ersättas med en uppdaterad sekvens av toppnivåposter. Om hela strömmen inte ersätts, kan alla tidigare befintliga toppnivåposter som omfattade någon tidigare användarredigering göras föråldrade av de efterföljande bifogade toppnivåposterna som utgör den aktuella användarredigeringen.

#### Bilder Stream ####

Detta är en valfri ström som innehåller data om bilderna i en PowerPoint-presentation. Dess namn MÅSTE vara "Bilder". Innehållet i denna ström specificeras av OfficeArtBStoreDelay-posten enligt [MS-ODRAW] avsnitt 2.2.21.

#### Sammanfattningsinformationsström ####

Den håller statistik om dokumentet enligt Microsoft Office-standard. Namnet på sammanfattningsinformationsströmmen måste vara "\005SummaryInformation", där \005 är tecknet med värdet 0x0005, inte den bokstavliga strängen "\005". Denna ström SKA utelämnas för krypterade dokument. Innehållet i denna ström specificeras i [MS-OSHARED] avsnitt 2.3.3.2.1.

#### Informationsström för dokumentsammanfattning ####

En valfri ström vars namn MÅSTE vara "\005DocumentSummaryInformation", där \005 är tecknet med värdet 0x0005, inte den bokstavliga strängen "\005". Denna ström KAN <2> utelämnas för krypterade dokument. Innehållet i denna ström specificeras i [MS-OSHARED] avsnitt 2.3.3.2.2.

#### Krypterad sammanfattningsinformationsström ####

En valfri ström vars namn MÅSTE vara "EncryptedSummary". Denna ström finns bara i ett krypterat dokument. Innehållet i denna ström specificeras i [MS-OFFCRYPTO] avsnitt 2.3.5.4.

#### Digital signaturlagring ####

En valfri lagring vars namn MÅSTE vara "_xmlsignatures". Det KAN utelämnas och KAN ignoreras. Innehållet i denna lagring specificeras i [MS-OFFCRYPTO] avsnitt 2.5.2.

#### Anpassad XML-datalagring ####

En valfri lagring vars namn MÅSTE vara "MsoDataStore". Innehållet i lagringen specificeras i [MS-OSHARED] avsnitt 2.3.6.

#### Signaturström ####

En valfri ström vars namn MÅSTE vara "_signatures". Det BÖR utelämnas och KAN ignoreras. Innehållet i denna ström specificeras i [MS-OFFCRYPTO] avsnitt 2.5.1.

## Referenser ##

* [PPT-filformatsspecifikationer](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint-filformat](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

