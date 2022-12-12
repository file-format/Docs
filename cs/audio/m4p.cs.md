{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "soubor", "přípona", "formát", "co je formát souboru m4p", "hudba", "formát souboru m4p", "M4b vs MP3", "specifikace formátu souboru m4p"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru M4P a rozhraních API, která mohou vytvářet, převádět a otevírat soubory M4P.",
  "title" :"M4P - Formát souboru audioknihy MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Co je soubor M4P?
Soubor s příponou .m4p je zvukový soubor, který je obvykle k dispozici ke stažení v obchodě Apple iTunes. Jinými slovy můžeme říci, že M4P je soubor AAC, ale chráněný proti kopírování pomocí správy digitálních práv (DRM). To znamená, že soubory M4P lze přehrávat pouze na autorizovaných systémech nebo zařízeních. Soubory M4P jsou obvykle specifické pro multimediální zařízení Apple. Tyto soubory lze tedy přehrávat pouze na macboocích Apple, podcastech a chytrých telefonech, jako je iPhone 6 nebo iPhone 7.

## Formát souboru M4P
M4P je zkratka pro MPEG 4 Protected (audio) a kóduje zvuk pomocí pokročilého zvukového kodeku (AAC) a chrání soubor před neoprávněným použitím souboru. Tento formát souboru je obvykle považován za formát zvukového souboru v iTunes Music Store. Apple používá svůj systém FairPlay Digital Rights Management (DRM) k ochraně souborů M4P. FairPlay DRM je založeno na technologii vyvinuté společností Veridisc. Jeho ochranný mechanismus funguje tak, že zašifruje audio stream AAC pomocí šifrování AES. Uživatel obdrží hlavní klíč, který je přiřazen k jeho účtu pro dešifrování. Tento formát souboru byl zaveden jako náhrada za formát souboru MP3, protože MP3 nebyl původně zamýšlen jako zvukový soubor, ale jako vrstva III ve video souboru MPEG 1 nebo 2.


## Specifikace formátu souboru M4P

Podobně jako u [M4A](/cs/audio/m4a/) se soubory M4P také skládají z po sobě jdoucích bloků. Každý blok má 8bajtové záhlaví a je rozdělen takto:
- Velikost 4bajtového bloku (big-endian, vysoký bajt jako první)
- 4bajtový typ bloku - jeden z předdefinovaných podpisů: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt" ", "ctab", "ssrc".

Podobně jako u M4A bude první blok v M4P typu "ftype" a má podtyp na offsetu 8. M4P definovaný podtypem, který musí být "M4P_".

Opakováním bloků, dokud není detekován blok neznámého typu, vytvoří soubor M4P (MPEG-4 Audio).

## Reference ##

* [MPEG-4 část 14 – Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Formát a příklad obnovení](https://www.file-recovery.com/m4a-signature-format.htm)

