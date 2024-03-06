{
  "date": "2021-06-24",
  "keywords": [
"DAĻA",
"daļēja",
"pagarinājumu",
"failu",
"formātā",
"tīmeklī",
"lejupielādēts"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DAĻA — daļēji lejupielādēts fails",
  "description": "Uzziniet par PART faila formātu un API, kas var izveidot un atvērt PART failus.",
  "linktitle": "PART",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-par-lvt"
}
},
  "lastmod": "2021-06-24"
}

## Kas ir PART fails? ##

Daļas fails vai .part paplašinājums ir daļēji lejupielādēts fails. To izmanto, kad notiek lejupielāde vai ir pārtraukta kāda problēma, dodot lejupielādes pārvaldniekam iespēju atsākt lejupielādi, kad vien iespējams.
Tas nozīmē, ka pārlūkprogramma, piemēram, Firefox vai failu pārsūtīšanas programmas, piemēram, eMule, eMule plus, FlashGet u.c., saglabā faila daļu, ko sauc par daļas failu, kamēr notiek lejupielāde jūsu ierīcē. Šis daļas fails parādīs, vai lejupielāde notiek vai ir pārtraukta pirms pabeigšanas. Ne tikai šis, bet arī PART fails saglabā visus datus, līdz lejupielāde ir pabeigta, tāpēc dažus no tiem vēlāk var atsākt, ja vēlaties atsākt lejupielādi.

## DAĻAS faila formāts ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
