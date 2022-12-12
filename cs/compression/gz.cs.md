{
  "date" : "2019-10-11",
  "keywords" :[ "soubor gz", "formát souboru gz", "co je soubor gz", "soubor", "příklad gz", "přípona souboru gz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru GZ - archivní soubor GNU ZIP",
  "description":"Zjistěte, co je soubor GZ a rozhraní API, která mohou vytvářet a otevírat soubory GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GZ?

Soubor GZ je komprimovaný archiv, který je vytvořen pomocí standardního kompresního algoritmu [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Může obsahovat více komprimovaných souborů, adresářů a útržků souborů. Tento formát byl původně vyvinut, aby nahradil kompresní formáty v systémech UNIX. a stále je jedním z nejběžnějších typů archivů na systémech Linux. Aplikace jako [WinZip](https://www.winzip.com/en/) mohou otevírat soubory GZ a zobrazovat jejich obsah v systémech Windows i MacOS.

## Formát souboru GZ - Další informace

Gzip používá pro kompresi archivu algoritmus [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) a liší se od formátu archivu [ZIP](/cs/compression/zip/) v použití kompresního algoritmu na celý archiv spíše než jednotlivé soubory. Specifikace formátu souboru GZIP verze 4.3 publikované organizací Internet Engineering Task Force (IETF) obsahují podrobné informace o formátu souboru. Formát souboru se skládá z:

* Záhlaví souboru
* Volitelné záhlaví
* Komprimovaná data
* Zápatí souboru

## Záhlaví souboru GZ ##

Záhlaví souboru GZ se skládá z 10 bajtů takto:

|Offset|Velikost|Hodnota|Popis
---|---|---|---|
|0|2|0x1f 0x8b|Magické číslo identifikující typ souboru
|2|1| |Metoda komprese * 0-7 (rezervováno) * 8 (vypuštění)
|3|1| |Vlajky souborů
|4|4| |32bitové časové razítko
|8|1| | Kompresní příznaky
|9|1| |ID operačního systému

### Příznaky souboru ###

|Hodnota|Identifikátor|Popis
---|---|---|
|0x01|FTEXT|Pokud je nastaveno, nekomprimovaná data musí být považována za text namísto binárních dat. Tento příznak naznačuje převod na konci řádku pro textové soubory napříč platformami, ale nevynucuje jej.
|0x02|FHCRC|Soubor obsahuje kontrolní součet záhlaví (CRC-16)
|0x04|FEXTRA|Soubor obsahuje další pole
|0x08|FNAME|Soubor obsahuje původní řetězec názvu souboru
|0x10|FCOMMENT|Soubor obsahuje komentář
|0x20| |Rezervováno
|0x40| |Rezervováno
|0x80| |Rezervováno

### Operační systém ###

|Hodnota|Popis
---|---|
|0|Souborový systém FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (nebo OpenVMS)
|3|Unix
|4|VM/CMS
|5|TOS Atari
|6|Souborový systém HPFS (OS/2, NT)
|7|Macintosh
|8|Systém Z
|9|CP/M
|10|TOPS-20
|11|Souborový systém NTFS (NT)
|12|QDOS
|13|Žalud Riscos
|255|neznámý

## GZ volitelná záhlaví ##

Volitelná další záhlaví jsou ta, která jsou označena příznakem souboru a zahrnují informace, jako je původní název souboru, další pole, komentáře a kontrolní součet záhlaví.

## Komprimovaná data ##

Tato část obsahuje komprimovaná data pomocí kompresního algoritmu DEFLATE.

## Zápatí souboru GZ ##

Zápatí souboru má velikost 8 bajtů a obsahuje následující informace.

|Odsazení|Velikost|Popis
---|---|---|
|0|4|Kontrolní součet (CRC-32)
|4|4|Hodnota velikosti nekomprimovaných dat v bajtech

## Reference ##

* [gzip – Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: Specifikace formátu souboru GZIP] (http://tools.ietf.org/html/rfc1952), od IETF.

