{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"TMP fails",
"TMP dokumenti",
"TMP faili",
"Pagaidu fails",
"pieteikumu",
"programmas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP — pagaidu faila formāts",
  "description": "Uzziniet par TMP faila formātu un API, kas var izveidot un atvērt TMP failus.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-lvp"
}
},
  "lastmod": "2021-07-15"
}

## Kas ir TMP fails? ##

TMP fails attiecas uz pārejošu dublējumu, krātuvi vai citu failu sistēmu, ko ģenerējusi programmatūra. Reizēm tas tiek izveidots kā neredzams fails un bieži tiek iznīcināts, kad programma tiek aizvērta. TMP failus var izmantot arī, lai īslaicīgi saglabātu informāciju, kamēr tiek veidots jauns fails.

## TMP faila formāts ##

TMP failu parasti veido neapstrādāti dati, kas tiek izmantoti kā fāze materiāla pārveidošanas procesā no viena stila uz citu. Microsoft Word un Apple Safari ir divas lietotnes, kas var izveidot un izmantot TMP faila formātu.

Ģenerētie TMP dokumenti teorētiski būtu automātiski jāizņem, kad programma tiek aizvērta vai iekārta tiek izslēgta. Praksē tas ne vienmēr notiek. Tā rezultātā, pārlūkojot programmas dokumentus, varat saskarties ar īslaicīgiem failiem, kurus sistēma vai cita programmatūra aktīvi neizmanto.

### Papildatmiņa ###

Operētājsistēmās tiek izmantota virtuālā atmiņa, taču programmām, kas izmanto lielu informācijas apjomu, var būt nepieciešams izveidot pagaidu dokumentus.

### Starpprocesu komunikācija ###

Lielākā daļa operētājsistēmu nodrošina primitīvus datu pārsūtīšanai starp programmām, piemēram, caurulēm, ligzdām vai galveno atmiņu, taču vienkāršākā metode ir pārsūtīt failus uz pagaidu failu un informēt saņēmēju lietojumprogrammu par pagaidu faila atrašanās vietu.


## Tehniskā specifikācija Nr.

Atšķirīgu pagaidu dokumentu nosaukumu iegūšanu parasti nodrošina operētājsistēmas un programmatūras.
Pagaidu failus var droši ģenerēt POSIX sistēmās, izmantojot bibliotēkas funkcijas mkstemp vai tmpfile. Dažās sistēmās ir iekļauta iepriekšējā POSIX (kopš vairs nav) mktemp lietojumprogramma. Šie faili parasti ir atrodami parastajā pagaidu direktorijā Unix platformās mapē /TMP vai %TEMP% (tas ir īpaši paredzēts pieteikšanās gadījumā) Windows datoros.

Kad programma apstājas vai dokuments tiek aizvērts, īslaicīgais fails, kas ģenerēts ar tmpfile, tiek automātiski noņemts. GetTempFileName (Windows) vai tmpnam (POSIX) var izmantot, lai izveidotu pagaidu faila nosaukumu, kas kalpos ilgāk nekā programma, kas to izveidoja.

## Atsauce Nr.

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
