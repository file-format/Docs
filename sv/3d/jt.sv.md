{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "fil", "tillägg", "format", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om JT-filformat och API:er som kan skapa och öppna JT-filer.",
  "title" :"JT - Jupiter Tessellation File Format",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är JT fil?

**JT** (Jupiter Tessellation) är ett effektivt, industrifokuserat och flexibelt ISO-standardiserat 3D-dataformat utvecklat av Siemens PLM Software. Mekaniska CAD-domäner inom flyg-, bilindustrin och tung utrustning använder JT som sitt mest ledande 3D-visualiseringsformat.

JT-format är en scengraf som stöder de attribut och noder som är CAD-specifika. Sofistikerade komprimeringstekniker används för att lagra facettdata (trianglar). Detta format är strukturerat för att stödja visuella attribut, produkt- och tillverkningsinformation (PMI) och metadata. Det finns ett bra stöd för asynkron streaming av innehåll. Inom tung mekanisk industri använder proffs JT-filer i sina CAD-lösningar och program för produktlivscykelhantering (PLM) för att undersöka geometrin hos komplicerade varor.

Eftersom JT stöder nästan alla viktiga 3D CAD-format, kan dess sammansättning hantera en mängd olika kombinationer som kallas "multi-CAD". Denna multi-CAD-sammansättning är alltid välskött och uppdaterad eftersom synkronisering mellan inhemska CAD-produktbeskrivningsfiler med tillhörande JT-filer sker automatiskt. JT-filer är ursprungligen lätta, så de anses vara lämpliga för internetsamarbeten. Företag samarbetar genom att skicka 3D-visualiseringar över media mycket lättare jämfört med "tunga" original-CAD-filer. Dessutom säkerställer JT-filer många säkerhetsfunktioner som gör delning av immateriella rättigheter säkrare.

## Kort historik om JT-filformat

Engineering Animation, Inc. och Hewlett Packard var de ursprungliga designers av JT, som utvecklade det formatet som Direct Model Toolkit. Efter att EAI förvärvades av UGS Corp. blev JT en del av UGS:s svit. Tidigt 2007 tillkännagav UGS JT som deras master 3D-format. Samma år köpte Siemens AG UGS och visade sig vara Siemens PLM Software. Siemens använder JT som det vanliga interoperabilitetsformatet och dataarkiveringsformatet. Under 2009 accepterade ISO JT-specifikationen för publicering som en ISO Publicly Available Specification (PAS). I mitten av 2010 meddelade ProSTEP iViP att på industriell nivå kan JT och STEP AP 242 XML användas tillsammans för att uppnå maximal fördel i data utbytesscenarier. Under 2012 har JT officiellt deklarerats som ett ISO-standardiserat (ISO 14306:2012 (ISO JT V1)) 3D-visualiseringsformat.

## JT filformat ##

Alla objekt i JT-formatet representeras genom en objektidentifierare och referenser mellan objekt hanteras genom refererade objekts identifierare. Integriteten hos dessa objektreferenser kan upprätthållas genom att pekare svänger av/svrider.

En JT-fil är arrangerad som en serie block och Header-blocket är alltid det första datablocket i filen. En serie datasegment och ett TOC-segment följer omedelbart efter huvudblocket. Det ena datasegmentet (6 LSG-segment) har en referenskompatibel JT-fil finns alltid. TOC-segmentet innehåller platsinformationen för alla andra datasegment i den filen.

{{< figure src="../JT-1.png" alt="JT filformat" >}}

### Filhuvud ###

File Header är det första blocket i JT-filens datahierarki. Versioneringsinformation och TOC-platsinformation är innesluten i rubriken vilket underlättar laddare vid filläsning. Innehållet i filhuvudet är ordnat enligt följande.

### TOC-segment ###

TOC-segmentet måste finnas i en fil och innehåller identifierings- och platsinformation för alla andra datasegment. Den faktiska platsen för TOC-segmentet anges av fältet TOC Offset i filhuvudet. Varje individuellt adresserbart datasegment representeras av TOC-post i ett TOC-segment.

### Datasegment ###

JT-filen definierar all lagrad data inom ett datasegment. Vissa datasegment kan komprimera alla databytes med information som finns kvar inom segmentet. Datasegment har följande struktur:

![alt text](../JT-2.png "JT Data Segment")

Följande tabell beskriver olika typer av datasegment:

|Namn|Beskrivning
---|---|
|LSG segment|Omfattar en samling objekt länkade genom riktade referenser för att bilda LSG (riktad acyklisk grafstruktur)
|Shape LOD-segment|innehåller definierande data för de geometriska formerna (t.ex. hörn, normaler, polygoner, etc)
|JT B-Rep Segment|Har element för att data ska representera den exakta geometriska gränsen för en enskild del i JT B-Rep-format.
|XT B-Rep segment|Har element för att data ska representera den exakta geometriska gränsen för en enskild del i gränsrepresentationsformat
|Wireframe-segment|Datan representerar exakt 3D-wireframe för en viss del definieras av ett element som ingår i detta segment.
|Metadatasegment|Tillåter att lagra metadata i distinkta adresserbara segment.
|JT ULP-segment|Har element för att data ska representera den semi-exakta geometriska gränsen för en enskild del i JT ULP-format.
|JT LWPA segment|Innehåller ett element definiera analytisk data för en viss del. LWPA omsluter den analytiska ytsamlingen i b-rep-definitionen av delen.

## Kompression ##

Kraven på överföring och lagring av 3D-modeller är mer krävande, så JT-filer kan dra fördel av komprimering. En JT-datamodell kan vara sammansatt av olika filer med olika komprimeringstekniker, men komprimeringsprocessen är transparent för JT-dataanvändare.

Hittills är JT Open Toolkit (som standard) och avancerad komprimering två komprimeringstekniker som används av JT-filer. JT Open Toolkit använder en enkel, förlustfri komprimeringsalgoritm, medan den avancerade komprimeringen använder en mer förfinad, domänspecifik komprimeringsteknik leder till förlustfri geometrikomprimering. Klientapplikationer föredrar avancerad komprimering snarare än att använda standardkomprimering, eftersom avancerad komprimering ger ganska höga kompressionsförhållanden. Bakåtkompatibilitet med vanliga JT-filvisningsprogram bibehålls genom tillhandahållandet av standardkomprimering. Komprimeringsformuläret måste vara kompatibelt med versionen av JT-filformatet som kan ses när en JT-fil öppnas med hjälp av textredigerare och inkluderas i ASCII-huvudinformation.

## Referenser ##

* [JT File Format Reference](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (visualization format)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

