{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor CPIO - Formát archivního souboru Unix CPIO",
  "description":"Naučte se vědět, co je soubor CPIO a rozhraní API, která mohou vytvářet a otevírat soubory CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Co je soubor CPIO?

Soubor CPIO je archivní soubor vytvořený ve formátu CPIO (Copy In Copy Out) systému Unix. Je podobný formátu souboru TAR, kromě toho, že je nekomprimovaný. Soubory CPIO mohou ukládat soubory zařízení, symbolické odkazy a rozšířené atributy souborů.

## Formát souboru CPIO

Archiv CPIO je vytvořen jako binární soubor, který není čitelný pro člověka. Ukládá kolekci souborů a adresářů. Obsah archivu CPIO je identifikován informacemi metadat, jako jsou názvy souborů, oprávnění, vlastnictví a časová razítka. Tyto metadatové informace jsou také uloženy v archivním souboru pro boční přístup systému.

## Formát archivu CPIO

Soubor CPIO se skládá z jednoho nebo více zřetězených souborů členů. Každý soubor v archivu se skládá z hlavičky volitelně následované obsahem souboru, jak je uvedeno v hlavičce. Archiv obsahuje na konci další hlavičku, která je popsána prázdným souborem s názvem TRAILER!!.

### Typy archivů CPIO

Existují dva typy archivů CPIO. Tyto se liší pouze stylem záhlaví.

* Archivy ASCII – Tyto archivy CPIO mají tisknutelnou hlavičku, která se stává součástí archivu CPIO, pokud se samotný archiv skládá ze souborů ASCII
* Binární archivy – Tyto archivy CPIO mají binární záhlaví.

## Práce s archivem CPIO

### Jak vytvořit archivy CPIO?

Na systémech podobných Unixu můžete vytvořit CPIO pomocí příkazu **cpio**. Následující příkaz najde všechny soubory a adresáře v aktuálním adresáři a jeho podadresářích. Tento výstup je poté přenesen do příkazu cpio, který vygeneruje nový archiv CPIO s názvem archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Jak extrahovat soubory z archivů CPIO?

Následující příkaz extrahuje soubory z existujícího archivu.

```
cpio -id < archive_cpio.cpio
```
Načte soubor archive.cpio ze standardního vstupu a rozbalí soubory do aktuálního adresáře.


## Reference

* [CPIO – podle Wikipedie](https://en.wikipedia.org/wiki/Cpio)
* [Formát souboru CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

