{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MPG",
  "keywords" :[ "MPG", "soubor", "rozšíření", "formát", "formát videa", "co je formát souboru mpg", "formát souboru mpg", "přehrávač souborů mpg", "komprese mpeg", "video", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Další informace o formátu souboru MPG a rozhraních API, která mohou vytvářet a ukázat, jak otevřít soubory MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Co je formát souboru MPG? ##

Soubor s příponou .mpg patří do skupiny přípon souborů pro kompresi zvuku a videa MPEG-1 nebo MPEG-2. Video MPEG-1 Part 2 není snadno dostupné a toto rozšíření (formát souboru MPG) obvykle odkazuje na programový proud MPEG, který je definován v MPEG-1 a MPEG-2, nebo na transportní proud MPEG, který je definován v MPEG-2. . Existují také další přípony, jako je .m2ts, které specifikují přesný kontejner, v tomto případě MPEG-2 TS, ale to má jen malý význam pro média MPEG-1. [.mp3](https://docs.fileformat.com/audio/mp3/) je nejběžnější přípona pro soubory obsahující zvuk MP3. Soubor MP3 je typický proud nezpracovaného zvuku; tradičním způsobem označování souborů MP3 je zapisování datových proudů do „odpadních“ segmentů každého snímku, které ukládají informace o médiích, ale **přehrávač souborů mpg** je zahodí. Jedná se o podobnou techniku používanou k označování souborů AAC, ale v dnešní době méně podporovanou.

## MPEG komprese ##

Název MPEG znamená Moving Pictures Experts Group. MPEG je nástroj pro kompresi videa, který zahrnuje kompresi obrázků a zvuků a také jejich synchronizaci.
V současné době existuje několik standardů MPEG.

- MPEG-1 je navržen pro střední datové rychlosti, řádově 1,5 Mbit/s.
- MPEG-2 je navržen pro vysoké přenosové rychlosti alespoň 10 Mbit/s.
- MPEG-3 byl navržen pro kompresi HDTV, ale byl shledán nadbytečným a byl sloučen s MPEG-2.
- MPEG-4 je navržen pro velmi nízké datové rychlosti nižší než 64 Kbit/s.


## Programový stream souboru MPG ve formátu ##

Programový proud je kontejner pro multiplexování digitálního zvuku, videa a dalších. Formát Program Stream je specifikován v 1. části MPEG-1 (ISO/IEC 11172-1) a 1. části MPEG-2, Systémy (norma ISO/IEC 13818-1/ITU-T H.222.0). MPEG-2 Program Stream je analogový a podobný systémové vrstvě ISO/IEC 11172 a je dopředně kompatibilní.

### Podrobnosti o kódování ###

Zde jsou podrobnosti o kódování formátu záhlaví částečného balíčku MPEG-2 Program Stream:

| Jméno | Počet bitů | Popis |
---|---|---|
| synchronizační bajty | 32 | 0x000001BA |
| značkovací bity | 2 | 01b pro verzi MPEG-2. Značkové bity pro verzi MPEG-1 jsou 4 bity s hodnotou 0010b. |
| Systémové hodiny [32..30] | 3 | Bity 32 až 30 referenčních hodin systému (SCR) |
| značkovací bit | 1 | Vždy nastaven 1 bit. |
| Systémové hodiny [29..15] | 15 | Bity systémových hodin 29 až 15 |
| značkovací bit | 1 | Vždy nastaven 1 bit. |
| Systémové hodiny [14..0] | 15 | Bity systémových hodin 14 až 0 |
| značkovací bit | 1 | Vždy nastaven 1 bit. |
| Rozšíření SCR | 9 | |
| značkovací bit | 1 | Vždy nastaven 1 bit. |
| přenosová rychlost | 22 | V jednotkách 50 bajtů za sekundu. |
| značkovací bity | 2 | Vždy nastaveno 11 bitů. |
| rezervováno | 5 | vyhrazeno pro budoucí použití |
| délka náplně | 3 | |
| vycpávky | 8*délka náplně | |
| hlavička systému (volitelné) | 0 nebo více | pokud následuje počáteční kód záhlaví systému: 0x000001BB |

Následující tabulka ukazuje formát částečného záhlaví systému:

| Jméno | Počet bajtů | Popis |
---|---|---|
| synchronizační bajty | 4 | 0x000001BB |
| délka hlavičky | 2 | |
| sazba vázaná a značkovací bity | 3 | |
| zvuková vazba a příznaky | 1 | |
| vlajky, bit značky a vázané video | 1 | |
| Omezení paketové rychlosti a rezervovaný bajt | 1 | |


## Reference ##

- [MPEG-1 - Wikipedie](https://en.wikipedia.org/wiki/MPEG-1)



