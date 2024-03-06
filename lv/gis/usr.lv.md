{
  "date": "2023-08-03",
  "keywords": [
"usr",
"usr failu",
"kas ir usr fails",
"kā atvērt usr failu",
"failu",
"usr faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "USR faila formāts — Lowrance GPS datu fails",
  "description": "Uzziniet par USR formātu un API, kas var izveidot un atvērt USR failus.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr-lv",
      "parent": "gis"
}
},
  "lastmod": "2023-08-03"
}

## Kas ir USR fails?

Faila paplašinājums .usr ir saistīts arī ar Lowrance GPS ierīcēm. Jo īpaši to izmanto GPS datu glabāšanai formātā, kas pazīstams kā Lietotāja datu formāts (USR formāts), ko izmanto Lowrance GPS ierīces.

Izmantojot Lowrance GPS ierīci, jūs varat saglabāt savus ceļa punktus, pēdas un maršrutus kā .usr failus. Šajos failos parasti ir ietverta tāda informācija kā platums, garums, augstums virs jūras līmeņa, laikspiedols un citi dati, kas saistīti ar jūsu GPS darbībām.

Tālāk ir norādīti daži izplatīti .usr failu lietojumi Lowrance GPS ierīcēs.

- **Maršruta punkti:** maršruta punkti ir noteiktas vietas, kas atzīmētas GPS, piemēram, orientieri, iecienītākās makšķerēšanas vietas vai apskates vietas. Šīs atrašanās vietas varat saglabāt kā .usr failus, un tās var importēt, eksportēt vai koplietot ar citiem Lowrance GPS lietotājiem.

- **Tracks:** Trases attēlo jūsu GPS kustību ierakstīto ceļu. Varat saglabāt maršrutu žurnālus kā .usr failus, ļaujot vēlāk pārskatīt un analizēt maršrutus vai kopīgot tos ar citiem.

- **Maršruti:** Maršruti ir iepriekš noteikti ceļi, kurus varat izveidot un saglabāt savā GPS ierīcē. Šos maršrutus var arī saglabāt kā .usr failus turpmākai lietošanai vai koplietošanai.

Lai pārvaldītu .usr failus savā Lowrance GPS ierīcē, parasti izmantojat programmatūru, piemēram, Lowrance Insight Planner vai Lowrance GPS Utility, lai importētu, eksportētu un apstrādātu savus GPS datus.

## USR faila formāts — vairāk informācijas

Lowrance iFinder GPS ierīcēs .usr faili tiek izveidoti un saglabāti ierīcē ievietotajā MultiMediaCard (MMC) atmiņas kartē. Šajos failos ir ietverti lietotāja dati, piemēram, pieturas punkti, pēdas un maršruti.

Lai pārsūtītu .usr failus no MMC uz datoru, varat veikt šādas darbības:

- **Noņemiet MMC:** uzmanīgi izņemiet MultiMediaCard (MMC) no Lowrance iFinder GPS ierīces.

- **Ievietojiet MMC datorā:** izmantojiet atbilstošu MMC karšu lasītāju, lai ievietotu atmiņas karti datora karšu lasītāja slotā.

- **Atrodiet .usr failus:** Kad dators ir atpazinis MMC, jums vajadzētu būt iespējai piekļūt tajā saglabātajiem failiem. Meklējiet .usr failus, kas satur jūsu GPS datus.

- **Konvertēšana ar GPSBabel:** lai konvertētu .usr failus citā GPS formātā, varat izmantot GPSBabel, kas ir bezmaksas atvērtā koda rīks darbam ar dažādiem GPS failu formātiem. GPSBabel atbalsta plašu ievades un izvades formātu klāstu, ļaujot konvertēt .usr failus formātos, kas ir saderīgi ar citu GPS programmatūru vai ierīcēm.

Jūs varat lejupielādēt GPSBabel no oficiālās vietnes (http://www.gpsbabel.org/) un instalēt to savā datorā. Pēc instalēšanas varat izmantot programmatūras komandrindas interfeisu vai grafisko lietotāja interfeisu (ja pieejams), lai veiktu konvertēšanu.

Piemēram, ja vēlaties konvertēt .usr failus GPX formātā, varat izmantot šādu komandu:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Iepriekš minētā komanda uzdod GPSBabel nolasīt ievades failu input.usr Lowrance USR formātā un ierakstīt izvades failu output.gpx GPX formātā.

- **Konvertētu failu importēšana/izmantošana:** pēc konvertēšanas jūsu GPS dati būs jaunajā formātā (piemēram, GPX), ko varēsiet izmantot ar citu GPS programmatūru vai ierīcēm, kas atbalsta šo formātu.

## Kā atvērt USR failu?

Programmas, kas atver USR failus vai atsaucas uz tiem, ietver

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Atsauces
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)


