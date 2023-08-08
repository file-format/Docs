{
  "date" : "2021-08-23",
  "keywords" :[ "img-fil", "img-filformat", "vad är en img-fil", "fil", "img-exempel", "img-filtillägg", "tillägg", "format", "filformat för img", "diskavbildning" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om IMG-filformat och API:er som kan skapa och öppna IMG-filer.",
  "title" :"IMG - Disk Image File Format",
  "linktitle" : "IMG",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-img",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-23"
}

## Vad är en IMG fil?

Inom datorområdet hanterar filerna med .img-filtillägg lagring av rådiskbilder av diskar som disketter, hårddiskar eller optiska skivor etc. Denna råbild består av en binär bild av källan med specifikationer för sektor för sektor.

Innehållet i IMG-filformatet är beroende av filsystemet på skivan som anges för skapandet av bilden. När det gäller CD-ROM och DVD-skivor innehåller bilderna av dessa filer data från motsvarande sektorer tillsammans med kontrollrubriker och fält för felkorrigering enligt varje sektor.

IMG-filerna har specificerat innehåll för disken, så dessa är kompatibla med de specifika program som är lämpliga för att detektera deras filsystem.

## IMG-filformat ##

Under åren då en diskett användes för lagringsändamål och hantering av datalagring, utvecklades dessa filer för att komma åt diskens råa bilder. Många program hänvisades av IMG-filerna. Dessa skapades av diskavbildningsprogram. I Windows-operativsystemprogram som ström, används en mjukvarubrännare för att hantera dessa filer.

## Teknisk specifikation ##

Det finns andra filtillägg som IMA och IMZ som liknar detta filformat. Storleken på dessa bilder är alltid i form av flera olika sektorstorlekar. Denna storlek är 512 byte för disketter och hårddiskar. Sektorns råa storlek är 2 352 för CD-rom och DVD-skivor. Storleken på den råa skivavbildningen är multipel av denna storlek.

Detta format används mest med program som RawWrite och WinImage. Dessa program använder detta format för att läsa och skriva bilder på disketter. Dessutom kan dessa filer konverteras till andra mer populära filformat genom att använda vissa program som PowerISO.

Eftersom IMG-filer inte har några tillagda data förutom innehållet på skivorna, kan dessa IMG-filer bara hanteras av programmen automatiskt och upptäcka filsystemen. Till exempel, en vanlig diskbild av en rå diskett börjar med startsektorn för FAT och kan användas för att identifiera filsystemet.

Optiska medias skivbilder åtföljs oftast av deskriptorfilen. Den förklarar skivlayouten och involverar information som spårgränser och dessa lagras inte bara i en bildfil i rå form.



## Referenser ##

* [IMG - av Wikipedia](https://en.wikipedia.org/wiki/IMG_(file_format))


