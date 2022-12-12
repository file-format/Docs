{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Formát souboru obrazu disku",
  "description":"Co je soubor ISO a rozhraní API, která mohou vytvářet a otevírat soubory ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Co je soubor ISO?

Soubor s příponou .iso je nekomprimovaný archivní obraz disku, který představuje obsah celých dat na optickém disku, jako je CD nebo DVD. Na základě standardu [ISO-9660](https://www.iso.org/standard/17505.html) obsahuje formát souboru obrazu ISO data disku spolu s informacemi o systému souborů, které jsou na něm uloženy. Schopnost souborů ISO obsahovat přesnou repliku obsahu z něj činí dokonalý typ souboru pro vytváření kopií disků CD/DVD a většinou se používají k ukládání zaváděcích dat pro instalaci. Soubory ISO jsou ve většině případů vypáleny na USB/CD/DVD jako spouštěcí obsah pro spuštění počítače za účelem instalace. Soubory ISO mají typ MIME application/x-iso9660-image.

## Formát souboru ISO

Formát souboru ISO není jako jiné formáty souborů kontejneru, i když archivuje zadaný obsah dat. Archiv je vytvořen jako binární soubor s přesnou strukturou obsahu a informacemi o souborovém systému. Formát souboru ISO je popsán v [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) následovně.

### Struktura souboru ISO nejvyšší úrovně

Celková struktura souboru se skládá z:

* "Systémová oblast" - 32 768 bajtů a ISO_9660 ji nepoužívá
* `Data Area` - skládá se ze sady deskriptorů svazku a tabulek cest, adresářů a souborů

### Sada deskriptorů svazku

Datová oblast začíná sadou deskriptorů svazku, sadou jednoho nebo více deskriptorů svazku zakončenou terminátorem sady deskriptorů svazku. Ty společně fungují jako hlavička pro datovou oblast popisující její obsah (podobně jako blok parametrů BIOS používaný u disků s formátem FAT, HPFS a NTFS).

Sada deskriptorů objemu je znázorněna níže.

|Sada deskriptorů hlasitosti|
---|
|Deskriptor svazku #1|
|...|
|Deskriptor svazku #N|
|Ukončení sady deskriptoru hlasitosti|

#### Deskriptor svazku

Každý deskriptor svazku má velikost 2048 bajtů a má následující strukturu:

|Část |Typ |Identifikátor |Verze |Data|
---|---|---|---|---|
|Velikost |1 bajt |5 bajtů (vždy 'CD001') |1 bajt (vždy 0x01) |2 041 bajtů|

## Reference

* [Obrázek optického disku – Wikipedie](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Podpisy souborů](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 – Wikipedie](https://en.wikipedia.org/wiki/ISO_9660)

