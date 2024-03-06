{
  "date": "2021-08-24",
  "keywords": [
"wdb failu",
"wdb faila formātā",
"kas ir wdb fails",
"failu",
"wdb piemērs",
"wdb faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WDB faila formātu un API, kas var izveidot un atvērt WDB failus.",
  "title": "WDB — SQL servera izsekošanas fails",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-lvb"
}
},
  "lastmod": "2021-08-24"
}

## Kas ir WDB fails?
Fails ar paplašinājumu .wdb faktiski ir Microsoft Works izveidots datu bāzes fails, kas tika izmantots, lai veiktu tādas funkcijas kā datu bāzes pārvaldības sistēma. WDB fails ir līdzīgs Access Database ([MDB](/database/mdb/)) failam, taču tas ir mazāk efektīvs un ar lielākiem ierobežojumiem. WDB failus nevar atvērt, izmantojot Microsoft Access. Tomēr varat atvērt WDB failu programmā Microsoft Works un pēc tam eksportēt to uz MDB failu, lai atvērtu WDB failu programmā MS Access.

## WDB faila formāts
Microsoft Works datu bāze ir Microsoft Works biroja komplekta vietējais datu bāzes formāts. Formāta patentētā rakstura un dažu ierobežojumu dēļ. WDB failus nevar atvērt nevienā citā programmatūrā, izņemot Microsoft Works. Faila formātā pirms katras ASCII teksta virknes var atrast atkārtotu 10 baitu galveni, kas apzīmē to lauku vērtības, kuri tika pabeigti ar NULL vērtību. Galvenes parasti sākas ar **\x0f** baitu un NULL, kam seko 4 datu baiti, kas mijas ar NULL.

### Faila struktūra

WDB faila struktūra ir norādīta zemāk:
- **1. galvene**: no faila sākuma, kas beidzas ar \x25\x00\xf2 un 244 NULL baitiem
- **2. galvene**: sākas ar \xffT, ti, \xff\x54 un pagarina līdz 4096 baitiem, kas satur kolonnu/lauku nosaukumus un citas lietas, un šķiet, ka sākas ar 6144. baita pozīciju.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. datu baits 2 ir lauka numurs, datu baits 3 ir ieraksta numurs (pievienojot datu 3. baitu, 2. daļu, ja tas pārsniedz 256 ierakstus).


## Atsauces Nr.

* [Lietotājs:JesseW/wdb formāts](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


