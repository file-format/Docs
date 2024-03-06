{
  "date": "2021-07-29",
  "keywords": [
"pes fails",
"pes faila formātā",
"kas ir pes fails",
"failu",
"pes piemērs",
"pes faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PES faila formāts - Brother PE izšūšanas formāts",
  "description": "Uzziniet par PES failu formātu un API, kas var izveidot un atvērt PES failus.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pe-lvs"
}
},
  "lastmod": "2021-07-29"
}

## Kas ir PES izšūšanas fails?

PES izšūšanas fails ir dizaina fails, kurā ir instrukcijas izšūšanas/šujmašīnām. To izstrādāja Brother Industries savām izšūšanas mašīnām, taču vēlāk tas tika formalizēts kā vispārējs faila formāts. Šujmašīnas izmanto PES failus, lai izlasītu instrukcijas paraugu uzšūšanai uz auduma. Šie faili kalpo diviem mērķiem; Pirmkārt, sniedzot dizaina informāciju lietojumprogrammai PE-Design, ko izstrādājusi Brother Industries, un, otrkārt, sniedzot dizaina nosaukumu, krāsas un izšūšanas mašīnu kodus, piemēram, stop, jump un trim.

## PES faila formāts — vairāk informācijas

PES fails tiek saglabāts diskā binārā faila formātā. Tajā ir vairākas sadaļas, kurās ir informācija par šūšanu, kas saglabāta, izmantojot iepriekš noteiktu metodi. PES faila formāts ir šāds.

 * Versijas dati — sniedz informāciju par versiju, un tā var būt jebkura vērtība #PES0001, #PES0020, #PES0030, #PES0040, #PES0050, #PES0055, #PES0060.
 * PEC meklēšanas vērtība — 4 baitu maza gala vesels skaitlis, kas tūlīt seko versijas datiem un apzīmē meklēšanas vērtību PEC sadaļai, kurā ir informācija par dizainu.
 * PSE sadaļa — satur informāciju par dizainu, kas attiecas uz Brother PE-Design, un var būt arī citi šūšanas pielietojumi
 * PCE sadaļa — var atrasties jebkur PSE failā, bet uz to norāda PEC meklēšanas vērtība.

## Šujmašīnu veids, izmantojot PES failu

PES failus galvenokārt veido PE-Design programmatūra, kas tiek izmantota kopā ar Brother šujmašīnām. Dažas citas mašīnas, kas var atbalstīt PES failus, ietver Babylock un Bernina mājas izšūšanas mašīnas.

## Kā konvertēt PSE failus?

Programmatūras lietojumprogramma PE-Design var [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) uz citiem formātiem, piemēram, .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd vai .xxx. . To var izdarīt, izmantojot lietojumprogrammu PE-Design, atverot failu un izvēloties konvertēšanas formātu.

## Atsauces

* [PE dizains — instrukciju rokasgrāmata](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)


