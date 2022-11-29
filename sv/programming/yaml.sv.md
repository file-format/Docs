{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","vad är en yaml-fil","hur man öppnar en yaml-fil", "tillägg", "fil", "yaml-fil","yaml-filformat", ".yaml-tillägg" , "yaml vs json" ,"YAML-filexempel", "docer yaml-filexempel"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Lär dig om YAML-filformat och API:er som kan skapa och öppna en YAML-fil.",
  "title" :"YAML filformat",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Vad är YAML fil? ##

**YAML-fil** består av ett språk YAML (YAML Ain't Markup Language) som är ett Unicode-baserat dataserialiseringsspråk; används för konfigurationsfiler, internetmeddelanden, objektbeständighet, etc. YAML använder tillägget .yaml för sina filer. Dess syntax är oberoende av ett specifikt programmeringsspråk. I grund och botten är YAML designad för mänsklig interaktion och för att fungera bra med moderna programmeringsspråk. Stöd för att serialisera godtyckliga inbyggda datastrukturer ökade läsbarheten för YAML-filerna, men det har gjort tolkningen och filgenereringsprocessen lite komplicerad.

## Kortfattad bakgrund ##

YAML föreslogs först 2001 och utvecklades av Clark Evans, Ingy döt Net och Oren Ben-Kiki. YAML sades först betyda "Yet Another Markup Language" för att indikera dess syfte som ett märkningsspråk. Det byttes senare om som "YAML Aint Markup Language" för att indikera dess syfte som dataorienterat.


## YAML filformat ##

YAML-filen består av följande datatyper

- **Skalärer**: Skalärer är värden som strängar, heltal, booleaner osv.
- **Sekvenser**: Sekvenser är listor där varje objekt börjar med ett bindestreck (-). Listor kan också kapslas.
- **Mappningar**: Mappning ger möjlighet att lista nycklar med värden.

### Syntax ###

- **Whitespace**: Whitespace-indragning används för att indikera kapsling och övergripande struktur.

``` jaml
namn: John Smith
Kontakt:
hem: 1012355532
kontor: 5002586256
adress:
gata: |
Tornadogränd 123
Svit 16
stad: East Centerville
ange: KS
```

- **Kommentarer**: Kommentarer skrivs med början med "#"-symbolen.

``` jaml
# Det här är en YAML-kommentar
```

- **Listor**: Bindestreck (-) används för att indikera listmedlemmar med varje medlem på en separat rad. Listmedlemmar kan också omges av hakparenteser ([...]) med medlemmar separerade med kommatecken (,).

``` jaml
  - A
  - B
  - C
```

``` jaml
[A, B, C]
```

- **Associativ array**: En associativ array omges av parenteser ({...}). Nycklarna och värdena separeras med kolon(:) och varje par separeras med kommatecken (,).

``` jaml
  {name: John Smith, age: 20}
```

- **Strängar**: Sträng kan skrivas med eller utan dubbla citattecken (") eller enkla citattecken (').

``` jaml
Exempel sträng
"Sample String"
"Sample String"
```

- **Skalärt blockinnehåll**: Skalärt innehåll kan skrivas i blocknotation genom att använda följande:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

``` jaml
data: |
YAML
(YAML Ain't Markup Language)
är ett dataserialiseringsspråk
```

``` jaml
data: ?
YAML (YAML Ain't Markup Language)
är ett dataserialiseringsspråk
```

- **Flera dokument**: Flera dokument separeras med tre bindestreck (---) i en enda ström. Bindestreck anger början av dokumentet. Bindestreck används också för att skilja direktiv från dokumentinnehåll. Slutet på dokumentet indikeras med tre punkter (...).

``` jaml
  ---
Dokument 1
  ---
Dokument 2
...
```

- **Typ**: För att ange typen av värde används dubbla utropstecken (!!).

``` jaml
a: !!float 123
b: !!str 123
```

- **Tag**: För att tilldela en tagg till en anteckning används ett et-tecken (&) och för att referera till den noden används en asterisk (*).

``` jaml
namn: John Smith
fakturera till: &id01
gata: |
Tornadogränd 123
Svit 16
stad: East Centerville
ange: KS

skicka till: *id01
```

- **Direktiv**: YAML-dokument kan föregås av direktiv i en ström. Direktiv börjar med ett procenttecken (%) följt av namnet och sedan parametrarna separerade med mellanslag.

``` jaml
%YAML 1.2
  ---
Dokumentinnehåll
```
## Exempel på YAML-fil
Här kan du se ett **docker yaml-filexempel** nedan:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
I grund och botten är både JSON och YAML utvecklade för att tillhandahålla ett läsbart datautbytesformat. YAML realiseras som en superset av JSON-format. Det betyder att vi kan analysera JSON med en YAML-parser. Även om det praktiska genomförandet av denna teori är lite knepigt. Därför ges några grundläggande skillnader mellan YAML och JSON nedan:

|YAML| JSON|
---|---|
|Komplex och tidskrävande process för att tolka serialiserade data |Snabbt och enkelt analysera JSON-serialiserad data med sin enklare design|
|Mindre gemenskapsstöd| Större gemenskapsstöd och popularitet|
|Stöder kommentarer| Stöder inte kommentarer|
|Möjlighet att använda referenser för andra dataobjekt| Omöjligt att serialisera komplexa strukturer med objektreferenser|
|Hierarki betecknas med dubbla mellanslag. Tabtecken är inte tillåtna|Objekt och matriser anges inom klammerparenteser.|
|Citatsträngar är valfria men det stöder enkla och dubbla citattecken.|Strängar måste stå inom dubbla citattecken.|
|Rotnod kan vara vilken som helst av de giltiga datatyperna|Rotnoden måste antingen vara en array eller ett objekt.|


## Referenser ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

