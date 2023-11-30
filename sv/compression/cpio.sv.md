{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO-fil - Unix CPIO-arkivfilformat",
  "description":"Lär dig veta vad en CPIO-fil och API:er är som kan skapa och öppna CPIO-filer.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Vad är en CPIO fil?

En CPIO-fil är en arkivfil som skapats i Unix-formatet Copy In Copy Out (CPIO). Det liknar TAR-filformatet förutom att det är okomprimerat. CPIO-filer kan lagra enhetsfiler, symboliska länkar och utökade filattribut.

## CPIO filformat

Ett CPIO-arkiv skapas som en binär fil som inte är läsbar för människor. Den lagrar samlingen av filer och kataloger. Innehållet i ett CPIO-arkiv identifieras med metadatainformation som filnamn, behörigheter, ägande och tidsstämplar. Denna metadatainformation lagras också i arkivfilen för åtkomst i sidled av systemet.

## Format för CPIO-arkiv

En CPIO-fil består av en eller flera sammanlänkade medlemsfiler. Varje fil i arkivet består av en rubrik som valfritt följs av filinnehållet som nämns i rubriken. Arkivet innehåller en annan rubrik i slutet som beskrivs av en tom fil med namnet TRAILER!!.

### Typer av CPIO-arkiv

Det finns två typer av CPIO-arkiv. Dessa skiljer sig bara i stilen med rubriken.

* ASCII-arkiv - Dessa CPIO-arkiv har en utskrivbar rubrik som blir en del av CPIO-arkivet om själva arkivet består av ASCII-filer
* Binära arkiv - Dessa CPIO-arkiv har binära rubriker.

## Arbetar med CPIO Archive

### Hur skapar man CPIO-arkiv?

Du kan skapa en CPIO på Unix-liknande system med kommandot **cpio**. Följande kommando hittar alla filer och kataloger i den aktuella katalogen och dess underkataloger. Denna utdata skickas sedan till kommandot cpio som kommer att generera ett nytt CPIO-arkiv med namnet archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Hur extraherar man filer från CPIO-arkiv?

Följande kommando extraherar filerna från ett befintligt arkiv.

```
cpio -id < archive_cpio.cpio
```
Den kommer att läsa filen archive.cpio från standardinmatning och extrahera filerna till den aktuella katalogen.


## Referenser

* [CPIO - av Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [CPIO-filformat](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

