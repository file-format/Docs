{
  "date": "2019-10-11",
  "keywords": [
"yaml",
".yaml",
"hvad er en yaml-fil",
"hvordan man åbner filen yaml",
"udvidelse",
"fil",
"yaml filen",
"yaml filformat",
".yaml udvidelse",
"yaml vs json",
"YAML fil eksempel",
"docker yaml fil eksempel"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " Lær om YAML filformat og API'er, der kan oprette og åbne en YAML fil.",
  "title": "YAML filformat",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-dal"
}
},
  "lastmod": "2021-05-05"
}

## Hvad er YAML fil? ##

**YAML-fil** består af et sprog YAML (YAML Ain't Markup Language), som er et Unicode-baseret data-serialiseringssprog; bruges til konfigurationsfiler, internetmeddelelser, objektpersistens osv. YAML bruger .yaml-udvidelsen til sine filer. Dens syntaks er uafhængig af et specifikt programmeringssprog. Grundlæggende er YAML designet til menneskelig interaktion og til at fungere godt med moderne programmeringssprog. Understøttelse af serialisering af vilkårlige native datastrukturer øgede læsbarheden af YAML-filerne, men det har gjort parsing- og filgenereringsprocessen lidt kompliceret.

## Kort historie ##

YAML blev først foreslået i 2001 og blev udviklet af Clark Evans, Ingy döt Net og Oren Ben-Kiki. YAML blev først sagt at betyde Yet Another Markup Language for at angive dets formål som et markup-sprog. Det blev senere genbrugt som YAML Aint Markup Language for at angive dets formål som data-orienteret.


## YAML filformat ##

YAML-filen består af følgende datatyper

- **Skalarer**: Skalarer er værdier som strenge, heltal, booleaner osv.
- **Sekvenser**: Sekvenser er lister, hvor hvert element starter med en bindestreg (-). Lister kan også indlejres.
- **Mappings**: Mapping giver mulighed for at liste nøgler med værdier.

### Syntaks ###

- **Whitespace**: Whitespace-indrykning bruges til at angive indlejring og overordnet struktur.

``` yaml
navn: John Smith
kontakt:
hjem: 1012355532
kontor: 5002586256
adresse:
gade: |
Tornado Alley 123
Suite 16
by: East Centerville
stat: KS
```

- **Kommentarer**: Kommentarer skrives begyndende med #-symbolet.

``` yaml
# Dette er en YAML-kommentar
```

- **Lister**: Bindestreg (-) bruges til at angive listemedlemmer med hvert medlem på en separat linje. Listemedlemmer kan også være omgivet af firkantede parenteser ([...]) med medlemmer adskilt af kommaer (,).

``` yaml
  - "EN"
  - "B"
  - "C"
```

``` yaml
[A, B, C]
```

- **Associativ array**: En associativ array er omgivet af krøllede parenteser ({...}). Nøglerne og værdierne er adskilt af kolon(:), og hvert par er adskilt med komma (,).

``` yaml
{navn: John Smith, alder: 20}
```

- **Strings**: Streng kan skrives med eller uden dobbelte anførselstegn () eller enkelte anførselstegn (').

``` yaml
Prøvestreng
"Prøvestreng"
Sample String
```

- **Skalært blokindhold**: Skalært indhold kan skrives i bloknotation ved at bruge følgende:
  - "**|**: Alle live-pauser er betydelige."
  - "**>**: Hvert linjeskift foldes til mellemrum. Det fjerner det indledende mellemrum for hver linje."

``` yaml
data: |
YAML
(YAML Ain't Markup Language)
er et data-serialiseringssprog
```

``` yaml
data: ?
YAML (YAML Ain't Markup Language)
er et data-serialiseringssprog
```

- **Flere dokumenter**: Flere dokumenter adskilles af tre bindestreger (---) i en enkelt strøm. Bindestreger angiver starten af dokumentet. Bindestreger bruges også til at adskille direktiver fra dokumentindhold. Slutningen af dokumentet er angivet med tre prikker (...).

``` yaml
  ---
Dokument 1
  ---
Dokument 2
...
```

- **Type**: For at specificere værditypen bruges dobbelte udråbstegn (!!).

``` yaml
a: !!float 123
b: !!str 123
```

- **Tag**: For at tildele et mærke til en note, bruges et og-tegn (&), og for at referere til den node bruges en stjerne (*).

``` yaml
navn: John Smith
fakturering til: &id01
gade: |
Tornado Alley 123
Suite 16
by: East Centerville
stat: KS

afsendelse til: *id01
```

- **Direktiver**: YAML-dokumenter kan indledes med direktiver i en strøm. Direktiverne begynder med et procenttegn (%) efterfulgt af navnet og derefter parametrene adskilt af mellemrum.

``` yaml
%YAML 1.2
  ---
Dokumentindhold
```
## YAML fil eksempel
Her kan du se et **docker yaml-fileksempel** nedenfor:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Grundlæggende er både JSON og YAML udviklet til at give et menneskelæsbart dataudvekslingsformat. YAML er realiseret som et supersæt af JSON-format. Det betyder, at vi kan parse JSON ved hjælp af en YAML-parser. Selvom den praktiske implementering af denne teori er lidt vanskelig. Derfor er nogle grundlæggende forskelle mellem YAML og JSON givet nedenfor:

|YAML| JSON|
---|---|
|Kompleks og tidskrævende proces med at parse serialiserede data |Hurtigt og nemt parse JSON serialiserede data med dets enklere design|
|Mindre fællesskabsstøtte| Større fællesskabsstøtte og popularitet|
|Understøtter kommentarer| Understøtter ikke kommentarer|
|Mulighed for at bruge reference til andre dataobjekter| Umuligt at serialisere komplekse strukturer med objektreferencer|
|Hierarki er angivet ved at bruge dobbelte mellemrumstegn. Tab-tegn er ikke tilladt|Objekter og arrays er angivet i klammer og parenteser.|
|Strenganførselstegn er valgfri, men den understøtter enkelte og dobbelte anførselstegn.|Strenge skal stå i dobbelte anførselstegn.|
|Rodknude kan være enhver af de gyldige datatyper|Rodknude skal enten være et array eller et objekt.|


## Referencer ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

