{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AGI fails — zvaigznītes vārtejas interfeisa faila formāts",
  "description":"Uzziniet, kas ir AGI faila formāts, izmantojot piemēru un API, kas var izveidot un atvērt AGI failus.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas ir AGI fails?

AGI fails ir skripta fails, ko izmanto atvērtā pirmkoda telefonijas sistēma Asterisk. Tajā ir informācija, ko var izmantot, lai automatizētu procesus un Asterisk dialplan. Izmantojot AGI skriptu failus, var izveidot savienojumus ar relāciju datu bāzēm, piemēram, PostgreSQL vai MySQL. Turklāt AGI skriptus var izmantot, lai piekļūtu arī citiem ārējiem resursiem. AGI skripti var nodot numura sastādīšanas plāna vadību ārējam AGI skriptam, ļaujot zvaigznītei veikt sarežģītus uzdevumus.

## AGI faila formāts — vairāk informācijas

AGI skriptu faili tiek saglabāti kā teksta faili, un tos var atvērt jebkurā teksta redaktorā, lai veiktu izmaiņas.

### Standarta AGI komunikācijas modelis

AGI skripts ielādē mainīgos un to vērtības, ko tam nosūtījis zvaigznīte. Šo mainīgo kopējais izskats ir šāds.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Šiem mainīgajiem seko tukša rindiņa, ko nosūta Zvaigznīte, norādot, ka AGI skripts tagad var pārņemt sastādīšanas plānu.

### Programmēšanas valoda AGI skriptu failiem

AGI skriptus parasti var rakstīt programmā Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal vai Bourne Shell.

## Atsauces

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

