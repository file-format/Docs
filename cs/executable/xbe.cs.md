{
  "date" : "2021-08-31",
  "keywords" :[ "soubor xbe", "formát souboru xbe", "co je soubor xbe", "soubor", "příklad xbe", "přípona souboru xbe", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru XBE a rozhraních API, která mohou vytvářet a otevírat soubory XBE.",
  "title" :"XBE - soubor balíčku aplikace iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Co je soubor XBE?
Soubor s příponou .xbe je spustitelná aplikace z disku videohry Xbox. Soubory XBE jsou hlavní soubory, které se spouštějí v systému Xbox a neměly by se obvykle otevírat na počítači, ale lze je otevřít na počítači pomocí emulačního programu Xbox. Tyto soubory jsou obvykle vytvořeny vývojáři her a poté podepsány společností Microsoft. Struktura souborů je podobná souborům Windows PE, ale jsou provedeny některé důležité změny podle nastavení XBoxu, aby bylo možné jej spustit na XBoxu.

## Formát souboru XBE
Soubor XBE se skládá ze záhlaví obrázku, kolekce záhlaví sekcí, certifikátu, dat místního úložiště vláken, kolekce verzí knihoven, bitmapy Microsoft a sekcí, které obsahují kód a prostředky.

### Záhlaví obrázku
Záhlaví obrázku obsahuje informace, které vysvětlují, kde jsou v souboru umístěny další součásti spustitelného souboru a jak by se mělo s spustitelným souborem zacházet a jak jej načítat.

### Tabulka TLS
Tabulka TLS obsahuje všechny informace, které XBE potřebuje ke správnému nastavení lokálního úložiště vláken. Je v podstatě jedinečný pro adresář TLS, který se nachází v souborech PE32, a lze jej odtud přímo zkopírovat. Tato tabulka může být vynechána, pokud soubor XBE nepoužívá žádné místní úložiště vláken a příslušné pole v záhlaví obrázku je nastaveno na nulu.

| Offset | Velikost | Jméno | Popis |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Začátek nezpracovaných dat | Absolutní (tj. ne RVA) adresa začátku dat proměnné TLS v obraze programu. |
| 0x0004 | 0x0004 | Konec nezpracovaných dat | Absolutní (tj. ne RVA) adresa konce dat proměnné TLS v obraze programu. |
| 0x0008 | 0x0004 | Adresa rejstříku | Absolutní (tj. ne RVA) adresa proměnné indexu TLS. |
| 0x000C | 0x0004 | Adresa zpětných volání | Absolutní (tj. ne RVA) adresa tabulky funkcí zpětného volání TLS ukončená nulou. |
| 0x0010 | 0x0004 | Velikost nulové výplně | Počet bajtů po nezpracovaných datech, který by měl být v paměti nastaven na nulu. |
| 0x0014 | 0x0004 | Vlastnosti | Popisuje zarovnání. |

### Certifikát

Certifikát je povinný pro každý spustitelný soubor Xbox, který obsahuje informace o titulech:
 


- Čas a datum vytvoření certifikátu
- ID titulu
- Název titulu
- ID alternativních titulů
- Povolené typy médií, ze kterých lze spustitelný soubor (HD, DVD, CD atd.)
- Oblast hry
- Hodnocení hry
- Číslo disku
- Verze
- Nezpracovaná data klíčů LAN použitá pro System Link
- Nezpracovaná data podpisového klíče (používá se k podepisování uložených her)
- Alternativní podpisové klíče
- Původní velikost certifikátu
– Název online služby (není obsažen v raných spustitelných souborech)
- Příznaky zabezpečení v době běhu (není k dispozici v raných spustitelných souborech)
 


### Povolené typy médií
Typy médií, ze kterých může spustitelný soubor spouštět. Jsou známy následující hodnoty:
| Typ média | Hodnota |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIÁLNÍ_DESKA | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Sekce
Oddíly jsou vyjádřeny záhlavími oddílů. Záhlaví sekcí začíná hned za certifikátem a obsahuje informaci, kde v souboru aktuální sekce existují. Ve spustitelném souboru Xbox jsou vždy přítomny alespoň dvě sekce:


- .text


- .rdata


## Reference



* [Xbe - XBox spustitelný soubor](https://xboxdevwiki.net/Xbe)


