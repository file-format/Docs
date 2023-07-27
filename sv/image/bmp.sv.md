{
  "date" : "2019-10-11",
  "keywords" :[ "bmp-fil", "bmp-filformat", "vad är en bmp-fil", "fil", "bmp-exempel", "bmp-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Bildfilformat",
  "description":"Läs mer om BMP-filformat och API:er som kan skapa och öppna BMP-filer.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Vad är en BMP-fil? #

Filer med tillägget .BMP representerar bitmappsbildfiler som används för att lagra digitala bitmappsbilder. Dessa bilder är oberoende av grafikkort och kallas även enhetsoberoende bitmappsfilformat (DIB). Detta oberoende tjänar syftet att öppna filen på flera plattformar som Microsoft Windows och Mac. BMP-filformatet kan lagra data som tvådimensionella digitala bilder i både svartvitt och färgformat med olika färgdjup.

## BMP-filformatspecifikationer ##

Enhetsoberoende bitmappar fungerar som ett hjälpmedel för att utbyta bitmappar mellan enheter och applikationer. På grund av den kontinuerliga utvecklingen av detta filformat kan informationen i rubrikerna skilja sig från versionen av Bitmap. En enda bitmappsfil består av fasta såväl som strukturer av variabel storlek i en specifik sekvens.

Strukturer i en bitmappsfil är ordnade i följande ordning:


|Struktur|Valfritt|Storlek|Syfte
---|---|---|---|
|File Header|No|14|För att lagra allmän information om bitmappsbildfilen
|DIB Header|No|Fixed-Size|För att lagra detaljerad information om bitmappsbilden och definiera pixelformatet
|Extra bitmasker|Ja|12 eller 16 byte|För att definiera pixelformatet
|Färgpalett|Halvvalfritt|Variabel storlek|För att definiera färger som används av bitmappsbilddata
|Gap1|Ja|Variabel storlek|Strukturjustering
|Pixel Array|No|Variabelstorlek|Pixelformat definieras av DIB-huvudet eller extra bitmasker.
|Gap2|Ja|Variabel storlek|Strukturjustering
|ICC Färgprofil|Ja|Variabel storlek|För att definiera färgprofilen för färghantering

När en bitmappsbild läses in i minnet blir den en DIB-struktur, som används av Windows via dess GDI API. Filhuvudet är inte en del av denna datastruktur. Färgen kan också bestå av 16-bitars poster som utgör index till den för närvarande refererade paletten istället för explicita RGB-färgdefinitioner. Låt oss ta en titt på några av dessa i detalj, särskilt rubrikerna.

### Bitmap File Header ###

En bitmappsfilrubrik liknar andra filrubriker som används för att identifiera filen. Eftersom det finns olika varianter av BMP-filformat är de första 2 byten av BMP-filformatet tecken "B" och sedan tecken "M" i ASCII-kodning. Alla heltalsvärden lagras i little-endian-format.

|Offset hex|Offset dec|Storlek|Syfte
---|---|---|---|
|00|0|2 bytes|Rubrikfältet som används för att identifiera BMP- och DIB-filen är 0x42 0x4D i hexadecimal, samma som BM i ASCII. Det kan följa möjliga värden.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2-struktur bitmappsmatris * **CI** – OS/2-struktur färgikon * **CP** – OS/2-konst färgpekare * **IC** – OS/2-strukturikon * **PT** – OS/2-pekare
|02|2|4 byte|Storleken på BMP-filen i byte
|06|6|2 byte|Reserverad; Det faktiska värdet beror på applikationen som skapar bilden
|08|8|2 byte|Reserverad; Det faktiska värdet beror på applikationen som skapar bilden
|0A|10|4 bytes|Offset, dvs startadressen, för byten där bitmappsbilddata (pixel array) kan hittas.

#### DIB-huvud (bitmappsinformationshuvud) ####

Den detaljerade informationen om bilden representeras av denna rubrik. Baserat på denna information kommer applikationen att fastställas som kommer att användas för att visa bilden på skärmen. Alla sådana rubriker innehåller ett DWORD-fält (32-bitars) som anger deras storlek, så att ett program enkelt kan bestämma rubriken som används i bilden. Detta beror i grunden på att DIB-formatet genomgick flera förlängningar. Följande är DIB Header med listade fält.

#### Färgpalett ####

En BMP-färgpalett är en rad strukturer som anger RGB-intensitetsvärdena för varje färg i en bildskärmsenhets färgpalett. Varje pixel i bitmappsdata lagrar ett enda värde som används som ett index i färgpaletten. Färginformationen som lagras i elementet vid det indexet anger färgen på den pixeln. Tillgängligheten av färg i en bitmappsfil varierar enligt följande:

* En, 4 och 8-bitars - förväntas alltid innehålla en färgpalett
* Sexton, 24 och 32-bitars - innehåller aldrig färgpaletter
* Sexton och 32-bitars BMP-filer - innehåller bitfältsmaskvärden istället för färgpaletten

#### Pixellagring ####

Bitmappspixlar lagras som bitar packade i rader där storleken på varje rad avrundas uppåt till en multipel av 4 byte (ett 32-bitars DWORD) genom utfyllnad. Den totala mängden byte som krävs för att lagra pixlarna i en bild kan inte direkt beräknas genom att bara räkna bitarna. Eftersom det är utfyllnad krävs effekten av att runda upp storleken på varje rad till en multipel av 4 byte. Utfyllnadsbytes (inte nödvändigtvis 0) ska läggas till i slutet av raderna för att få upp längden på raderna till en multipel av fyra byte. När pixelmatrisen laddas in i minnet måste varje rad börja på en minnesadress som är en multipel av 4.

Bilden beskrivs faktiskt av 32-bitars DWORDs representation av pixelmatrisen. Vanligtvis lagras pixlar "nedifrån och upp", med början i det nedre vänstra hörnet, från vänster till höger och sedan rad för rad från botten till toppen av bilden. Pixelformat och deras konsekvenser är enligt nedan:

* Formatet 1 bit per pixel (1 bpp) stöder 2 distinkta färger (till exempel: svart och vitt).
* Formatet 2-bitar per pixel (2bpp) stöder 4 distinkta färger och lagrar 4 pixlar per 1 byte, den längst till vänster är i de två mest signifikanta bitarna. Varje pixelvärde är ett 2-bitars index i en tabell med upp till 4 färger.
* 4-bitars per pixel (4bpp)-formatet stöder 16 distinkta färger och lagrar 2 pixlar per 1 byte, den längst till vänster är i den mer signifikanta biten. Varje pixelvärde är ett 4-bitars index i en tabell med upp till 16 färger.
* Formatet 8-bitar per pixel (8bpp) stöder 256 distinkta färger och lagrar 1 pixel per 1 byte. Varje byte är ett index i en tabell med upp till 256 färger.
* Formatet 16-bitar per pixel (16bpp) stöder 65536 distinkta färger och lagrar 1 pixel per 2-byte WORD. Varje ORD kan definiera alfa, röda, gröna och blå prover av pixeln.
* 24-bitars pixelformat (24bpp) stöder 16 777 216 distinkta färger och lagrar 1 pixelvärde per 3 byte. Varje pixelvärde definierar de röda, gröna och blå proverna av pixeln (8.8.8.0.0 i RGBAX-notation). Specifikt i ordningen: blå, grön och röd (8 bitar per varje prov).
* Formatet 32-bitar per pixel (32bpp) stöder 4 294 967 296 distinkta färger och lagrar 1 pixel per 4-byte DWORD. Varje DWORD kan definiera alfa, röda, gröna och blå prover av pixeln.

## Referenser ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP-filformat](https://en.wikipedia.org/wiki/BMP_file_format)

