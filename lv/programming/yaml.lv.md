{
  "date": "2019-10-11",
  "keywords": [
"jaml",
".yaml",
"kas ir yaml fails",
"kā atvērt yaml failu",
"pagarinājumu",
"failu",
"yaml fails",
"yaml faila formāts",
".yaml paplašinājums",
"yaml vs json",
"YAML faila piemērs",
"docker yaml faila piemērs"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " Uzziniet par YAML faila formātu un API, kas var izveidot un atvērt YAML failu.",
  "title": "YAML faila formāts",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-lvl"
}
},
  "lastmod": "2021-05-05"
}

## Kas ir YAML fails? ##

**YAML fails** sastāv no valodas YAML (YAML Ain't Markup Language), kas ir uz Unikoda bāzes datu serializācijas valoda; izmanto konfigurācijas failiem, interneta ziņojumapmaiņai, objektu noturībai utt. YAML failiem izmanto paplašinājumu .yaml. Tās sintakse nav atkarīga no noteiktas programmēšanas valodas. Būtībā YAML ir paredzēts cilvēku mijiedarbībai un labi darbam ar mūsdienu programmēšanas valodām. Atbalsts patvaļīgu vietējo datu struktūru serializēšanai palielināja YAML failu lasāmību, taču tas ir nedaudz sarežģījis parsēšanas un failu ģenerēšanas procesu.

## Īsa vēsture ##

YAML pirmo reizi tika ierosināts 2001. gadā, un to izstrādāja Klārks Evanss, Ingy döt Net un Orens Ben-Kiki. Vispirms tika teikts, ka YAML nozīmē vēl viena iezīmēšanas valoda, lai norādītu tās kā iezīmēšanas valodas mērķi. Vēlāk tā tika pārdēvēta par YAML Aint Markup Language, lai norādītu, ka tā ir orientēta uz datiem.


## YAML faila formāts ##

YAML fails sastāv no šādiem datu tipiem

- **Skalāri**: skalāri ir tādas vērtības kā virknes, veseli skaitļi, Būla skaitļi utt.
- **Secības**: secības ir saraksti, kuros katrs vienums sākas ar defisi (-). Sarakstus var arī ievietot ligzdā.
- **Kartēšana**: kartēšana sniedz iespēju uzskaitīt atslēgas ar vērtībām.

### Sintakse ###

- **Atstarpes**: atstarpes atkāpe tiek izmantota, lai norādītu ligzdošanu un vispārējo struktūru.

``` jaml
vārds: Džons Smits
kontaktēties:
mājas numurs: 1012355532
birojs: 5002586256
adrese:
iela: |
123 Tornado aleja
Suite numurs 16
pilsēta: East Centerville
valsts: KS
```

- **Komentāri**: Komentāri tiek rakstīti, sākot ar simbolu #.

``` jaml
# Šis ir YAML komentārs
```

- **Saraksti**: defise (-) tiek izmantota, lai norādītu saraksta dalībniekus ar katru dalībnieku atsevišķā rindā. Saraksta dalībniekus var arī ievietot kvadrātiekavās ([...]), atdalot tos ar komatiem (,).

``` jaml
  - "A"
  - "B"
  - "C"
```

``` jaml
[A, B, C]
```

- **Asociatīvais masīvs**: asociatīvo masīvu ieskauj krokainas iekavas ({...}). Atslēgas un vērtības ir atdalītas ar kolu (:), un katrs pāris ir atdalīts ar komatu (,).

``` jaml
{vārds: Džons Smits, vecums: 20}
```

- **Virknes**: virkni var rakstīt ar dubultpēdiņām () vai vienpēdiņām (') vai bez tām.

``` jaml
Virknes paraugs
"Virknes paraugs"
Parauga virkne
```

- **Skalārā bloka saturs**: skalāro saturu var rakstīt bloka apzīmējumā, izmantojot tālāk norādīto.
  - "**|**: visi tiešraides pārtraukumi ir nozīmīgi."
  - "**>**: katrs rindiņas pārtraukums tiek pārlocīts līdz atstarpei. Tas noņem katras rindas vadošo atstarpi."

``` jaml
dati: |
YAML
(YAML nav iezīmēšanas valoda)
ir datu serializācijas valoda
```

``` jaml
dati: ?
YAML (YAML nav iezīmēšanas valoda)
ir datu serializācijas valoda
```

- **Vairāki dokumenti**: vairāki dokumenti ir atdalīti ar trim defisēm (---) vienā straumē. Defises norāda dokumenta sākumu. Defises tiek izmantotas arī, lai atdalītu direktīvas no dokumenta satura. Dokumenta beigas ir apzīmētas ar trim punktiem (...).

``` jaml
  ---
1. dokuments
  ---
2. dokuments
...
```

- **Tips**: lai norādītu vērtības veidu, tiek izmantotas dubultās izsaukuma zīmes (!!).

``` jaml
a: !!peld 123
b: !!str 123
```

- **Tags**: lai piezīmei piešķirtu atzīmi, tiek izmantota & (&) un, lai atsauktos uz šo mezglu, tiek izmantota zvaigznīte (*).

``` jaml
vārds: Džons Smits
rēķina saņēmējs: &id01
iela: |
123 Tornado aleja
Suite numurs 16
pilsēta: East Centerville
valsts: KS

piegāde uz: *id01
```

- **Direktīvas**: pirms YAML dokumentiem straumē var ievietot direktīvas. Direktīvas sākas ar procentu zīmi (%), kam seko nosaukums un pēc tam parametri, kas atdalīti ar atstarpēm.

``` jaml
%YAML 1.2
  ---
Dokumenta saturs
```
## YAML faila piemērs
Tālāk ir redzams **docker yaml faila piemērs**:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Būtībā gan JSON, gan YAML ir izstrādāti, lai nodrošinātu cilvēkiem lasāmu datu apmaiņas formātu. YAML tiek realizēts kā JSON formāta superkopa. Tas nozīmē, ka mēs varam parsēt JSON, izmantojot YAML parsētāju. Lai gan šīs teorijas praktiskā īstenošana ir nedaudz sarežģīta. Tāpēc dažas pamata atšķirības starp YAML un JSON ir norādītas tālāk:

|YAML| JSON|
---|---|
|Sarežģīts un laikietilpīgs serializētu datu parsēšanas process |Ātri un viegli parsējiet JSON serializētos datus, izmantojot vienkāršāku dizainu|
|Mazāks kopienas atbalsts| Lielāks kopienas atbalsts un popularitāte|
|Atbalsta komentārus| Neatbalsta komentārus|
|Spēja izmantot atsauci uz citiem datu objektiem| Nav iespējams serializēt sarežģītas struktūras ar objektu atsaucēm|
|Hierarhija tiek apzīmēta, izmantojot dubultās atstarpes rakstzīmes. Tabulēšanas rakstzīmes nav atļautas|Objekti un masīvi ir apzīmēti iekavās un iekavās.|
|Virku pēdiņas nav obligātas, taču tā atbalsta vienpēdiņas un dubultpēdiņas.|Virknēm jābūt dubultpēdiņās.|
|Saknes mezgls var būt jebkurš no derīgajiem datu tipiem|Saknes mezglam ir jābūt masīvam vai objektam.|


## Atsauces Nr.

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

