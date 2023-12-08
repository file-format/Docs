{
"datum": "2023-03-14",
  "keywords": [
"crypt14 fil",
"vad är en crypt14-fil",
"fil",
"crypt14 filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CRYPT14-filformat - WhatsApp-krypterad databasfil",
  "description":"Läs mer om CRYPT14-format och API:er som kan skapa och öppna CRYPT14-filer.",
  "linktitle": "CRYPT14",
  "menu": {
    "docs": {
      "identifier": "database-crypt14",
      "parent": "database"
}
},
"lastmod": "2023-03-14"
}

## Vad är en CRYPT14 fil?

En CRYPT14-fil är en typ av fil som används av meddelandeappen WhatsApp för att lagra krypterad meddelandedata på en Android-enhet. När du använder WhatsApp för att skicka och ta emot meddelanden, krypterar appen dessa meddelanden så att de inte kan läsas av någon som fångar upp dem. WhatsApp lagrar dessa krypterade meddelanden i en databasfil på din Android-enhet. Databasfilen har filtillägget .crypt14, vilket indikerar att den är krypterad med en specifik krypteringsalgoritm.

Krypteringen som används av WhatsApp för att skydda data i crypt14-filen är end-to-end-kryptering, vilket innebär att endast avsändaren och mottagaren av ett meddelande kan läsa dess innehåll. WhatsApp använder signalprotokollet för end-to-end-kryptering, vilket anses vara mycket säkert.

Du kan inte öppna eller läsa en crypt14-fil direkt, eftersom data är krypterad och endast kan nås av WhatsApp med hjälp av lämpliga krypteringsnycklar. För att återställa din WhatsApp-chatthistorik från en säkerhetskopia måste du följa stegen från WhatsApp för att återställa data i appen.

## CRYPT14 Filformat – Mer information

När du säkerhetskopierar dina WhatsApp-meddelanden på en Android-enhet skapar appen en säkerhetskopia som innehåller din chatthistorik, mediefiler och andra data. Denna säkerhetskopia har filtillägget .crypt14 om den skapades med WhatsApp version 2.12.556 eller senare.

För att återställa dina WhatsApp-meddelanden från en .crypt14 säkerhetskopia kan du följa dessa steg:

1. Överför säkerhetskopian till din nya Android-enhet eller till samma enhet efter en fabriksåterställning.
2. Installera WhatsApp på enheten och verifiera ditt telefonnummer.
3. När du uppmanas, välj att återställa din chatthistorik från säkerhetskopian.
4. Vänta tills återställningsprocessen är klar. Detta kan ta lite tid om du har en stor mängd data i din säkerhetskopia.
5. När återställningen är klar bör du kunna komma åt alla dina säkerhetskopierade WhatsApp-meddelanden och mediafiler på din Android-enhet.

Det är värt att notera att om du har en säkerhetskopia från en äldre version av WhatsApp (före version 2.12.556), kan filen ha ett annat filtillägg och kanske inte är kompatibel med nyare versioner av appen. I så fall kan du behöva först uppdatera din WhatsApp-app till den senaste versionen och sedan skapa en ny säkerhetskopia.

## Referenser
* [WhatsApp](https://en.wikipedia.org/wiki/WhatsApp)

