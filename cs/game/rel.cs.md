{
  "date" : "2021-09-08",
  "keywords" :[ "soubor rel", "formát souboru rel", "co je soubor rel", "soubor", "příklad rel", "přípona souboru rel", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru REL a rozhraních API, která mohou vytvářet a otevírat soubory REL.",
  "title" :"REL - Relocatable Module File",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Co je soubor REL?
Soubor s příponou .rel lze použít k několika účelům. Proto je z hlediska klasifikace her známý jako přemístitelný modulový soubor používaný některými hrami pro Nintendo Wii, jako jsou Brawl, Super Smash Bros a Mario Kart Wii. Zahrnuje herní data, včetně modelů postav a fází. Soubory REL fungují podobně jako soubory .DLL používané systémem Microsoft Windows.

## Formát souboru REL
Ve formátu souboru REL je soubor rozdělen do několika sekcí, seskupených podle podobného přístupu, např. data pouze pro čtení v jedné sekci, veškerý spustitelný kód je umístěn v jiné atd. Soubor začíná sekcí záhlaví, za kterou následuje:
- Tabulka obsahující informace o sekci.
- Údaje o sekci.
- Informace o přemístění.

### Záhlaví souboru
Soubor začíná záhlavím o velikosti až 0x4C bajtů:
| Offset | Velikost | Název pole | Popis |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Svévolné identifikační číslo. Musí být jedinečné mezi všemi REL používanými hrou. Nesmí být 0. |
| 0x04 | 4 | další | Ukazatel na další modul, vyplněný za běhu. |
| 0x08 | 4 | předchozí | Ukazatel na předchozí modul, vyplněný za běhu. |
| 0x0c | 4 | numSections | Počet oddílů v souboru. |
| 0x10 | 4 | sectionInfoOffset | Odsazení na začátek tabulky sekcí. |
| 0x14 | 4 | názevOffset | Offset na řetězec ASCII obsahující název modulu. Může být NULL. Relativní k začátku souboru REL. |
| 0x18 | 4 | jménoVelikost | Velikost názvu modulu v bajtech. |
| 0x1c | 4 | verze | Číslo verze formátu souboru REL. |
| 0x20 | 4 | velikost bss | Velikost sekce '.bss'. |
| 0x24 | 4 | relOffset | Offset k přemístění tabulky. |
| 0x28 | 4 | imOffset | Offset k tabulce imp. |
| 0x2c | 4 | imSize | Velikost tabulky imp v bajtech. |
| 0x30 | 1 | sekce prolog | Index do tabulky sekcí, ke které se prolog vztahuje. Přeskočte, pokud je toto pole 0. |
| 0x31 | 1 | epilogSection | Indexujte do tabulky sekcí, ke kterému se epilog vztahuje. Přeskočte, pokud je toto pole 0. |
| 0x32 | 1 | nevyřešená sekce | Index do tabulky sekcí, ke které se nevyřešené vztahují. Přeskočte, pokud je toto pole 0. |
| 0x33 | 1 | bssSection | Index do tabulky sekcí, ke které je bss relativní. Vyplněno za běhu! |
| 0x34 | 4 | prolog | Offset do zadané části funkce _prolog. |
| 0x38 | 4 | epilog | Offset do zadané části funkce _epilog. |
| 0x3c | 4 | nevyřešeno | Offset do zadané části funkce _unresolved. |
| 0x40 | 4 | zarovnat | Pouze verze ≥ 2. Omezení zarovnání na všech řezech, vyjádřené jako mocnina 2. |
| 0x44 | 4 | bssAlign | Pouze verze ≥ 2. Omezení zarovnání na všech částech '.bss', vyjádřené jako mocnina 2. |
| 0x48 | 4 | fixSize | Pouze verze ≥ 3. Pokud je REL propojen s OSLinkFixed (místo OSLink), lze mezeru za touto adresou použít pro jiné účely (jako BSS). |

### Informační tabulka sekce
Informační tabulka sekce obsahuje **numSections** záznamů o délce 0x8 bajtů:
| Offset | Velikost | Popis |
-------|------------|-------------|
| 0x0 | 30 bitů | Odsazení od začátku REL k sekci. Pokud je toto nula, sekce je neinicializovaná sekce (tj. .bss). |
| 0x3,6 | 1 bit | Neznámý. |
| 0x3,7 | 1 bit | Spustitelný příznak; pokud je to 1, sekce je spustitelná. |
| 0x4 | 4 | Délka sekce v bajtech. Pokud je toto nula, bude tento záznam přeskočen. |
| 0x8 | Další záznam | Další záznam |

### Údaje o přemístění
Data o přemístění jsou jeden nebo více seznamů struktur 0x8 bajtů. Konec každého seznamu je označen speciálním kódem typu 203:
| Offset | Jméno | Velikost | Popis |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Posun v bajtech od předchozího přemístění do tohoto. Pokud se jedná o první přemístění v sekci, je to relativní k začátku sekce. |
| 0x2 | typ | 1 | Typ přemístění. Popsané níže. |
| 0x3 | sekce | 1 | Část symbolu, na kterou se má přemístit. Pro speciální typ přemístění 202 je to místo toho číslo sekce v tomto souboru, na kterou se vztahují následující položky přemístění. |
| 0x4 | přidat | 4 | Odsazení v bajtech symbolu, proti kterému se má přemístit, vzhledem k začátku jeho části. Toto je absolutní adresa místo toho pro přemístění proti main.dol. |
| 0x8 | Další záznam | Další záznam | Další záznam |


 




## Reference


* [Formát modulu Relocatable Object Module](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


