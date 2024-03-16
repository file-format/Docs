{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru QT - soubor rychlého filmu",
  "keywords" :[ "QT", "Video QuickTime", "formát qt", "jak přehrávat soubory qt", "Soubor rychlého filmu", "QTFF", "video", "Apple" ],
  "description":"Další informace o formátu souborů QT a rozhraních API, která mohou vytvářet a otevírat soubory QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Co je soubor QT?

Soubor s příponou .qt je soubor multimediálního kontejneru, který používá framework QuickTime k ukládání obsahu multimediálních souborů. QuickTime File Format (QTFF) vyvinutý společností Apple Inc. je multimediální kontejnerový soubor, který obsahuje zvuk, video nebo text pro pozdější přehrávání. Je to formát volby pro výměnu digitálních médií mezi zařízeními, aplikacemi a operačními systémy. Soubory QT se také ukládají ve formátu [MOV](/cs/video/mov/), který byl také vyvinut společností Apple Inc. Některé z aplikací, které mohou otevírat soubory QT, zahrnují přehrávač Apple QuickTime, přehrávač médií VLC a Media Player Classic s K- Balíček Lite Codec Pack.

## Formát souboru QT

QTFF je objektově orientovaný, který odhaluje flexibilní kolekci objektů pro snadnou analýzu a rozšiřování. Každá stopa v souboru QT obsahuje digitálně kódovaný mediální tok nebo datový odkaz na mediální tok umístěný v jiném souboru. Hierarchická datová struktura sestávající z objektů nazývaných atomy funguje jako kontejnery stop. Specifikace formátu souboru pro [formát souboru QT](https://developer.apple.com/documentation/quicktime-file-format) jsou oficiálně dostupné společností Apple Inc.

### Popis média

Popis média souboru QuickTime je uložen odděleně od dat média. Informace, jako je počet stop, formát komprese videa a informace o časování, jsou uloženy v popisu média (také známého jako filmový zdroj, atom filmu nebo jednoduše film). Na data médií se v této struktuře médií odkazuje index. Mediální data jsou skutečná ukázková data, jako jsou snímky videa a audio ukázky, použité ve filmu.

### Atomy

Atom je základní jednotkou souboru QuickTime. V každém atomu jsou dvě hlavní pole před jakýmkoli jiným polem: pole Velikost a Typ. Pole velikosti zobrazuje velikost atomu, zatímco pole typu označuje typ dat uložených v atomu. Atomy jsou přirozeně hierarchické, což znamená, že jeden atom může obsahovat další atomy, které mohou stále obsahovat další. Rozložení atomu vzorku je znázorněno na následujícím obrázku.

Každý atom má dvě části, záhlaví a data. Hlavička obsahuje pole velikosti a typu a datová část obsahuje skutečná data. Dále je každé pole vysvětleno níže:

#### Velikost atomu

Hlavička a obsah atomu jsou označeny 32bitovým celým číslem známým jako velikost atomu. Pole size obsahuje velikost atomu v bajtech, vyjádřenou jako 32bitové celé číslo bez znaménka.

#### Typ atomu

Typ atomu je také znázorněn 32bitovým celým číslem, které je většinou považováno za čtyřznakové pole s knemonickou hodnotou, jako je „moov“ (0x6D6F6F76) pro atom filmu nebo „trak“ (0x7472616B) pro dráhový atom. Jakmile je znám typ atomu, umožňuje interpretaci jeho dat.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Struktura souboru ##

Soubory QT/MOV se skládají z po sobě jdoucích částí. Každý chunk má 8bajtové záhlaví: 4bajtová velikost chunku (big-endian, high byte first) a 4bajtový typ chunk – jeden z předdefinovaných podpisů: „ftyp“, „mdat“, „moov“, „pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". První chunk je typu "ftype" a má podtyp na offsetu 8. MOV definovaný podtypem, který musí být "qt". Chcete-li sestavit soubor MOV, je potřeba iterovat bloky, dokud není detekován neznámý typ.

Zde je ukázkový příklad: Při kontrole binárních dat ukázkového souboru MOV je zřejmé, že začíná podpisem **ftyp** (hex: 66 74 79 70) na offsetu 4, který definuje QuickTime Container File Type. Podtyp souboru je **qt~_~_** (hex: 71 74 20 20), což ukazuje na typ souboru MOV. Velikost prvního bloku je 32 (hex: 00 00 00 20, big-endian, první vysoký byte), velikost umístěná na offsetu 0. Na offsetu 32 (hex: 20) je umístěn druhý blok, který má velikost 8 a zadejte **mdat** (hex: 6D 64 61 74).

Další blok se nachází na offsetu 32+8#40 (hex: 28) a má velikost 3 263 028 (hex: 00 31 CA 34) a typ **mdat** (hex: 6D 64 61 74) na offsetu 44 (hex. : 2C). Další blok se nachází na offsetu 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) a má velikost 21,189 (hex: 00 00 52 C5) a typ **moov** (hex: 6D 6F) na offset 6F 76 1,836,019,574 (hex: 00 31 CA 60). Toto je poslední blok, takže celková velikost souboru je 3 263 068 + 21 189 # 3 284 257 bajtů.

## Reference ##

* [Formát souboru QT – Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Formát souboru QuickTime – Wikipedie](https://en.wikipedia.org/wiki/QuickTime_File_Format)

