{
  "date" : "2021-09-08",
  "keywords" :[ "gam-fil", "gam-filformat", "vad är en gam-fil", "fil", "gam-exempel", "gam-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om GAM-filformat och API:er som kan skapa och öppna GAM-filer.",
  "title" :"GAM - Sparad spelfil",
  "linktitle" : "GAM",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är en GAM fil?
En fil med filtillägget .gam används av olika videospel för att få spelarna att fortsätta där de slutade nästa gång programmet öppnas. Därför betyder det att GAM-filen sparar informationen om vad en användare har gjort vid vilken tidpunkt. Dessa filer kan sparas automatiskt av spelmjukvaran eller så kan spelarna bli ombedda att spara om de vill fortsätta med spelets tillstånd där de lämnar.
## GAM filformat
GAM-filformat används i princip för att lagra speldata i sparade spel. GAM-filen lagrar inte varelse, föremålsinformation eller område, istället sparar den data om partimedlemmarna och de allmänna eller globala variablerna som påverkar partimedlemmarna.
### GAM-filens struktur
GAM-filen har följande struktur:
- Header
– Partimedlemmar
- Partimedlem CRE-fildata
- NPC:er (som inte är med i sällskapet)
- NPC dödar statistik (inbäddad i NPC-struktur)
- NPC CRE-fildata
- Variabler (i det GLOBALA namnutrymmet)
- Journalanteckningar
- Bekant information
- Lagrade platser
- Pocket Plane Locations
- Bekant extra


 




## Referenser


* [GAM-filformat](https://gibberlings3.github.io/iesdp/file_formats/ie_formats/gam_v2.0.htm#GAMEV2_0_Stored)


