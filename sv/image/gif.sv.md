{
  "date" : "2019-10-11",
  "keywords" :[ "gif-fil", "gif-filformat", "vad är en gif-fil", "fil", "gif-exempel", "gif-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Bildfilformat",
  "description":"Läs mer om GIF-filformat och API:er som kan skapa och öppna GIF-filer.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en GIF-fil? ##

En GIF eller Graphical Interchange Format är en typ av mycket komprimerad bild. Ägs av Unisys, GIF använder LZW-komprimeringsalgoritmen som inte försämrar bildkvaliteten. För varje bild tillåter GIF vanligtvis upp till 8 bitar per pixel och upp till 256 färger är tillåtna över hela bilden. Till skillnad från en [JPEG](/sv/image/jpeg/)-bild, som kan visa upp till 16 miljoner färger och tämligen tangerar gränserna för det mänskliga ögat. När internet dök upp förblev GIF det bästa valet eftersom de krävde låg bandbredd och kompatibla för grafiken som konsumerar solida färgområden. En animerad GIF kombinerar många bilder eller ramar till en enda fil och visar dem i en sekvens för att generera ett animerat klipp eller en kort video. Färgbegränsningarna är upp till 256 för varje bildruta och är sannolikt den minst lämpade för att återge andra bilder och fotografier med färggradient.

## GIF-filformat ##

Begreppsmässigt har GIF-filer ett grafiskt område med fast storlek fyllt av noll eller fler bilder. Vissa GIF-filer delar upp det grafiska området eller blocken med fast storlek i underbilder som kan fungera som animerade ramar vid animerad GIF. GIF-formatet använder pixeldjupen på 1 till 8 bitar för att lagra bitmappsdata. RGB-färgmodell och palettdata används alltid för att lagra bilderna. Beroende på versionen definierar en rubrik med fast längd ("GIF87a" eller "GIF89a") början på en typisk GIF-fil.

För närvarande finns två versioner av GIF: 87a och 89a tillgängliga. Det förra är det ursprungliga GIF-formatet medan det senare är det nya GIF-formatet. I detta filformat nämns egenskaperna hos blocken och pixeldimensionerna i en logisk skärmbeskrivning med fast längd. Förekomsten och storleken av en global färgtabell kan specificeras av skärmbeskrivningen, som spårar ytterligare detaljer om sådan finns. Trailern är den sista byten i filen som innehåller en enda byte av ett ASCII-semikolon. En typisk GIF87a-fillayout är följande:

### Rubrik ###

Rubriken rymmer sex byte och används för att ange filtypen som GIF. Även om den logiska skärmbeskrivningen är separerad från den faktiska rubriken, betraktas den ibland som den andra rubriken. Samma struktur som används för att lagra rubriken kan lagra den logiska skärmbeskrivningen. Alla GIF-filer börjar med 3-bytesignaturen och använder tecknen "GIF" som identifierare. Versionen är också tre byte stor och deklarerar versionen av GIF-filen.

### Logisk skärmbeskrivning ###

En bildbeskrivning med fast längd anger den skärm- och färginformation som krävs för att skapa GIF-bilden. Fälten Höjd och Bredd omsluter det minsta värdet av skärmupplösning, vilket är obligatoriskt för att visa bilddata. Om visningsenheten inte kan visa den specificerade upplösningen kommer skalning att behövas för att visa bilden på lämpligt sätt. Skärm- och färgkartainformation visas av de fyra underfälten i tabellen nedan (medan bit 0 är den minst signifikanta biten):


|Bits|Underfält
---|---|
|0-2|Storlek på den globala färgtabellen
|3|Färgbordssorteringsflagga
|4-6|Färgupplösning
|7|Global färgtabellsflagga

#### Global färgtabell ####

En valfri global färgtabell placeras precis efter den logiska skärmbeskrivningen. Denna tabell mappas för att indexera pixelfärgdata inuti bilddata. I avsaknad av en global färgtabell använder varje bild i GIF-filen sin lokala färg. Det är bättre att tillhandahålla en standardfärgtabell om både global och lokal färgtabell saknas. En serie av tre-byte trippel komponerar elementen i färgtabellen. Varje byte kännetecknar ett RGB-färgvärde. De röda, gröna och blå färgerna används som värden för varje färgtabellselement. Posterna i den globala färgtabellen träffar maximalt 256 poster och representerar alltid i en potens av två.

#### Bilddata ####

Bilddata lagrar en byte av okodade symboler följt av länkad lista med under- tillsammans med LZW-kodad data.

#### Trailer ####

Trailer representerar en enda byte med data som är det sista tecknet i filen. Värdet på denna byte är permanent 3Bh och anger slutet på dataströmmen. Varje GIF-fil måste ha trailern i den sista av varje fil.

## Referenser ##

* [GIF-filformat](https://en.wikipedia.org/wiki/GIF)

