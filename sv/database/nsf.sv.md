{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om NSF-filformat och API:er som kan skapa och öppna NSF-filer.",
  "title" :"NSF-filformat - Lotus Notes-databasformat",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är NSF fil?

En fil med tillägget .nsf (Notes Storage Facility) är ett databasfilformat som används av [IBM Notes-programvaran](https://en.wikipedia.org/wiki/HCL_Domino), som tidigare var känt som Lotus Notes. Det definierar schemat för att lagra olika typer av objekt som e-postmeddelanden, möten, dokument, formulär och vyer. All denna information finns i en enda NSF-fil för affärssamarbete som liknar en PST/OST-fil. Några av de program som kan öppna NSF-filer inkluderar IBM Lotus Notes och IBM Domino.

## NSF filformatspecifikationer

NSF-filer är binära till sin natur och deras specifikationer är tillgängliga av Joachim Metz på [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Enligt dessa detaljer består en NSF-fil av:

* Filhuvud
* Databashuvud

Dessutom består den av:

* Superblock
* Bucket descriptor block
* Bitmapp
* Record Relocation Vector hink
* Sammanfattning hinkar
* Icke-sammanfattande hinkar


### NSF-filhuvud

NSF-filhuvudet är 6 byte stort. Den består av:

|Offset|Storlek|Värde|Beskrivning|
---|---|---|---|
0|2|0x1a 0x00|Signatur|
2|4| |Databashuvudets storlek|

### Databashuvud

NSD-databashuvudet innehåller följande bekräftade värden.

* Databasinformation
* Databasidentifierare (DBID)
* Replikeringsinformation
* Databasinformationsbuffertflaggor
* Titel
* Kategorier
* Klass
* Designklass (mallnamn)
* Särskilda anteckningsidentifierare
* Vaddering
* Databasinformation 2
* Databasinformation 3
* Databasinformation 4
* Databasinformation 5
* Vaddering
* Databasinstansidentifierare (DBIID)
* Replikeringshistorik

## Referenser

* [NSF-format - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

