{
  "date" : "2021-08-09",
  "keywords" :[ "soubor cso", "formát souboru cso", "co je soubor cso", "soubor", "příklad cso", "přípona souboru cso", "přípona", "formát", "iso", "komprese DAX"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů CSO a rozhraních API, která mohou vytvářet a otevírat soubory CSO.",
  "title" :"CSO - komprimovaný obraz disku ISO",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Co je soubor CSO?

Soubor s příponou .cso je komprimovaný soubor obrazu ISO. CSO je alternativou ke kompresní metodě DAX; také známý jako CISO; byla první metodou ke komprimaci souborů [ISO](/cs/compression/iso/) a je obvykle preferovanou metodou pro archivaci obsahu PlayStation Portable. Tento formát používá kompresi Deflate, která může obsahovat až devět vrstev komprese. K vytvoření obrázků se používá software jako Prometheus a YACC.

## Formát souboru CSO

Formát souboru CSO byl první kompresní metodou pro ISO pro úsporu více místa v paměti. Čas od času byla provedena vylepšení pro lepší kompresi. CSO používá kompresi Deflate s devíti úrovněmi předvoleb, obvykle každá úroveň zvládne samostatně bloky 2 KiB. Zatímco nejvyšší úrovně komprese mohou zpomalit a prodloužit načítání softwaru, který silně závisí na streamování disku, také nižší úrovně mohou provádět podstatnou kompresi.

### Struktura souborů CSO

Formát souboru CSO obsahuje 24bajtové záhlaví, datové bloky a indexovou tabulku. Little-endian se předpokládá pro pole větší než bajt. Architektura systému PlayStation Portable je uvedena níže.

#### Záhlaví

| Offset (bajty) | Jméno | Velikost (bajty) | Účel |
----------|----------|--------------|---------|
| 0x0 | Magie | 4 | Vždy CISO nebo 0x4F534943 při čtení jako 32bitové celé číslo. Toto pole se používá k identifikaci souboru CSO. Všimněte si, že toto pole se může lišit pro ostatní deriváty CSO, například ZSO použil magický kód ZISO. |
| 0x4 | Velikost záhlaví | 4 | U původního formátu souboru CSO "v1" je toto pole ignorováno, a proto nemusí být přesné. Formát "v2" a ZSO však vyžaduje, aby toto pole bylo vždy 0x18 (24 bajtů). |
| 0x8 | Nekomprimovaná velikost | 8 | Velikost původního nekomprimovaného ISO v bajtech. |
| 0x10 | Velikost bloku | 4 | Velikost každého bloku dat v bajtech před kompresí. Obvykle 2048 bajtů, stejně jako velikost každého sektoru ISO 9660. |
| 0x14 | Verze | 1 | Verze používaného formátu souboru. Pro formát "v1" může být hodnota 0 nebo 1. Pro formát "v2" to musí být 2. Formát ZSO navíc vyžaduje, aby to bylo 1. Zpět nahoru |
| 0x15 | Zarovnání indexu | 1 | Zarovnání každé položky indexu zadané v bitech. |
| 0x16 | Rezervováno | 2 | Toto pole je nevyužité. Ve formátu "v1" je toto pole ignorováno a může obsahovat libovolné hodnoty. Ve formátu „v2“ musí být toto pole nula. |

#### Indexová tabulka

Indexová tabulka obsahuje několik 4bajtových položek, které označují polohu každého datového bloku, a další, poslední položku, která ukazuje na konec souboru.
Obsah každého záznamu je následující:
| Bit | Délka | Maska | Jméno | Účel |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Pozice | Toto pole, když je posunuto doleva o zarovnání indexu uvedené v záhlaví, udává pozici, kde datový blok začíná. |
| 31 | 1 | 0x80000000 | Typ komprese | Formát ZSO má podobnou sémantiku, jen 0 představuje LZ4 místo Deflate. Ve formátu "v2". Blok je implicitně považován za nekomprimovaný, pokud je velikost bloku stejná nebo větší než velikost bloku zadaná v záhlaví souboru. |

#### Datové bloky

Datové bloky se skládají z nekomprimovaných nebo komprimovaných dat. Velikost bloku se vypočítá získáním jeho polohy a následným odečtením od polohy následujícího bloku. Pokud je zarovnání indexu větší než nula, je pravděpodobné, že velikost bloku je větší než data, která obsahuje.


## Reference

* [CSO – podle Wikipedie](https://en.wikipedia.org/wiki/.CSO)


