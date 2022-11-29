{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "fil", "tillägg", "filformat", "Word", "Dokument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word-dokumentfil",
  "description":"Läs mer om DOC-filformat och API:er som kan skapa och öppna DOC-filer.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Vad är en DOC fil?

Filer med filtillägget .doc representerar dokument som genererats av Microsoft Word eller andra ordbehandlingsdokument i binärt filformat. Tillägget användes från början för klartextdokumentation på flera olika operativsystem. Den kan innehålla flera olika typer av data som bilder, formaterad såväl som vanlig text, grafer, diagram, inbäddade objekt, länkar, sidor, sidformatering, utskriftsinställningar och mycket annat. Formatet var populärt för alla typer av dokumentation på grund av de olika alternativ som det erbjuder användarna för att skriva manualer, förslag, specifikationer, CV, artiklar eller liknande dokument. Den uppdaterade versionen av DOC är [DOCX](/sv/Word%20Processing/DOCX/) som är baserad på Office OpenXML vars specifikationer är öppet tillgängliga.

## Kortfattad bakgrund ##

WordPerfect, en produkt från [Corel](https://www.corel.com/en/), använde DOC som en förlängning av deras proprietära format. På 1980-talet förblev WordPerfect valet av användning på de flesta datorer på grund av dess lättillgänglighet, överensstämmelse med de flesta datormaskiner och operativsystem. Men WordPerfect såg sin undergång för Windows OS när Microsoft introducerade Microsoft Word som sin produkt för dokumentfilformat och valde DOC-tillägget för deras proprietära format. I takt med att Microsoft Word blev mer och mer populärt, genomgick DOC-filformatet flera revisioner från Microsoft Word 97 - 2003. Det var 2007 när standard DOC-filformatet ersattes av Office Open XML-formatet (känd som DOCX) och de nya versionerna av Microsoft Word använder nu detta nya tillägg som standardfilformat.

## DOC-filformatspecifikationer - Mer information

Microsoft släppte inte DOC-filformatspecifikationerna på länge förrän 2008. I februari 2008 släpptes formatspecifikationer för .doc-filformat under Microsofts Open Specification Promise. Även om specifikationen inte beskriver alla funktioner som används av DOC-formatet, ger den riklig information om den kunskap som krävs för att arbeta med detta filformat. Ändå krävs reverse engineering för att kunna använda den tillgängliga informationen. Specifikationerna har uppdaterats flera gånger och den senaste [revisionen](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) är 8.0 som uppdaterades i augusti 2018 .

### Några grundläggande begrepp ###

Innan vi går in på några detaljer om filformatspecifikationerna för DOC, är några grundläggande begrepp nödvändiga att förstå för att kunna arbeta med detta filformat.

**Filinformationsbas (Fib):** Fib-strukturen innehåller information om dokumentet och anger filpekarna till olika delar som utgör dokumentet.
Fib är en struktur med variabel längd. Med undantag för basdelen som är fast i storlek, föregås varje avsnitt av ett räknefält som anger storleken på nästa avsnitt.

**Teckenposition:** CP eller Character Position representerar ett osignerat 32-bitars heltal som fungerar som det nollbaserade indexet för ett tecken i dokumenttexten. Platsen och storleken för varje tecken i filen kan inte hämtas direkt och måste beräknas med en fördefinierad algoritm. Karaktärerna inkluderar:

* Text i dokumentet
* Ankare av objekt som fotnoter eller textrutor
* Kontrolltecken som styckemärken och tabellcellmärken

**PLC:** PLC-strukturen är en array av CP:er följt av en array av dataelement. Dataelementen för alla PLC måste ha samma storlek på noll eller fler byte, och av denna anledning måste antalet CP:er vara en mer än antalet dataelement. PLC-strukturer är av olika typer där varje typ anger om duplicerade CP:er är tillåtna för den typen eller inte. En PLC-struktur består av:

* **aCP (variabel längd):** En uppsättning CP-element. Varje typ av **PLC**-struktur specificerar innebörden av CP-elementen och det tillåtna intervallet.
* **aData (variabel längd):** Varje typ av **PLC**-struktur specificerar strukturen och betydelsen av dataelementen, eventuella restriktioner för antalet dataelement och eventuella restriktioner för data som finns däri. Den specificerar också förhållandet mellan dataelementen och motsvarande CP.

**Giltigt urval:** .DOC-filkonstruktionerna beskrivs huvudsakligen av en rad CP:er. Det finns ett antal [regler](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) specificerade av Microsoft som ska följas i sådana fall.

**STTB:** STTB är en strängtabell som består av en rubrik som följs av en array av element. Värdet **cData** anger antalet element som finns i arrayen.

**Egenskapslagring:** En word-fil kan ha olika element som text, stycken, tabeller, bilder och avsnitt där var och en kan ha sina egna egenskaper. Egenskaper för dessa lagras i Word-filen som skillnader från standard. Sådana skillnader specificeras av PRl som består av en Single Property Modifier (Sprm) och dess operand. En applikation kan bestämma den slutliga uppsättningen egenskaper genom tillämpning av listor med **Prl**s.

**Lösenordsskydd:** Word-filer kan också lösenordsskyddas, för vilket en av följande mekanismer kan användas.

* XOR Obfuskation
* Office binärt dokument RC4-kryptering
* Office binärt dokument RC4 CryptoAPI-kryptering

Om FibBase.fEncrypted och FibBase.fObfuscation båda är 1, obfuskeras filen genom att använda XOR-obfuskation.

Om FibBase.fEncrypted är 1 och FibBase.fObfuscation är 0, krypteras filen genom att använda antingen Office Binary Document RC4 Encryption eller Office Binary Document RC4 CryptoAPI Encryption, med EncryptionHeader lagrad i de första FibBase.lKey byten i tabellströmmen. EncryptionHeader.EncryptionVersionInfo anger vilken krypteringsmekanism som användes för att kryptera filen.

### Filstruktur ###

En binär Word-fil i sin originalitet är en OLE-sammansatt fil som består av flera lagringar och strömmar. Dessa lagringar och strömmar har sin egen struktur och storlekar, som anger parametrarna för att skriva och läsa. Dessa är:

#### WordDocument Stream ####

Denna ström innehåller dokumenttexten och annan information som refereras från andra delar av filen. Strömmen har ingen fördefinierad struktur förutom FIB i början, vilket är obligatoriskt och bör vara på offset 0. Denna ström får inte vara större än 2147 MB.

#### 1TableStream eller 0TableStream ####

En binär Word-fil kan innehålla tabellströmmar som kallas 1Table stream eller 0Table stream. Minst en av dessa bör finnas i dokumentet. Men om ett dokument innehåller både 1Table- och 0Table-strömmar, används endast strömmen som refereras till av base.fWhichTblStm. Strömmen som inte refereras till MÅSTE ignoreras.
Tabellströmmen FÅR INTE vara större än 2147 MB.

#### Dataström ####

Dataströmmen har ingen fördefinierad struktur. Den innehåller data som refereras från FIB eller från andra delar av filen. Denna ström behöver inte finnas om det inte finns några referenser till den. Dataströmmen FÅR INTE vara större än 2147 MB.

#### Objektpoollagring ####

Objektpoollagringen innehåller lagringar för inbäddade OLE-objekt. Denna lagring behöver inte finnas om det inte finns några inbäddade OLE-objekt i dokumentet.

#### Anpassad XML-datalagring ####

Den anpassade XML-datalagringen är en valfri lagring vars namn MÅSTE vara "MsoDataStore".

#### Sammanfattningsinformationsström ####

Sammanfattningsinformationsströmmen är en valfri ström vars namn MÅSTE vara "\005SummaryInformation", där \005 är tecknet med värdet 0x0005, och inte den bokstavliga strängen "\005".

#### Informationsström för dokumentsammanfattning ####

Dokumentsammanfattningsinformationsströmmen är en valfri ström vars namn MÅSTE vara "\005DocumentSummaryInformation", där \005 är tecknet med värdet 0x0005, inte den bokstavliga strängen "\005".

#### Krypteringsström ####

Krypteringsströmmen är en valfri ström vars namn MÅSTE vara "kryptering". Denna ström FÅR INTE vara närvarande om inte båda följande villkor är uppfyllda:

* Dokumentet är krypterat med Office Binary Document RC4 CryptoAPI-kryptering.
* fDocProps-värdet ställs in i EncryptionHeader.Flags.

#### Makronlagring ####

Makronlagringen är en valfri lagring som innehåller makron för filen. Om det finns MÅSTE det vara en Project Root Storage.

#### XML-signaturlagring ####

XML-signaturlagringen är en valfri lagring vars namn MÅSTE vara "_xmlsignatures".

#### Signaturström ####

Signaturströmmen är en valfri ström vars namn MÅSTE vara "_signaturer". Denna ström innehåller digitala signaturer.

#### Information Rights Management Data Space Storage ####

Information Rights Management Data Space-lagring är en valfri lagring vars namn MÅSTE vara "\006DataSpaces", där \006 är tecknet med värdet 0x0006, och inte den bokstavliga strängen "\006". Om denna lagring finns, MÅSTE den skyddade innehållsströmmen också finnas.
Om denna lagring finns, SKA alla specificerade strömmar och lagringar förutom denna lagring och den skyddade innehållsströmmen läsas från den skyddade innehållsströmmen enligt [MS-OFFCRYPTO] och om någon av dessa strömmar och lagringar finns utanför det skyddade innehållet Stream, de SKA ignoreras.

#### Skyddad innehållsström ####

Den skyddade innehållsströmmen är en valfri ström vars namn MÅSTE vara "\009DRMContent", där \009 är tecknet med värdet 0x0009, och inte den bokstavliga strängen "\009".
Om denna ström är närvarande, MÅSTE även lagringsutrymmet för informationsrättshantering finnas.

## Referenser ##

* [MS-DOC filformateringsspecifikationer](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

