{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "soubor", "přípona", "formát", "co je formát souboru m4a", "hudba", "formát souboru m4a", "M4A vs MP3", "specifikace formátu souboru m4a"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru M4A a rozhraních API, která mohou vytvářet, převádět a otevírat soubory M4A.",
  "title" :"M4A - MPEG-4 Audio File",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Co je soubor M4A?

Formát souboru **M4A** je zvukový soubor vytvořený pomocí AAC (Advanced Audio Coding), který je známý jako ztrátová komprese. Slovo M4A zkráceně MPEG 4 Audio. Tyto zvukové soubory mají obvykle příponu .m4a. To platí zejména pro nechráněný obsah. Může ukládat různé typy zvukového obsahu, jako jsou audioknihy, písně a podcasty. M4A je obvykle realizován jako pokročilejší formát než MP3, který nebyl typicky navržen pouze pro zvuk. Je to pouze zvuková vrstva ve video souborech MPEG 1 nebo 2.

Formát M4A je zašifrován FairPlay Digital Rights Management, jak byly prodávány prostřednictvím iTunes Store, používající příponu .m4p. Apple iPhone používá pro své vyzváněcí tóny zvuk MPEG-4, ale tyto zvukové soubory používají příponu .m4r.


## M4A vs MP3

M4A i [MP3](https://docs.fileformat.com/audio/mp3/) jsou pouze zvukové formáty souborů.

**M4A**: Lepší než MP3, pokud jde o kvalitu a velikost při kódování při stejné přenosové rychlosti. Přípona souboru .m4a je tak běžná, protože ji Apple používal pro použití v iTunes Music Store. M4A je zvukový soubor, který je komprimován pomocí technologie MPEG-4; algoritmus pro ztrátovou kompresi. V zásadě je spojena s „MPEG-4 Audio Layer“, soubory s příponou .m4a jsou zvukovou vrstvou filmů MPEG-4. Má předběhnout MP3 a stát se novým standardem v kompresi zvuku. V mnoha ohledech se velmi blíží MP3, ale byl představen proto, aby měl lepší kvalitu při stejné nebo dokonce menší velikosti souboru. Formát M4A byl poprvé představen společností Apple. Typ formátu je také realizován jako Apple Lossless Encoder (ALE).

Proto v současné době M4A nemohl získat hlavní úspěch MP3, protože zvukový formát ještě není obecně hratelný. Je nějak omezena pouze na MacOS, iPod a další produkty Apple.

**Mp3**: Nejznámější formát digitálního zvuku. Byl to také jeden z prvních kompresních formátů na scéně a stal se velmi oblíbeným mezi milovníky hudby. Jeho mainstreamový úspěch je tak rychlý, že tento typ souboru je možné přehrát univerzálně a téměř s čímkoli, s hardwarem nebo softwarem. V obecném smyslu bude M4A produkovat lepší kvalitu zvuku, ale mnozí by tvrdili, že ať už je to pravda nebo ne, rozdíl ve zvuku není rozpoznatelný a bylo by ztrátou času zkoušet převádět soubory MP3 na soubory M4A. Konverze nakonec způsobí, že ztratíte původní kvalitu zvuku.

## Specifikace formátu souboru M4A

Soubory M4A se skládají z po sobě jdoucích částí. Každý blok má 8bajtové záhlaví a je rozdělen takto:
- Velikost 4bajtového bloku (big-endian, vysoký bajt jako první)
- 4bajtový typ bloku - jeden z předdefinovaných podpisů: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

První blok bude typu "ftype" a má podtyp na offsetu 8. M4A definovaný podtypem, který musí být "M4A_", pro podtyp M4B musí být "M4B_" a pro podtyp M4P musí být "M4P_".

Opakováním bloků, dokud není detekován blok neznámého typu, vytvoří soubor M4A (MPEG-4 Audio).

## Reference ##

* [MPEG-4 část 14 – Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Formát a příklad obnovení](https://www.file-recovery.com/m4a-signature-format.htm)

