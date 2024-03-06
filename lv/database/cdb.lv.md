{
  "date": "2021-06-16",
  "keywords": [
"CDB",
"pagarinājumu",
"cdb failu",
"cdb faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"kas ir cdb fails"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CDB failu formātu un API, kas var izveidot un atvērt CDB failus.",
  "title": "CDB — pastāvīgs datu bāzes fails",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-lvb"
}
},
  "lastmod": "2021-06-16"
}

## Kas ir CDB fails?
CDB faili tiek izmantoti misijai kritiskās lietojumprogrammās, piemēram, e-pastā. CDB apzīmē konstante datu bāze, ātra, uzticama un vienkārša pakotne konstantu datu bāzu izveidei vai lasīšanai. Datu bāzes nomaiņa ir droša pret sistēmas avārijām. Pārrakstīšanas laikā lietotājiem nav jāaptur. CDB darbojas kā asociatīvs masīvs (diskā), kartējot atslēgas ar vērtībām un ļauj vienā atslēgā saglabāt vairākas vērtības.

## CDB faila formāts

CDB faila formāts saglabā skaitļus, nobīdes, garumus un jaucējvērtības mazā formātā kā neparakstītus 32 bitu veselus skaitļus. Tiek uzskatīts, ka atslēgas un dati ir necaurredzamas baitu virknes bez īpašas apstrādes. Datubāzes sākumā fiksēta izmēra galvene attēlo 256 jaucējtabulas, norādot to atrašanās vietu failā un garumu slotos. Parasti dati tiek glabāti kā ierakstu secība, katrs ieraksts saglabā atslēgas garumu, datu garumu, atslēgu un datus. Nav šķirošanas vai izlīdzināšanas noteikumu. Ierakstiem seko 256 dažāda garuma jaucējtabulu komplekts. Tā kā nulle ir derīgs garums, datu bāzē var būt fiziski saglabātas mazāk nekā 256 jaucējtabulas, taču nekas netiek uzskatīts par 256 tabulām. Hash tabulas sastāv no virknes laika nišu, no kurām katra satur jaucējvērtību un ieraksta nobīdi. Tukšajām vietām ir nulles nobīde.

### CDB faila formāta struktūra

CDB datu bāze sastāv no visas datu kopas vienā datora failā. Tas satur trīs daļas:
- Fiksēta izmēra galvene
- Dati
- Hash tabulu komplekts.

Meklēšana ir pieejama tikai precīzām atslēgām. Uzmeklēšana darbojas, izmantojot šādu algoritmu:

- Sajauc atslēgu.
- Nosakiet, kurā hash tabulā un slotā šim ierakstam jāatrodas.
- Pārbaudiet norādīto slotu hash tabulā.

Meklējot atslēgas ar vairākām vērtībām, papildu vērtības var atrast, vienkārši atsākot meklēšanu nākamajā slotā.

#### Iespējas

CDB datu bāzes struktūra nodrošina vairākas funkcijas:

##### Ātra meklēšana
Veiksmīgai uzmeklēšanai milzīgā datubāzē parasti nepieciešamas tikai divas diska piekļuves, bet neveiksmīgai uzmeklēšanai nepieciešama tikai viena.
##### Zemas pieskaitāmās izmaksas
Datu bāzē tiek izmantoti 2048 baiti, 24 baiti katram ierakstam un vieta atslēgām un datiem.
##### Nav nejaušu ierobežojumu
CDB var pārvaldīt jebkuru datu bāzi līdz 4 gigabaitiem. Tā kā citu ierobežojumu nav, ierakstiem pat nav jāietilpst atmiņā. Datu bāzes tiek glabātas no mašīnas neatkarīgā formātā.
##### Ātra atomu datu bāzes nomaiņa
Komanda **cdbmake** var pārrakstīt visu datu bāzi divās kārtās ātrāk nekā citas jaukšanas pakotnes.
##### Ātras datu bāzes izgāztuves
**cdbdump** var izdrukāt datu bāzes saturu ar cdbmake saderīgā formātā.


## Atsauces Nr.

* [cdb (programmatūra) — Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))

* [CDB specifikācija] (http://cr.yp.to/cdb.html)


