{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "tillägg", "fil", "format", "system", "LNK-fil", "länk", "LNK-filer", "LNK-dokument", "applikation", "program" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Länkfilformat",
  "description":"Läs mer om LNK-filformat och API:er som kan skapa och öppna LNK-filer.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Vad är LNK fil? ##

En LNK-fil, analog med en identitet på Mac-systemet, är ett Windows-alternativ eller "länk" som fungerar som en anslutning till en originalbilddokumentmapp, eller ett program. Den innehåller typ, position och filnamn för genvägsdestinationen, såväl som programmet som öppnar måldokumentet och ytterligare en kortkommando.

I Windows, rakt ut en fil, mapp eller ett körbart program och välj Skapa genväg. Placeringen av filformatet och "Början"-katalogen är två grundläggande funktioner i LNK-filer. Filformatet för LNK-filer är maskerat, och en böjd pil indikerar att de är genvägar.

## LNK filformat ##

LNK-filformat har vanligtvis samma ikon som sina målfiler, men med tillägg av en liten krökt pil för att visa att filen pekar på en annan plats. När genvägen dubbelklickas, beter sig den som om användaren hade dubbelklickat på den faktiska filen.

LNK-filer som innehåller programgenvägar kan ha egenskaper som påverkar hur programmet körs. För att ändra attributen, högerklicka på genvägsfilen och välj **Egenskaper** och ändra sedan fältet Mål.

Istället för att vara filtillägg är LNK-filer Windows Explorer-tillägg. Som ett terminaltillägg kan .lnk-dokument endast användas i Utforskaren i Windows för att ersätta en fil, och de har andra syften i Utforskaren i Windows förutom att fungera som en genväg till ett lokalt dokument. Dessa filer börjar också med bokstaven "L".

Medan genvägar länkar till specifika filer och kataloger när de skapas, kan de bli obrukbara om målet ändras till en annan plats. Utforskaren kommer att börja reparera en genvägsmapp som pekar på ett dött mål när den öppnas.


## Teknisk specifikation ##

Endast när mappvisningsinställningen "Dölj filtillägg för igenkända filtyper" är avmarkerad, visar inte Windows dokumenttillägget .lnk för dokumentgenvägar. Även om det inte rekommenderas, kan du aktivera filtillägget för att visas genom att ta bort egenskapen "NeverShowExt" från HKEY_CLASSES_ROOT\lnk-filen Windows-registerobjekt.

För att göra det, ta dessa steg:

* Öppna "Registreringsredigeraren" genom att ange "Regedit" i sökfältet i aktivitetsfältet och välja programmet
* I programmet, navigera till datorn\HKEY HKEY_CLASSES_ROOT\lnkfilplatsen
* Gör en säkerhetskopia av objektet genom att högerklicka på det och välja Exportera
* Välj och ta bort attributet "NeverShowExt".
* Windows bör startas om


## Referens ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
