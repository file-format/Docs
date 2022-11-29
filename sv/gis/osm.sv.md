{
  "date" : "2019-10-11",
  "keywords" :[ "osm-fil", "vad är en osm-fil", "fil", "osm-exempel", "osm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap filformat",
  "description":"Läs mer om OSM-filformat och API:er som kan skapa och öppna OSM-filer.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en OSM fil?

OpenStreetMap (OSM) är en enorm samling av frivilliga lagrade geografiska informationer i olika typer av filer, som använder olika kodningsscheman för att konvertera dessa data till bitar och bytes. OSM är ett samarbete för att skapa en gratis redigerbar karta över världen. Det primära resultatet av detta samarbete är geografiska data snarare än själva kartan. Restriktionerna för användning eller tillgänglighet av geografisk information över stora delar av världen utlöser behovet av att skapa ett OSM. Datan som är tillgänglig från OSM är redo att ersätta Google Maps för klassiska applikationer (Facebook, Craigslist etc.) och standarddata för GPS-mottagarens applikationer.^^ ^^Även om datakvaliteten är varierande över hela världen kan OpenStreetMap-data enkelt jämföras med patent datakällor.

## Kortfattad bakgrund ##

Inspirerad av framgången med Wikipedia skapade Steve Coast en brittisk entreprenör 2004 detta samhällsbaserade världskartläggningsprojekt i Storbritannien. Han fokuserade till en början på att kartlägga Storbritannien. OpenStreetMap Foundation grundades först i april 2006 för att stödja utvecklingen, expansionen och cirkulationen av gratis geospatial för vem som helst. I december 2006 hjälpte Yahoo OpenStreetMap med sin flygfotografering för kartproduktion. Fullständig vägdata för Nederländerna och stamvägsdata för Indien och Kina bidrog till OSM i april 2007 av Automotive Navigation Data (AND). I december 2007 var Oxford University den mest framstående organisationen som integrerade OpenStreetMap-data på sin huvudwebbplats. Sedan dess har över 2 miljoner registrerade användare bidragit med data i detta projekt med hjälp av GPS-enheter, flygfotografering och manuella undersökningar. Denna community-bidragsdata görs tillgänglig under Open Database License. En England-registrerad, ideell organisation OpenStreetMap Foundation upprätthöll OSM-webbplatsen.

## OSM-filformat ##

Det finns många sätt och filformat att lagra geografiska data men **OSM** filformat är begränsat till OpenStreetMap. OSM är speciellt utformat standardformat avsett att enkelt transporteras över internet. Ett strukturerat ordnat format, kodat i XML, utgör en .osm-fil. I OpenStreetMap finns det fyra pivotelement för att lagra topologisk datastruktur:

{{< figure src="../OSM.png" alt="OSM filformat" >}}


|Noder|Vägar|Relationer|Taggar
---|---|---|---|
|<ul><li> Representerar geografisk position lagrad som par av en latitud och en longitud.</li><li> Används för att representera kartfunktioner utan storlek, till exempel bergstoppar.</li></ul> |<ul><li> Sorterade listor med noder, som betecknar en polylinje eller en polygon</li><li> Representerar linjära egenskaper som vägar och floder och zoner, som parkeringsområden, djungler och parker.</li></ul> |<ul><li> Sorterade listor med noder och vägar representerar deras relation som barriärer och u-svängar på vägar, motorvägar spänner över olika befintliga vägar och områden med hål.</li></ul> |<ul><li> Lagra metadata om kartobjekten.* Alltid kopplad till någon nod, väg eller en relation</li></ul>


Taggar används för att karakterisera fysiska egenskaper på marken (byggnader och vägar etc.) i OpenStreetMap. Varje tagg relaterar en geografisk egenskap hos den egenskap som representeras av den specifika noden eller relationen. I detta kostnadsfria taggningssystem, för att beskriva en funktion, kan ett obegränsat antal attribut inkluderas i en karta. Specifika nyckel- och värdekombinationer som godkänts av registrerade användare fungerar som informella standarder för de ofta använda taggarna. Däremot kan nya taggar skapas när nya aspekter kräver att analysera tidigare omappade attribut för funktionerna. De flesta funktioner använder bara ett litet antal taggar för beskrivning.

Tre typer av filer används av OSM för att lagra dess huvuddata.

OSM hanterar alla dessa filer med information om deras formateringsdetaljer. Men samma interna objekt produceras av dessa filer. För datafiler är den synliga flaggan på OSM-objekt alltid sann vilket inte är fallet för historik- och ändringsfiler.

I vanligt bruk finns det en mångfald i OSM-filformat. Filformat definierar innehållskodningen på disk eller tråd i bitar och byte. OSM kan läsa och skriva maximalt av dessa format.

**XML**

Det ursprungliga OSM-formatet är XML-baserat. Returdata från huvud-OSM-databasens API är i XML-format.

**PBF**

Protokollbuffertkodning står på binärt format och ett av de mest kompakta formaten.

**O5M/O5C**

Binärt format baserat enklare format men relativt mindre använt. OSM kan läsa men inte skriva detta format.

**OPL**

Ett enkelt format som föreslås att användas med vanliga UNIX-kommandoradsverktyg. Nära till CSV-filer, tillåter en OSM-enhet på en rad.

**DEBUG**

Ett textbaserat format avsett att skapa för felsökning. OSM kan skriva detta format men kan inte läsa.

**SVART HÅL**

Ett dummyformat som tar bort all data. OSM kan skriva detta format men kan inte läsa.

## OSM-datalagring ##

OSM:s huvudsakliga **PostgreSQL**-databas behåller huvudkopian av OSM-data med PostGIS-tillägget. För varje primitiv data upprätthåller huvuddatabasen en tabell vars rader lagrar enskilda objekt. Alla redigeringar uppdaterar denna databas och alla andra format skapas med hjälp av denna databas. Många nedladdningsbara databaspooler skapas för att överföra data från en plats till en annan. Två format, ett som använder XML och ett annat som använder Protocol Buffer Binary Format (PBF) definierar dessa pooler. Den fullständiga informationen lagras i en fil som heter planet.osm

## Komprimering i OSM-filer ##

Textbaserade format (XML, OPL och Debug) använder valfritt gzip- eller bzip2-komprimering.

## Referenser ##

* [Manual för OSM-filformat](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Lär dig OSM](https://learnosm.org/en/osm-data/getting-data/)

