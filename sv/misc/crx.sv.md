{
"date": "2023-06-08",
  "keywords": [
"crx-fil",
"vad är en crx-fil",
"hur man installerar crx-fil i google chrome",
"hur man öppnar crx-fil",
"vad innehåller crx-filen",
"vilket är formatet på crx-filen",
"fil",
"crx filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CRX-filformat - Google Chrome-tillägg",
  "description":"Lär dig mer om CRX-format och API:er som kan skapa och öppna CRX-filer.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Vad är en CRX fil?

CRX-filformat är associerat med webbläsartillägg för Google Chrome. En CRX-fil är i huvudsak ett komprimerat paket som innehåller nödvändiga filer och metadata för att ett tillägg ska installeras och köras i Google Chrome. Det förbättrar funktionaliteten eller utseendet på en webbläsare genom att tillhandahålla en extra funktion eller ett tema.

När en CRX-fil laddas ner och installeras i Google Chrome, verifierar webbläsaren tilläggets integritet med hjälp av offentlig nyckel och signatur. Om verifieringen lyckas extraherar Chrome innehållet i CRX-filen och installerar tillägget, vilket gör det tillgängligt för användning. Användare kan hantera sina tillägg via Chrome Extensions-sidan, som gör det möjligt att aktivera, inaktivera eller ta bort installerade tillägg.

## Hur installerar man CRX-fil i Google Chrome?

För att installera en CRX-fil i Google Chrome kan du följa dessa steg:

1. Öppna webbläsaren Chrome.
2. Skriv `chrome://extensions` i adressfältet och tryck på Retur.
3. Aktivera växlingsknappen "Utvecklarläge" i det övre högra hörnet av tilläggssidan.
4. Klicka på knappen "Ladda uppackad".
5. Leta upp och välj mappen som innehåller det extraherade innehållet i CRX-filen (eller välj helt enkelt själva CRX-filen).
6. Klicka på "Öppna" för att installera tillägget.

## Vad innehåller CRX-filen?

En CRX-fil innehåller nödvändiga filer och metadata som krävs för Google Chrome-tillägget. Här är en uppdelning av typiskt innehåll som finns i en CRX-fil:

- **Manifest-fil (manifest.json):** Den här filen är en JSON-formaterad fil som innehåller information om filtillägg som dess namn, version, beskrivning, behörigheter och bakgrundsskript. Den definierar förlängningens struktur och beteende.
- **JavaScript-filer:** Dessa filer innehåller koden som definierar tilläggets funktionalitet. De kan innehålla skript för att hantera händelser, modifiera webbsidor eller interagera med Chromes API:er.
- **HTML, CSS och bildfiler:** Tillägg innehåller ofta användargränssnittselement, som popup-fönster eller alternativsidor. HTML-filer definierar strukturen för dessa gränssnitt, medan CSS-filer styr deras utseende. Bildfiler används för ikoner eller andra grafiska tillgångar.
- **Valfria resursfiler:** Tillägg kan innehålla ytterligare resurser, till exempel lokaliseringsfiler för stöd för flera språk. Dessa filer innehåller översättningar av text som används i tilläggets användargränssnitt.
- **Bakgrundsskript:** Om ett tillägg har bakgrundsprocesser eller skript som körs oberoende av aktiv webbsida, kommer dessa skript att inkluderas i CRX-filen.
- **Innehållsskript:** Innehållsskript är skript som kan injiceras på webbsidor för att ändra deras beteende eller interagera med deras innehåll. Om tillägget använder innehållsskript, kommer de nödvändiga filerna för dessa skript att finnas i CRX-filen.
- **Andra tillgångar:** Beroende på specifika krav för tillägg kan ytterligare filer som ljud- eller videofiler, typsnitt eller datafiler inkluderas.

CRX-filformatet är i huvudsak ett komprimerat paket som innehåller alla dessa filer och mappar på ett strukturerat sätt. När CRX-filen är installerad i Google Chrome extraherar webbläsaren innehållet och placerar det på lämpliga platser, vilket gör att tillägget kan laddas och köras i webbläsaren.

## Vilket är formatet på filen CRX?

CRX-filformatet är ett specifikt format för paketering och distribution av Google Chrome-tillägg. Det är i huvudsak ett komprimerat ZIP-arkiv med olika filtillägg. Den grundläggande strukturen för CRX-filen är som följer:

- **Filsignatur:** De första 4 byten av filen innehåller det magiska numret "Cr24" (hexadecimalt: 43 72 32 34) som fungerar som signatur för att identifiera filen som CRX-fil.
- **Versionsnummer:** De nästa 4 byten representerar versionsnumret för CRX-formatet.
- **Längd på den offentliga nyckeln:** Följande 4 byte indikerar längden på den kodade offentliga nyckeln som används för verifiering av tilläggssignatur.
- **Signaturens längd:** De efterföljande 4 byten anger längden på signaturen för tillägget.
- **Offentlig nyckel:** Det här avsnittet innehåller den kodade offentliga nyckeln som används för att verifiera tilläggets integritet.
- **Signatur:** Det här avsnittet innehåller signatur för tillägg, som genereras genom att signera tilläggets innehåll med en privat nyckel som motsvarar den offentliga nyckeln som nämns ovan.
- **ZIP-arkiv:** De återstående byten av CRX-filen består av ett komprimerat ZIP-arkiv. Detta arkiv innehåller alla nödvändiga filer och mappar med tillägg, inklusive manifestfiler, JavaScript-filer, HTML-filer, CSS-filer, bilder och andra resurser.

## Referenser
* [CRX-formatspecifikation](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

