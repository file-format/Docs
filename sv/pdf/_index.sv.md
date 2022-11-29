{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "grundläggande" ],
  "description":"Portable Document Format (PDF) är en standardrepresentation av dokument oberoende av programvara, hårdvara och OS. PDF-standarder inkluderar PDF/A, PDF/E, PDF/UA, PDF/VT och PDF/X.",
  "title" :"PDF-filformat - Vad är en PDF-fil?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) är en typ av dokument som skapades av Adobe redan på 1990-talet. Syftet med detta filformat var att införa en standard för representation av dokument och annat referensmaterial i ett format som är oberoende av applikationsprogramvara, hårdvara samt operativsystem. PDF-filformatet har full förmåga att innehålla information som text, bilder, hyperlänkar, formulärfält, rich media, digitala signaturer, bilagor, metadata, geospatiala funktioner och 3D-objekt i det som kan bli en del av källdokumentet.

I de flesta fall konverteras befintliga dokument till PDF istället för att skapa en ny PDF från början. Men det betyder inte att det inte finns någon programvara för att skapa eller manipulera PDF-filer.

**(Måste dela något om PDF-filformat? Du kan lägga upp dina resultat i avsnittet [PDF File Format News](https://news.fileformat.com/t/PDF).)**

## PDF-filformat - Kort historik

En snabb genomgång av tidslinjen om PDF-filbildningen när det gäller tidslinjen är följande:

**1993** - Adobe Systems gjorde PDF-specifikationerna tillgängliga utan kostnad

**2008** - PDF släpptes som en öppen standard den 1 juli 2008 och publicerades av International Organization for Standardization som **ISO 32000-1:2008**.

**2008** - Adobe publicerade en offentlig patentlicens till ISO 32000-1-formatet royaltyfria rättigheter för alla patent som ägs av Adobe och som är nödvändiga för att göra, använda, sälja och distribuera PDF-kompatibla implementeringar.

Den första versionen av PDF benämnd PDF 1.0 som senare gick igenom revisioner upp till PDF 1.7. PDF 1.7, som blev ISO 32000-1, inkluderar vissa icke-standardiserade egenutvecklade teknologier såväl som Adobe XML Forms Architecture (XFA) och JavaScript-tillägg för Acrobat. Det var den 28 juli 2017 när PDF 2.0, känd som ISO 32000-2:2017, publicerades som inte inkluderar några icke-standardiserade tekniker.

## Specifikationer för PDF-filformat

En PDF-fil är en uppsättning byte som kan grupperas i tokens enligt syntaxregler som definieras av PDF-specifikationer. En eller flera tokens kombineras för att bilda syntaktiska enheter på högre nivå, huvudsakligen objekt, som är de grundläggande datavärdena från vilka ett PDF-dokument är konstruerat.

### Filstruktur för PDF-filer

PDF-filens innehåll är ordnat i följande ordning inuti filen.

|Rubrik
|Kroppen
|Korsreferenstabell
| Trailer

#### PDF-filhuvud ####

Oavsett PDF-version börjar en PDF-fil med en rubrik som innehåller en unik identifierare för PDF och versionen av formatet som %PDF-1.x där x sträcker sig från 1-7.

#### Filtext ####

Brödtexten i en PDF-fil består av en sekvens av indirekta objekt som representerar innehållet i ett dokument. Objekten, som beskrivits ovan, representerar komponenter i dokumentet såsom typsnitt, sidor och samplade bilder. Från och med PDF 1.5 kan kroppen också innehålla objektströmmar, som var och en innehåller en sekvens av indirekta objekt.

#### Korsreferenstabell ####

Korsreferenstabellen innehåller information som tillåter slumpmässig åtkomst till indirekta objekt i filen så att hela filen inte behöver läsas för att hitta något speciellt objekt. Tabellen ska innehålla en enradspost för varje indirekt objekt, som anger byteoffset för det objektet i filens brödtext. (Från och med PDF 1.5 kan en del eller all korsreferensinformation alternativt finnas i korsreferensströmmar.

#### File Trailer ####

Trailern till en PDF-fil gör det möjligt för en läsare att snabbt hitta korsreferenstabellen och vissa specialobjekt. Konforma läsare bör läsa en PDF-fil från dess ände. Den sista raden i filen ska endast innehålla filslutmarkören, %%EOF. De två föregående raderna ska innehålla, en per rad och i ordning, nyckelordet startxref och byteoffset i den avkodade strömmen från början av filen till början av xref nyckelordet i den sista korsreferenssektionen.

### PDF-objekt ###

En PDF-fil innehåller flera olika typer av objekt som är av följande typer

* Booleska värden - representerar villkorligt sant eller falskt
* Tal - heltal och reella värden
* Strängar - innehåller tecken inom parentes
* Namn - börja med ett framåt / tecken t.ex. /ASomewhatLongerName resulterar i ASomewhatLongerName
* Arrayer - PDF stöder endimensionella arrayer. Matriser med högre dimensioner kan konstrueras genom att använda matriser som kapslade element
* Ordböcker - samling av objekt som nyckel-värde-par. Den kan ha noll poster.
* Strömmar - representerar en sekvens av byte som också kan vara av obegränsad längd
* Null Object - representerar ett nollvärde

Det kan finnas andra andra objekt som kommentarer som introduceras med %-tecknet och kan innehålla 8-bitars tecken.

### Indirekta objekt ###

Alla objekt i en PDF-fil kan märkas som ett indirekt objekt. Indirekta objekt ges en unik objektidentifierare med vilken andra objekt kan referera till det. Korsreferenser till dessa behålls i en indextabell och markeras med nyckelordet xref som följer huvuddelen och ger byteoffset för varje indirekt objekt från början av filen.

### Linjära och icke-linjära PDF-layouter ###

PDF-layouter kategoriseras som Llnära och icke-linjära beroende på målapplikationerna och andra faktorer.

Icke-linjär - Icke-linjära PDF-filer använder mindre diskutrymme jämfört med linjära PDF-filer. PDF-sidor av dokumentet finns i spridd form över PDF-filen och det är därför icke-linjära filer är långsammare jämfört med linjära filer.

Linjär PDF - Linjära PDF-filer är inriktade på online-PDF-visare konstruerade på ett sådant sätt att de skrivs till disk på ett linjärt sätt. Detta kräver inte webbläsarplugin för att hela dokumentet ska laddas först innan visning.

### Objektöversikt ###

Som nämnts är PDF body en samling objekt som nämns ovan. PDF är till stor del baserad på PostScript utan kontrollfunktionerna i programmeringsspråk som if och loop-kommandon. Kommandon som utfärdas av Postscript-kod för att generera grafiskt innehåll samlas in och tokeniseras utöver alla filer, grafik eller typsnitt som dokumentet refererar till. Allt detta innehåll ackumuleras till en enda fil, vilket resulterar i sammansatt PostScript-utdata.

#### Text ####

Text i PDF representeras av textelement som faktiskt visas med glyfer från teckensnitt. En glyf är en grafisk form och är föremål för alla grafiska manipulationer, såsom koordinattransformation. På grund av vikten av text i de flesta sidbeskrivningar ger PDF möjligheter på högre nivå att beskriva, välja och återge glyfer på ett bekvämt och effektivt sätt.

#### Grafik ####

Grafikoperatorerna som används i PDF-innehållsströmmar beskriver utseendet på sidor som ska reproduceras på en rasterutgångsenhet. Faciliteterna är avsedda för både skrivar- och displayapplikationer. Grafikoperatorerna bildar sex huvudgrupper:

* Grafiktillståndsoperatörer manipulerar datastrukturen som kallas grafiktillståndet, det globala ramverket inom vilket de andra grafikoperatörerna exekverar. Grafiktillståndet inkluderar den aktuella transformationsmatrisen (CTM), som mappar användarutrymmeskoordinater som används i en PDF-innehållsström till utdataenhetskoordinater. Den inkluderar också den aktuella färgen, den aktuella klippbanan och många andra parametrar som är implicita operander för målningsoperatorerna.
* Bankonstruktionsoperatörer anger banor som definierar former, linjebanor och regioner av olika slag. De inkluderar operatorer för att starta en ny bana, lägga till linjesegment och kurvor till den och stänga den.
* Banmålningsoperatorer fyller en bana med en färg, målar en linje längs den eller använder den som en klippgräns.
* Andra målaroperatörer målar vissa självbeskrivande grafikobjekt. Dessa inkluderar samplade bilder, geometriskt definierade skuggningar och hela innehållsströmmar som i sin tur innehåller sekvenser av grafikoperatorer.
* Textoperatorer väljer och visar teckenglyfer från teckensnitt (beskrivningar av typsnitt för att representera texttecken). Eftersom PDF behandlar glyfer som allmänna grafiska former, kan många av textoperatorerna grupperas med grafiktillståndet eller målningsoperatorerna. Datastrukturerna och mekanismerna för att hantera glyf- och teckensnittsbeskrivningar är dock tillräckligt specialiserade.
* Markerade innehållsoperatörer associerar logisk information på högre nivå med objekt i innehållsströmmen. Denna information påverkar inte innehållets återgivna utseende; det är användbart för program som använder PDF för dokumentutbyte.

## Referenser ##

* [PDF-filformat: Grundläggande struktur](https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [PDF-referens - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

