{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","co je soubor yaml","jak otevřít soubor yaml", "přípona", "soubor", "soubor yaml","formát souboru yaml", "přípona .yaml" , "yaml vs json" ,"příklad souboru YAML", "příklad souboru docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru YAML a rozhraních API, která mohou vytvořit a otevřít soubor YAML.",
  "title" :"Formát souboru YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Co je soubor YAML? ##

**Soubor YAML** se skládá z jazyka YAML (YAML Ain't Markup Language), což je jazyk pro serializaci dat založený na Unicode; používá se pro konfigurační soubory, internetové zprávy, persistenci objektů atd. YAML používá pro své soubory příponu .yaml. Jeho syntaxe je nezávislá na konkrétním programovacím jazyce. V zásadě je YAML navržen pro lidskou interakci a pro dobrou spolupráci s moderními programovacími jazyky. Podpora pro serializaci libovolných nativních datových struktur zvýšila čitelnost souborů YAML, ale trochu zkomplikovala proces analýzy a generování souborů.

## Stručná historie ##

YAML byl poprvé navržen v roce 2001 a byl vyvinut Clarkem Evansem, Ingy döt Net a Oren Ben-Kiki. YAML bylo poprvé řečeno, že znamená „Ještě další značkovací jazyk“, aby naznačil svůj účel jako značkovací jazyk. Později byl přepracován jako „YAML Aint Markup Language“, aby naznačil svůj účel jako datově orientovaný.


## Formát souboru YAML ##

Soubor YAML se skládá z následujících datových typů

- **Skaláry**: Skaláry jsou hodnoty jako řetězce, celá čísla, booleovské hodnoty atd.
- **Sekvence**: Sekvence jsou seznamy, kde každá položka začíná pomlčkou (-). Seznamy lze také vnořovat.
- **Mappings**: Mapování umožňuje vypsat klíče s hodnotami.

### Syntaxe ###

- **Whitespace**: Whitespace odsazení se používá k označení vnoření a celkové struktury.

```jaml
jméno: John Smith
Kontakt:
domov: 1012355532
kancelář: 5002586256
adresa:
ulice: |
123 Tornádo Alley
Apartmá 16
město: East Centerville
stav: KS
```

- **Komentáře**: Komentáře začínají znakem „#“.

```jaml
# Toto je komentář YAML
```

- **Seznamy**: Spojovník (-) se používá k označení členů seznamu s každým členem na samostatném řádku. Členy seznamu lze také uzavřít do hranatých závorek ([...]) s členy oddělenými čárkami (,).

```jaml
  - A
  - B
  - C
```

```jaml
[A, B, C]
```

- **Asociativní pole**: Asociativní pole je obklopeno složenými závorkami ({...}). Klíče a hodnoty jsou odděleny dvojtečkou (:) a každý pár je oddělen čárkou (,).

```jaml
  {name: John Smith, age: 20}
```

- **Řetězce**: Řetězec lze psát s uvozovkami nebo bez uvozovek (") nebo jednoduchých uvozovek (').

```jaml
Vzorový řetězec
"Ukázkový řetězec"
'Ukázkový řetězec'
```

- **Obsah skalárních bloků**: Skalární obsah lze zapsat v blokovém zápisu pomocí následujícího:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```jaml
údaje: |
YAML
(YAML není značkovací jazyk)
je jazyk pro serializaci dat
```

```jaml
údaje: ?
YAML (YAML není značkovací jazyk)
je jazyk pro serializaci dat
```

- **Více dokumentů**: Více dokumentů je odděleno třemi pomlčkami (---) v jednom proudu. Pomlčky označují začátek dokumentu. Pomlčky se také používají k oddělení direktiv od obsahu dokumentu. Konec dokumentu je označen třemi tečkami (...).

```jaml
  ---
Dokument 1
  ---
Dokument 2
...
```

- **Typ**: K určení typu hodnoty se používají dvojité vykřičníky (!!).

```jaml
a: !!plovoucí 123
b: !!str 123
```

- **Značka**: K přiřazení značky k poznámce se používá ampersand (&) a k odkazování na tento uzel se používá hvězdička (*).

```jaml
jméno: John Smith
bill-to: &id01
ulice: |
123 Tornádo Alley
Apartmá 16
město: East Centerville
stav: KS

odeslání: *id01
```

- **Směrnice**: Dokumentům YAML mohou v proudu předcházet směrnice. Direktivy začínají znakem procenta (%), za kterým následuje název a poté parametry oddělené mezerami.

```jaml
%YAML 1.2
  ---
Obsah dokumentu
```
## Příklad souboru YAML
Zde můžete vidět **příklad souboru yaml docker** níže:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
JSON i YAML jsou v zásadě vyvinuty tak, aby poskytovaly lidem čitelný formát pro výměnu dat. YAML je realizován jako nadmnožina formátu JSON. To znamená, že můžeme analyzovat JSON pomocí analyzátoru YAML. I když praktické provedení této teorie je málo složité. Některé základní rozdíly mezi YAML a JSON jsou proto uvedeny níže:

|YAML| JSON|
---|---|
|Složitý a časově náročný proces analýzy serializovaných dat |Rychlá a snadná analýza serializovaných dat JSON díky jednoduššímu designu|
|Menší podpora komunity| Větší podpora komunity a popularita|
|Podporuje komentáře| Nepodporuje komentáře|
|Schopnost používat reference jiných datových objektů| Není možné serializovat složité struktury s odkazy na objekty|
|Hierarchie je označena pomocí dvojitých mezer. Znaky tabulátoru nejsou povoleny|Objekty a pole jsou označeny ve složených závorkách a závorkách.|
|Řetězce jsou volitelné, ale podporují jednoduché a dvojité uvozovky.|Řetězce musí být ve dvojitých uvozovkách.|
|Kořenový uzel může být kterýkoli z platných datových typů|Kořenový uzel musí být pole nebo objekt.|


## Reference ##

- [YAML - Wikipedie](https://en.wikipedia.org/wiki/YAML)
– [YAML](https://yaml.org/spec/1.2/spec.html)

