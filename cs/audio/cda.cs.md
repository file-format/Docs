{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "soubor", "přípona", "formát", "co je soubor cda", "hudba", "formát souboru cda", "specifikace formátu souboru cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů CDA a rozhraních API, která mohou vytvářet, převádět a otevírat soubory CDA.",
  "title" :"CDA - soubor zástupce zvukové stopy CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Co je soubor CDA?

Soubor s příponou .cda je malý stub soubor generovaný systémem Microsoft Windows pro každou zvukovou stopu na zvukovém disku CD. Tyto soubory obsahují typické informace, jako jsou časy skladeb a zástupce systému Windows, který uživatelům umožňuje přístup ke konkrétním zvukovým stopám. Soubory CDA nejsou hudba, ale ukazují na hudební soubor, který někde v úložišti existuje. Můžeme to říci jako zástupce zvukového souboru, který je umístěn na CD.

## Formát souboru CDA

Formát souboru CDA se používá k tomu, aby počítači řekl, který zvukový soubor má na disku CD přehrát. Soubory CDA se tak stanou neužitečnými oddělenými od CD, které představují. Soubory CDA jsou běžně považovány za zdroje RIFF. Existuje pouze jeden chunk, který se jmenuje "CDDA" a obsahuje pouze jeden datový blok nazvaný "FMT" v aktuální verzi souboru .cda. Tento blok je dlouhý 24 bajtů. Identifikátor vytvořený systémem Windows používá jednotka CD související s Windows 95 a Windows 98 a její přehrávač se nemůže připojit k FreeDB nebo CDDB. Aby mohl zobrazovat název skladby a jméno interpreta, které musíte ručně zadat do souboru cdplayer.ini.

### Organizace souboru CDA

Následující tabulka ukazuje informace o typických offsetech:
| offset | délka | obsah |
---|---|---|
| 0x00 | 4 | 4 ASCII znaky "RIFF" |
| 0x04 | 4 | velikost následujícího bloku: vždy 36 (44 - 8), na 4 bytech (objednávka Intel) |
| 0x08 | 4 | identifikátor bloku: 4 znaky ASCII "CDDA" |
| 0x0C | 4 | 3 znaky ASCII "fmt" následované mezerou |
| 0x10 | 4 | délka bloku: vždy 24, na 4 bytech (pořadí Intel) |
| 0x14 | 2 | verze formátu CD, na 2 bytech (objednávka Intel). V květnu 2006 vždy rovno 1. |
| 0x016 | 2 | číslo rozsahu, na 2 bytech (objednávka Intel). První stopa má číslo 1. |
| 0x18 | 4 | identifikátor vypočítaný systémem Windows pro cdplayer.exe. |
| 0x1c | 4 | posun rozsahu, v počtu snímků (objednávka Intel) |
| 0x20 | 4 | trvání stopy, celkový počet snímků (objednávka Intel) |
| 0x24 | 1 | pozice rozsahu: rámečky |
| 0x25 | 1 | pozice rozsahu: sekundy |
| 0x26 | 1 | pozice rozsahu: minuty |
| 0x27 | 1 | nulový bajt (binární hodnota 0) |
| 0x28 | 1 | délka stopy: snímky |
| 0x29 | 1 | délka stopy: sekundy |
| 0x2a | 1 | délka stopy: minuty |
| 0x2b | 1 | nulový bajt (binární hodnota 0) |

## Reference

* [soubor .cda – z Wikipedie](https://en.wikipedia.org/wiki/.cda_file)

