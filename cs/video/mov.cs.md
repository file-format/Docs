{
  "date" : "2019-10-11",
  "keywords" :[ "soubor mov", "formát souboru mov", "co je soubor mov", "soubor", "příklad mov", "přípona souboru mov", "přípona", "formát", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV File - Apple QuickTime Movie File Format",
  "description":"Další informace o formátu souboru MOV a rozhraních API, která mohou vytvářet a otevírat soubory MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Co je soubor MOV?

Soubor MOV je typ video souboru vyvinutý společností Apple Inc., který obsahuje jednu nebo více stop. Každá stopa ukládá film, zvuk, filmové klipy a titulky. Jedná se o multimediální kontejner, který může ukládat různé typy mediálních prvků. Video formát MOV je kompatibilní se systémy Windows i Macintosh. Pro kompresi používá kódování MPEG-4 a stopy jsou udržovány v objektech nazývaných atomy, které jsou umístěny v hierarchické datové struktuře.

## Stručná historie formátu souboru MOV

Formát souboru MPEG-4 se vyvinul ze specifikace QuickTime File Format (**QTFF**) v roce 2001. Mezinárodní organizace pro normalizaci tento formát schválila a systémové specifikace MPEG-4 Part 1 byly zveřejněny v roce 1999. V roce 2001 byl soubor revize byl publikován formát [MP4](/cs/video/mp4/).

První verze MP4 byla revidována v roce 2003 jako MPEG-4 Part 14 (ISO/IEC 14496-14:2003). V roce 2004 byl MP4 zobecněn, aby definoval obecnou strukturu pro všechny časově založené mediální soubory. Proto se nyní používá jako základ pro různé další formáty multimediálních souborů.

## QuickTime File Format (QTFF) – Další informace

Aby bylo možné pracovat s digitálními multimédii, QTFF pojme mnoho druhů dat. Jde o myšlenkový formát pro výměnu digitálních médií, protože formát definuje standardy pro popis jakéhokoli druhu mediálních struktur. Formát souboru se skládá z flexibilní kolekce objektově orientovaných objektů. Pro ukládání filmů na disky používá QuickTime dvě struktury, tj. `atomy` a `QT atomy`.

### Atomy

Atom je základní jednotkou souboru QuickTime. V každém atomu jsou dvě hlavní pole před jakýmkoli jiným polem: pole Velikost a Typ. Pole velikosti zobrazuje velikost atomu, zatímco pole typu označuje typ dat uložených v atomu. Atomy jsou přirozeně hierarchické, což znamená, že jeden atom může obsahovat další atomy, které mohou stále obsahovat další. Rozložení atomu vzorku je znázorněno na následujícím obrázku.

Každý atom má dvě části, „záhlaví“ a „data“. Hlavička obsahuje pole velikosti a typu a datová část obsahuje skutečná data. Dále je každé pole vysvětleno níže:

### Velikost atomu

Hlavička a obsah atomu jsou označeny 32bitovým celým číslem známým jako velikost atomu. Pole size obsahuje velikost atomu v bajtech, vyjádřenou jako 32bitové celé číslo bez znaménka.

### Typ atomu

Typ atomu je také znázorněn 32bitovým celým číslem, které je většinou považováno za čtyřznakové pole s knemonickou hodnotou, jako je „moov“ (0x6D6F6F76) pro atom filmu nebo „trak“ (0x7472616B) pro dráhový atom. Jakmile je znám typ atomu, umožňuje interpretaci jeho dat.

### QT atomy a atomové kontejnery

Atomy QT poskytují univerzální formát úložiště a mají rozšířenou hlavičku skládající se z polí Size, Type, Atom ID a Count of Child atoms. Atomy QT jsou zabaleny do atomového kontejneru, což je jedinečná datová struktura se záhlavím s počtem zámků. V každém atomovém kontejneru je jeden kořenový atom, což je atom QT. Rozložení atomu QT je znázorněno na obrázku níže.

Záhlaví kontejneru atomu QT obsahuje následující údaje:

Rezervováno: 10bajtový prvek s hodnotou 0.

Lock Count: 16bitové celé číslo s hodnotou 0.

Záhlaví atomů QT mají následující data:

**Velikost -** Záhlaví atomu QT a obsah jsou označeny v bajtech 32bitovým celým číslem. V případě listového atomu pak toto pole obsahuje velikost jednoho atomu.

**Typ -** Typ atomu je označen 32bitovým celým číslem. V případě, že se jedná o kořenový atom, pak je hodnota nastavena na 'sean'.

**Atom ID -** Je to 32bitové celé číslo, které ukazuje ID atomu a musí být jedinečné pro všechny sourozence. Kořenový atom má vždy hodnotu ID atomu 1.

**Rezervováno -** 16bitové celé číslo, které musí být nastaveno na 0.

**Počet dětí -** 16bitové celé číslo, které udává počet podřízených atomů atomu.

**Rezervováno -** 32bitové celé číslo, které musí být nastaveno na 0.

## Struktura souborů MOV souborů

Soubory MOV se skládají z po sobě jdoucích částí. Každý chunk má 8bajtové záhlaví: 4bajtová velikost chunku (big-endian, high byte first) a 4bajtový typ chunk – jeden z předdefinovaných podpisů: „ftyp“, „mdat“, „moov“, „pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". První chunk je typu "ftype" a má podtyp na offsetu 8. MOV definovaný podtypem, který musí být "qt". Chcete-li sestavit soubor MOV, je potřeba iterovat bloky, dokud není detekován neznámý typ.

Zde je „ukázkový příklad“: Při kontrole binárních dat ukázkového souboru MOV je zřejmé, že začíná podpisem **ftyp** (hex: 66 74 79 70) na offsetu 4, který definuje typ souboru QuickTime Container. Podtyp souboru je **qt~_~_** (hex: 71 74 20 20), což ukazuje na typ souboru MOV. Velikost prvního bloku je 32 (hex: 00 00 00 20, big-endian, první vysoký byte), velikost umístěná na offsetu 0. Na offsetu 32 (hex: 20) je umístěn druhý blok, který má velikost 8 a zadejte **mdat** (hex: 6D 64 61 74).

Další blok se nachází na offsetu 32+8#40 (hex: 28) a má velikost 3 263 028 (hex: 00 31 CA 34) a typ **mdat** (hex: 6D 64 61 74) na offsetu 44 (hex. : 2C). Další blok se nachází na offsetu 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) a má velikost 21,189 (hex: 00 00 52 C5) a typ **moov** (hex: 6D 6F) na offset 6F 76 1,836,019,574 (hex: 00 31 CA 60). Toto je poslední blok, takže celková velikost souboru je 3 263 068 + 21 189 # 3 284 257 bajtů.

## Jak převést soubor MOV?

K dispozici je spousta přehrávačů médií a softwarových video editorů pro převod souborů MOV do jiných populárních formátů video souborů. Některé z přehrávačů médií, které mohou převádět soubory MOV do jiných formátů, zahrnují:

* Přehrávač médií VideoLAN VLC
* Eltima Elmedia Player

Několik přehrávačů médií a editorů videa, včetně přehrávače médií VideoLAN VLC a Eltima Elmedia Player, může převádět soubory MOV do jiných formátů. Tento software dokáže převést soubory MOV do následujících video formátů.

* Video MPEG-4 – [MP4](/cs/video/mp4/)
* WebM Video – [WEBM](/cs/video/webm/)
* Video Transport Stream – [TS](/cs/video/ts/)
* Formát pokročilého systému – [ASF](/cs/video/ts/)
* Ogg Vorbis Audio – [OGG](/cs/audio/ogg/)
* Audio MP3 – [MP3](/cs/audio/mp3/)
* Bezeztrátový zvukový kodek – [FLAC](/cs/audio/flac/)
* WAVE Audio – [WAV](/cs/audio/wav/)

## Open Source API pro soubory MOV

* [React Native API pro převod MOV na MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API pro opravu souborů MOV](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API pro převod MOV na GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Reference

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

