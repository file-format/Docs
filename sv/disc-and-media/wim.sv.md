{
  "date" : "2021-08-11",
  "keywords" :[ "wim-fil", "wim-filformat", "vad är en wim-fil", "fil", "wim-exempel", "wim filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om WIM-filformat och API:er som kan skapa och öppna WIM-filer.",
  "title" :"WIM - Windows Imaging Format File",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Vad är en WIM fil?
Filerna med .wim-tillägg sågs första gången i Windows Vista. WIM tillhör ett filbaserat bildformat som vanligtvis introducerades i Microsoft Windows Vista. Det gör att en enda diskavbildning kan distribueras till olika datorplattformar. WIM-filer används för att hantera filer som uppdateringar, drivrutiner och komponenter utan att starta om operativsystemavbildningen. AQ WIM-filen innehåller en uppsättning filer och tillhörande metadata som är mycket lik andra diskfilformat.

## WIM-filformat
WIM-filformatet är inte som sektorbaserade format som VHD eller IS, i själva verket är det ett filbaserat vilket betyder att den grundläggande informationsenheten i en WIM är en fil. Den grundläggande fördelen med att vara filbaserad är att en engångslagring av en fil som refereras flera gånger i filsystemträdet och hårdvaruoberoende. Det minskar kostnaden för att öppna och stänga olika filer individuellt, eftersom filerna lagras i en enda WIM fil. WIM-filer kan lagra flera diskbilder, som refereras antingen av deras unika namn eller med deras numeriska index.
### Stöd för komprimeringsalgoritmer
WIM stöder följande familjer av kompressionsalgoritmer i fallande hastighet och stigande förhållande:
- XPRESS
- LZX
- LZMS
- Solid-kompression.
De tre första familjerna är LZ77-baserade medan Solid-compression introducerades tillsammans med LZMS i WIMGAPI Windows 8 och DISM Windows 8.1.
### Verktyg för WIM-filformat
Följande verktyg stöder vanligtvis WIM-filformatet:

- **ImageX**: Ett kommandoradsverktyg som används för att redigera, skapa och distribuera Windows-diskavbildningar i Windows Imaging Format. Tillsammans med relevant WIMGAPI distribueras den som en del av det kostnadsfria Windows Automated Installation Kit. Från och med Windows Vista använder Windows Setup WAIK API för att installera Windows.
- **DISM**: Ett verktyg som introducerats i Windows 7 och Windows Server 2008 R2 som kan utföra tjänsterelaterade uppgifter på en Windows-installationsavbildning, oavsett om det är en onlinebild eller en offlinebild i en mapp eller WIM-fil. det här verktyget kunde montera och avmontera bilder, lägga till en enhetsdrivrutin till en offlinebild och söka efter installerade drivrutiner i en offlinebild.
 




## Referenser


* [Windows Imaging Format - av Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


