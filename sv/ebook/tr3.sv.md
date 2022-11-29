{
  "date" : "2021-04-10",
  "keywords" :[ "TR3", "Fil", "Tillägg", "Filformat", "eBook", "TomeRaider", "Yadabyte" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om TR3-filformat och API:er som kan skapa och öppna TR3-filer.",
  "title" :"TR3 - TomeRaider 3 eBook File",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-04-10"
}

## Vad är TR3 fil? ##

TR3-filen är en TomeRaider 3 eBook som ger stöd för snabb sökning och komprimering. Det kan fungera korrekt genom TomeRaider-relaterade program. Yadabyte är utvecklaren av denna programvara, ett brittiskt mjukvaru- och webbutvecklingsföretag baserat i Storbritannien. TomeRaider eBook Reader-applikationen kan användas för att fungera korrekt och hantera innehållet i dessa TR3-filer. Denna relaterade e-boksläsare kan installeras på datorer som körs på Microsoft Windows-baserade system och många överförbara prylar. TR3-filen tillhör gruppen eBook-filer som används i operativsystem som Windows 10, Windows 7, Windows 8/8.1, Windows Vista, Windows XP.

TR3-specifika **HTML-taggar** är följande:

|Tagg|Beskrivning|
---|---|
|\<new> |För att skapa TomeRaider-filer från textfiler är den nya taggen allt som behövs.<new> taggen definierar början på sidorna.|
|\<CATDEF> ... \</CATDEF> |definierar kategorinamnet|
|\<META> ... \</META> |är en tagg som används för att definiera all metadata som används i filformatet. Denna tagg innehåller ett antal parametrar.|
|\<EXPMSG> |Den här taggen styr meddelandet som visas när en fil har upphört att gälla. När en användare försöker visa en sida efter att filen har upphört att gälla, visas meddelandet om utgången i stället för den faktiska sidtexten.|
|\<DIEMSG> |Denna tagg liknar EXPMSG. Den används för att visa ett meddelande när filen dör.|
|\<ENGMSG> |Denna tagg används för att skapa meddelandet som visas för krypterade sidor. Meddelandet visas istället för sidtexten om användaren försöker öppna en krypterad sida innan den låser upp den.|
|\<expmsg> ,\<diemsg> och \<encmsg> |Ignoreras i sidtexten. De måste placeras i filhuvudet före den första<new> tag.|
|\<SELECTION> . \</ SELECTION> |Används för att stödja frågor. Den här taggen måste vara före den första<new> märka. Den sammanställer urvalsdata för användarens fråga.|
|\<catset> . \</catset> | Används för att tilldela kategorinamn för varje ämne.|


## Problem med att öppna en TR3-fil ##

Här är listan över några vanliga problem som kan uppstå och orsaka felfunktion i filformatet:

* Korrupt fil
* Infekterad fil på grund av virus
* Felaktiga länkar till TR3-filen i arkivåtkomster
* Ingen åtkomsträtt i systemet för att öppna filerna
* Föråldrad enhet i ditt system
* Borttagning av rapporten från TR3 från Windows-arkivet
* Att kontakta utvecklaren kan vara ett bättre alternativ för bättre resultat

