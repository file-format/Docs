{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType Collection File Format",
  "description":"Soubor TrueType Collection (TTC) kombinuje více písem do jednoho souboru. Apple i Microsoft používaly TTF v operačních systémech Mac a Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Co je soubor TTC?
TTC je zkráceno jako TrueType Collection je rozšířením formátu True Type. Soubor TTC do něj může kombinovat více souborů písem. Tyto soubory jsou výhodné pro kombinování více písem, které sdílejí mnoho společných glyfů. Před Windows 2000 byly soubory TTC používány v čínských, japonských a korejských verzích Windows, ale později byla podpora dostupná pro všechny regiony.


## Struktura souboru kolekce písem
Soubor TTC se skládá z tabulky záhlaví TTC, adresářů tabulek a více tabulek OpenType. Hlavička TTC musí být nalezena na začátku souboru. Musí existovat úplný adresář tabulky pro každé písmo. Formát TableDirectory by měl být podobný jako v souboru bez kolekce. Počty tabulek ve všech adresářích v souboru TTC se počítají od začátku souboru TTC.
Na tabulky v souboru TTC se odkazuje prostřednictvím adresáře tabulek příslušných písem. Několik tabulek OpenType se musí objevit vícekrát, jednou pro každý font přidaný do TTC. Zatímco ostatní tabulky mohou být sdíleny více fonty v souboru TTC.

### Záhlaví TTC
Dosud jsou k dispozici dvě verze tabulky záhlaví TTC:
- Verze 1.0 se používá pro soubory TTC bez digitálních podpisů.
- Verzi 2.0 lze použít pro soubory TTC s digitálním podpisem nebo bez něj.
Zde jsou tabulky záhlaví TTC obou verzí:

**TTC Header verze 1.0:**

|Typ|Název|Popis|
---|---|---|
|TAG|ttcTag|Řetězec ID kolekce písem: 'ttcf' (používá se pro písma s obrysy CFF nebo CFF2 a také obrysy TrueType)|
|uint16|majorVersion|Hlavní verze hlavičky TTC, = 1.|
|uint16|minorVersion|Vedlá verze hlavičky TTC, = 0.|
|uint32|numFonts|Počet písem v TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Pole offsetů k TableDirectory pro každý font od začátku souboru|

**TTC Header verze 2.0:**

|Typ|Název|Popis|
---|---|---|
|TAG|ttcTag |Řetězec ID kolekce písem: 'ttcf'|
|uint16| majorVersion |Hlavní verze hlavičky TTC, = 2.|
|uint16| minorVersion |Vedlejší verze hlavičky TTC, = 0.|
|uint32| numFonts |Počet písem v TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Pole offsetů do TableDirectory pro každý font od začátku souboru|
|uint32| dsigTag |Značka indikující existenci tabulky DSIG, 0x44534947 ('DSIG') (null, pokud není žádný podpis)|
|uint32| dsigLength |Délka (v bajtech) tabulky DSIG (null, pokud není žádný podpis)|
|uint32| dsigOffset |Offset (v bajtech) tabulky DSIG od začátku souboru TTC (null, pokud není žádný podpis)|

## Reference
* [Soubor písem OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

