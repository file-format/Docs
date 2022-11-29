{
  "date" : "2021-06-22",
  "keywords" :[ "Z", "Komprimerad", "Fil", "Tillägg", "Filformat", "UNIX", "Kartz" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Z komprimerat filformat",
  "description":"Läs mer om Z-filformat och API:er som kan skapa och öppna Z-filer.",
  "linktitle" : "Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-22"
}

## Vad är en Z-fil? ##

AZ-fil är en kategori av filer som tillhör UNIX-komprimerade datafiler. Komprimerade Unix-filer är den mest populära och mest använda förlängningstypen av Z-filen. Z-fil gör formatering, körning och öppning av filer enklare eftersom de används för att skapa små datorfiler som enkelt kan köras på Linux/Unix operativsystem. Det är fördelaktigt för användare som vill spara diskutrymme, eftersom genom att komprimera stora filer till en Z-fil kan användare spara mycket lagringsutrymme och göra sina filer mer organiserade. Dessa komprimerade Z-filer kan enkelt dekomprimeras i Unix-systemet genom att använda ett enkelt kommando "uncompress abc.z" för en fil som heter "abc".


## Kortfattad bakgrund ##

Z-filen skapades som ett resultat av en orubblig efterfrågan på en snabb arkivering i slutet av 80-talet och början av 90-talet. Eftersom internet inte var särskilt populärt och tillgängligt vid den tiden, var användarna tvungna att kämpa för att dela grundläggande filer och komma åt internet. Ett sådant sätt som användare använde för att överföra filer var att använda en arkivering. Z-filen introducerades av Phil Katz, som en snabbare och mer stödjande form av Archiver, genom vilken enorma filer kunde komprimeras i en och överföras. Den slutliga versionen av Kartz introducerades 1989, efter en juridisk strid, och den var tillägnad det offentliga området, som tillkännagavs av Kartz.


## Teknisk specifikation ##

Z-filen är en fil som stöder arkivfilformatet. Det är en av de första filtyperna som ger snabb och förlustfri datakomprimering och dekomprimering med Unix- och Linux-operativsystemen. I vissa operativsystem representerar ett filtillägg med gemener Z (.z) en GNU-komprimerad fil, medan en fil med versaler Z (.Z) representerar en komprimerad fil. Z-filen har flera versioner som den stöder, till exempel 2.0, 2.1, 4.5, 4.6, bland annat. Det finns olika algoritmer i olika Z-filversioner, och den mest populära är DEFLATE.




