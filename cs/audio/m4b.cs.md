{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "soubor", "přípona", "formát", "co je formát souboru m4b", "hudba", "formát souboru m4b", "M4b vs MP3", "specifikace formátu souboru m4b"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů M4B a rozhraních API, která mohou vytvářet, převádět a otevírat soubory M4B.",
  "title" :"M4B - Formát souboru audioknihy MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Co je soubor M4B?

Soubor s příponou .m4b je audiokniha obecně používaná knihami Apple a iTunes. Zvuk použitý v tomto formátu je uložen v MPEG-4 a komprimován pomocí kódování AAC. Soubor M4B je velmi podobný souboru M4A, ale podporuje funkce související s audioknihou, jako jsou záložky a konce kapitol. Soubory M4B jsou k dispozici ve verzi s povolenou DRM i bez DRM. Audioknihy zašifrované DRM jsou obvykle placené audioknihy z iTunes Store. Zatímco DRM zdarma lze najít snadno přes internet.

## Formát souboru M4B

Soubory audioknih obsahující metadata, obrázky, záložky a hypertextové odkazy lze uložit s příponou .m4a, ale obecně se při ukládání používá přípona .m4b, jen pro určení, že soubor má formát souboru audioknihy. Fairplay DRM (Digital Rights Management) používá aplikace k ochraně svých souborů M4B. Takže soubory stažené z iTunes lze přehrávat pouze na autorizovaných zařízeních nebo počítačích.


## M4B vs M4A

M4B i [MP3](/audio/mp3/) jsou pouze zvukové formáty souborů.

**M4B**: Zvítězí ve srovnání s MP3, pokud jde o kvalitu, pokud oba kódujete při stejné přenosové rychlosti. M4B je soubor audioknihy, který je komprimován pomocí kódování AAC. V zásadě je spojena s „MPEG-4 Audio Layer“, soubory s příponou .m4b jsou zvukovou vrstvou filmů MPEG-4, ale s dalšími funkcemi souvisejícími s audioknihami. Jeho cílem je předběhnout MP3 a stát se novým standardem v kompresi zvuku. V mnoha ohledech je velmi blízký MP3, ale byl vyvinut tak, aby měl lepší kvalitu při stejné nebo dokonce menší velikosti souboru. Formát M4B byl poprvé představen společností Apple. Typ formátu je také realizován jako Apple Lossless Encoder (ALE).

Proto v současné době M4B nemohlo dosáhnout hlavního proudu MP3 úspěchu, protože zvukový formát ještě není běžně hratelný.

**Mp3**: Digitální audio formát, který je všem dobře znám. Úplně první kompresní formát na scéně a stal se velmi známým mezi hudebními posluchači. Jeho mainstreamový úspěch je tak rychlý, že tento typ souboru je možné přehrávat univerzálně a je kompatibilní téměř s čímkoli, s hardwarem nebo softwarem. V obecném smyslu bude M4A produkovat lepší kvalitu zvuku, ale mnozí by tvrdili, že ať už je to pravda nebo ne, rozdíl ve zvuku není srovnatelný a bylo by ztrátou času zkoušet převádět soubory MP3 na soubory M4A. Konverze nakonec způsobí, že ztratíte původní kvalitu zvuku.

## Specifikace formátu souboru M4B

Podobně jako u [M4A](/cs/audio/m4a/) se soubory M4B také skládají z po sobě jdoucích bloků. Každý blok má 8bajtové záhlaví a je rozdělen takto:
- Velikost 4bajtového bloku (big-endian, vysoký bajt jako první)
- 4bajtový typ bloku - jeden z předdefinovaných podpisů: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT" ", "scpt", "ssrc".

Podobně jako M4A bude první blok v M4B typu "ftype" a má podtyp na offsetu 8. M4B je definován podtypem, který musí být "M4B_".

Opakováním bloků, dokud není detekován blok neznámého typu, vytvoří soubor M4B (MPEG-4 Audio).

## Reference

* [MPEG-4 část 14 – Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Formát a příklad obnovení](https://www.file-recovery.com/m4a-signature-format.htm)

