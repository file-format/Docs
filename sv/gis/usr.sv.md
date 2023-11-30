{
"datum": "2023-08-03",
  "keywords": [
"usr",
"usr-fil",
"vad är en usr-fil",
"hur man öppnar usr-filen",
"fil",
"usr filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "USR-filformat - Lowrance GPS-datafil",
  "description":"Läs mer om USR-format och API:er som kan skapa och öppna USR-filer.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Vad är USR fil?

Filtillägget ".usr" är också relaterat till Lowrance GPS-enheter. I synnerhet används den för att lagra GPS-data i ett format som kallas "User Data Format" (USR-format) som används av Lowrance GPS-enheter.

När du använder en Lowrance GPS-enhet kan du spara dina waypoints, spår och rutter som ".usr"-filer. Dessa filer innehåller vanligtvis information som latitud, longitud, höjd, tidsstämpel och andra data relaterade till dina GPS-aktiviteter.

Här är några vanliga användningsområden för .usr-filer med Lowrance GPS-enheter:

- **Waypoints:** Waypoints är specifika platser markerade på GPS:en, som landmärken, favoritfiskeplatser eller intressanta platser. Du kan spara dessa platser som .usr-filer och de kan importeras, exporteras eller delas med andra Lowrance GPS-användare.

- **Spår:** Spår representerar den registrerade banan för dina GPS-rörelser. Du kan spara dina spårloggar som .usr-filer, så att du kan granska och analysera dina rutter senare eller dela dem med andra.

- **Rutter:** Rutter är fördefinierade vägar som du kan skapa och spara på din GPS-enhet. Dessa rutter kan också sparas som .usr-filer för framtida användning eller delning.

För att hantera .usr-filer på din Lowrance GPS-enhet använder du vanligtvis programvara som Lowrances "Insight Planner" eller "Lowrance GPS Utility" för att importera, exportera och manipulera din GPS-data.

## USR-filformat - Mer information

I Lowrance iFinder GPS-enheter skapas .usr-filerna och sparas på MultiMediaCard-minneskortet (MMC) som satts in i enheten. Dessa filer innehåller användardata som waypoints, spår och rutter.

För att överföra .usr-filerna från MMC till en dator kan du följa dessa steg:

- **Ta bort MMC:** Ta försiktigt bort MultiMediaCard (MMC) från Lowrance iFinder GPS-enheten.

- **Sätt i MMC i datorn:** Använd en lämplig MMC-kortläsare för att sätta in minneskortet i din dators kortläsarplats.

- **Leta reda på .usr-filer:** När MMC har identifierats av din dator bör du kunna komma åt filerna som är lagrade på den. Leta efter .usr-filerna som innehåller dina GPS-data.

- **Konvertering med GPSBabel:** För att konvertera .usr-filerna till ett annat GPS-format kan du använda GPSBabel, som är ett gratis och öppen källkodsverktyg för att arbeta med olika GPS-filformat. GPSBabel stöder ett brett utbud av in- och utdataformat, vilket gör att du kan konvertera .usr-filerna till format som är kompatibla med andra GPS-program eller -enheter.

Du kan ladda ner GPSBabel från den officiella webbplatsen (http://www.gpsbabel.org/) och installera den på din dator. När den väl har installerats kan du använda programvarans kommandoradsgränssnitt eller grafiska användargränssnitt (om tillgängligt) för att utföra konverteringen.

Om du till exempel vill konvertera .usr-filer till GPX-format kan du använda ett kommando som:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Ovanstående kommando instruerar GPSBabel att läsa indatafilen "input.usr" i Lowrance USR-format och skriva utdatafilen "output.gpx" i GPX-format.

- **Importera/använda konverterade filer:** Efter konverteringen har du dina GPS-data i det nya formatet (t.ex. GPX), som du kan använda med annan GPS-programvara eller -enheter som stöder det formatet.

## Hur öppnar man filen USR?

Program som öppnar eller refererar till USR-filer inkluderar

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referenser
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

