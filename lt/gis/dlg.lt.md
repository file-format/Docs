{
  "date": "2021-07-30",
  "keywords": [
"dlg failą",
"dlg failo formatas",
"kas yra dlg failas",
"failą",
"dlg pavyzdys",
"dlg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "DLG – Shapefile Shape Index formatas",
  "description": "Sužinokite apie DLG failo formatą ir API, kurios gali kurti ir atidaryti DLG failus.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dl-ltg"
}
},
  "lastmod": "2021-07-30"
}

## Kas yra DLG failas?
Faile su plėtiniu .dlg yra skaitmeninė linijinė diagrama, kuri yra kartografinio žemėlapio funkcija, rodoma skaitmenine vektorine forma, kurią administruoja JAV geologijos tarnyba (USGS). DLG failai galimi dviem skirtingais formatais:
1. **Pasirenkamas formatas**: paprastas naudoti formatas, apimantis 80 baitų loginį įrašo ilgį, UTM žemės koordinačių sistemą ir topologijos ryšius, esančius linijos, mazgo ir srities elementuose.
2. **Erdvinių duomenų perdavimo standarto (SDTS) formatas**: formatas, palengvinantis erdvinių duomenų perdavimą tarp skirtingų kompiuterių sistemų.

## DLG failo formatas
DLG failo formatas yra skirtas USGS žemėlapiams ir yra perduodamas dideliu, vidutiniu ir mažu masteliu su iki devynių skirtingų funkcijų kategorijų. DLG failai yra pasirenkami ir erdvinio duomenų perdavimo standarto (SDTS) formatai, turintys topologinę struktūrą, skirtą naudoti žemėlapių ir GIS programose.
### DLG failo formato specifikacijos
DLG failai platinami trimis skirtingais masteliais:

1. **Didelės apimties** – paprastai atitinka:
- USGS 7,5–7,5 minutės
– 1:24 000 ir 1:25 000 mastelio topografinių keturkampių žemėlapių serijos
- 1:63 360 masteliu Aliaskai
- 1:30 000 masteliu Puerto Rike
 
2. **Tarpinė skalė** – gauta iš USGS: 
- 30 - 60 minučių
– 1:100 000 mastelio žemėlapių serijos
3. **Mažas mastelis** – gautas iš USGS 1:2 000 000 mastelio Jungtinių Valstijų nacionalinio atlaso pjūvių žemėlapių
### Duomenų kategorijos
Nine different categories of layers, or features, are available in DLG files:
1. Viešoji žemės matavimo sistema (PLSS)
2. Ribos (BD)
3. Transportas (TR)
4. Hidrografija (HY)
5. Hipsografija (HP)
6. Ne vegetatyvinės savybės (NV)
7. Apklausos valdymas ir žymekliai (SM) 
8. Žmogaus sukurtos funkcijos (MS) 
9. Vegetatyvinio paviršiaus danga (SC)

Didelės apimties DLG failai siūlo visus devynis sluoksnius, o vidutinio masto – penkis PLSS, BD, TR, HY ir HP sluoksnius. Mažos apimties DLG siūlo penkis PLSS, BD, TR, HY ir MS sluoksnius.

## Nuorodos

* [Skaitmeninė linijinė diagrama – Vikipedija)](https://en.wikipedia.org/wiki/Digital_line_graph)



