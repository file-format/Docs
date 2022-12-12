{
  "date" : "2021-04-21",
  "keywords" :[ "soubor hrachu", "formát souboru hrachu", "co je soubor hrachu", "soubor", "příklad hrachu", "přípona souboru hrachu", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip Archive File Format",
  "description":"Další informace o formátu souboru PEA a rozhraních API, která mohou vytvářet a otevírat soubory PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Co je soubor PEA?

Soubor s příponou .pea, zkratka pro Pack, Encrypt a Authenticate, je archiv [zip](/cs/compression/zip/) vytvořený pomocí archivační softwarové aplikace [PeaZip](https://peazip.github.io/). Vyznačuje se kompresí a výstupem na více svazků a nabízí flexibilní model zabezpečení prostřednictvím ověřeného šifrování a kryptografie. To poskytuje jak soukromí, tak autentizaci dat. Nástroj PeaZip je k dispozici jako open source engine, který lze zkompilovat pro různé OS podle požadavků.

## Formát souboru PEA

[Specifikace formátu souboru PEA](https://peazip.github.io/pea_help.pdf) jsou veřejně dostupné pro vývojáře. Archivy PEA jsou binární soubory s flexibilním bezpečnostním modelem a redundantními kontrolami integrity od kontrolních součtů po kryptograficky silné hashe. To definuje tři různé úrovně komunikace k ovládání:

* Proudy – aktuální výstupní datový tok, který je tvořen více vstupními soubory a může být zapsán na více výstupních svazků
* Objekty - vstupní soubory a složky odeslané do archivu .pea
* Svazky - výstupní archivní soubor, který lze rozložit na uživatelem definovanou velikost

Každý z nich je volitelný a může být začleněn podle požadavků uživatele. Souborový formát PEA může uložit jeden stream obsahující neomezený počet objektů. Každý stream má velikost až 2^64 bajtů.

Soubory PEA nabízejí volitelnou kontrolu integrity a ověřené šifrování pomocí AES v režimu EAX nebo HMAC, alternativně Twofish a Serpent v režimu EAX.

### Záhlaví archivu PEA

Záhlaví archivu má 10 bajtů a je strukturováno následovně.

|Bajty|Popis|
---|---|
|1 | Pole magického bajtu pro jednoznačnost formátu souboru: $EA|
|1 | Číslo verze|
|1 | Číslo revize|
|1 | Schéma ovládání hlasitosti|
|1 | Deklarování OS, kde byl stream vytvořen|
|1 | Deklarování kódování data a času OS|
|1 | Deklarace názvu objektu kódování znaků|
|1 | Deklaruje typ CPU (zakódovaný v 7 bitech) a endianness (v msb)|
|1 | Rezervováno pro budoucí použití|

## Reference

* [Specifikace formátu souboru PEA](https://peazip.github.io/pea_help.pdf)
* [Formát souboru PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

