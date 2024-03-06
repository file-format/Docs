{
  "date": "2021-04-22",
  "keywords": [
"aps fails",
"Visual Studio aps fails",
"pagarinājumu",
"formātā",
"aps fails vizuālā studija",
"aps faila paplašinājums",
"kā atvērt aps failu",
"APS faila formāts"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "APS — Visual C++ resursu fails",
  "description": "Uzziniet par APS faila formātu, izmantojot APS piemēru un API, kas var izveidot un atvērt APS failus.",
  "linktitle": "APS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ap-lvs"
}
},
  "lastmod": "2021-04-22"
}

## Kas ir APS faila formāts?
APS failu izveido Microsoft programmatūras izstrādes lietojumprogramma Visual C++. Tas saglabā projektā iekļautā resursa bināro attēlojumu un ļauj lietojumprogrammai ātrāk ielādēt resursus. Jūs varat viegli atrast šos failus ar .aps faila paplašinājumu. Faktiski resursu redaktori tieši nelasa resource.h failus, tāpēc resursu kompilators tos apkopo .aps failos, kurus patērē resursu redaktori.

## APS faila formāts
APS faila formāts ir tikai kompilēšanas darbība, un tajā tiek glabāti tikai simboliski dati. Nesimboliskā informācija, piemēram, komentēšana, kompilēšanas procesā tiek izmesta. Piemēram, kad jūs saglabājat, resursu redaktors pārraksta resursa skripta failu un failu resource.h. Visas izmaiņas pašos resursos paliek iekļautas resursa skripta failā, taču komentāri vienmēr tiks zaudēti, tiklīdz resursa skripta fails tiks pārrakstīts.


## Atsauces

 * [Resursu faili (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 

