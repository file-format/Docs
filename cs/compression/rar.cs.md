{
  "date" : "2019-10-11",
  "keywords" :[ "soubor rar", "formát souboru rar", "co je soubor rar", "soubor", "příklad rar", "přípona souboru rar", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Co je přípona souboru RAR a rozhraní API, která mohou vytvářet a otevírat soubory RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor RAR?

Soubory s příponou .rar jsou archivní soubory, které jsou vytvořeny pro ukládání informací v komprimované nebo normální formě. RAR, což je zkratka pro formát souboru Roshal ARchive, je proprietární formát souboru vytvořený Eugenem Roshalem v roce 1995, který byl ruským softwarovým inženýrem. Tento formát se používá k archivaci souborů různými metodami včetně různých technik komprese. Pro extrakci souborů RAR je k dispozici několik aplikačních programů pro Windows, Linux a MacOS. Software WinRAR od RARLab je sharewarový nástroj pro archivaci souborů (zdarma po dobu 40 dnů) pro platformu Microsoft Windows; software byl portován na Linux (pouze jako extraktor) stejným autorem, Eugenem Roshalem.

## Historie verzí formátu souborů RAR

* v1.3 (původní, nemá podpis "Rar!")
* verze 1.5
* v2.0 – vydáno s WinRAR 2.0 a Rar pro MS-DOS 2.0
* v2.9 - vydáno ve WinRAR verzi 3.00
* v5.0 – podporováno WinRAR 5.0 a novějšími

## Klíčové vlastnosti formátu RAR

RAR je v oboru již poměrně dlouho a patří mezi oblíbené formáty archivačních souborů. Klíčové vlastnosti formátu RAR jsou:

**`Vysoký kompresní poměr:`** Vynikající ve srovnání s [ZIP](/cs/komprese/zip/), srovnatelné s formátem 7z a zipx.

**`Silné šifrování souborů podle návrhu:`** Šifrované archivy RAR4 se spoléhají na šifrování založené na AES-128, zatímco šifrované archivy RAR5 se spoléhají na šifrování AES-256 s vylepšeným plánováním klíčů

**`Pokročilé možnosti opravy chyb a obnovy dat:`** volitelné záznamy obnovy během vytváření archivu

**`Velikost souboru:`** Velikost minimálně 20 bajtů a maximálně 2^63 bajtů (8 exabajtů celkové velikosti archivu)

**`Vícesvazkové archivy RAR:`** Možnost rozdělit velké archivy na několik menších souborů pro usnadnění přenosu po síti. V takovém případě se přípony souborů zvýší o 1, aby představovaly rozdělené svazky

## Formát souboru RAR

Kompletní specifikace formátu RAR nejsou veřejně dostupné, a proto nelze podrobnosti o formátu formulovat stručně.

### Obecné rozložení archivu

Obecné rozložení formátu souboru RAR představeného ve verzi 5.0 je následující:

| Formát souboru
---|
| Samorozbalovací modul (volitelný)
|Podpis RAR 5.0
|Záhlaví šifrování archivu (volitelné)
|Hlavní záhlaví archivu
|Archivovat záhlaví služby komentářů (volitelné)
Záhlaví souboru 1
|Záhlaví služeb (NTFS ACL, streamy atd.) pro předchozí soubor (volitelné)
|...
|Záhlaví souboru N
|Záhlaví služeb (NTFS ACL, streamy atd.) pro předchozí soubor (volitelné)
|Záznam o obnovení (volitelné)
|Konec hlavičky archivu

Informace o každé části souboru RAR uvedené výše lze nalézt v dokumentu [Specifikace formátu RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Samorozbalovací archivy RAR

Pokud je samotný soubor RAR samorozbalovací, jsou informace o samorozbalování obsaženy na začátku souboru před podpisem archivu. Jeho velikost a obsah nejsou definovány.

#### Podpis RAR 5.0

RAR signatura je 8bajtová hlavička, která se skládá z následujícího magického čísla:

0x 52 61 72 21 1A 07 00

kde

0x6152 – HEAD_CRC

0x72 – HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Reference

* [Formát archivu RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR – z Wikipedie](https://en.wikipedia.org/wiki/RAR_(formát_souboru))

