{
  "date": "2019-10-11",
  "keywords": [
"arsc",
".arsc",
"kas ir arsc fails",
"kā atvērt arsc failu",
"pagarinājumu",
"failu",
"arsc failu",
"arsc faila formātā",
"arsc faila paplašinājums",
"arsc faila piemērs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARSC — Android pakotnes resursu tabulas fails ",
  "description": "Uzziniet par ARSC faila formātu un API, kas var izveidot un atvērt ARSC failu.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ars-lvc"
}
},
  "lastmod": "2021-06-22"
}

## Kas ir ARSC fails?

ARSC fails ir Android resursu tabulas fails, kas satur lietojumprogrammas resursu sarakstu tabulas formātā. Tas satur tādu informāciju kā resursu nosaukumi, rekvizīti un ID. ARSC faili ir daļa no APK pakotnēm, kas tiek izmantotas šo Android lietotņu instalēšanai. Visi resursi, piemēram, attēli, izkārtojumi, stili un virknes, Android lietojumprogrammā tiek pārvērsti bināros failos, kad tiek ģenerēts APK fails. Tajā pašā laikā tiek ģenerēts arī ARSC fails, kurā ir visu programmas apkopoto resursu saraksts un to ID.

## ARSC faila formāts

.arsc paplašinājuma faili ir bināri faili, kas ģenerēti pēc tam, kad kompilators, piemēram, ANT (Eclipse) vai Gradle (AS), apkopo Android lietojumprogrammas kodu, lai izveidotu [APK](/compression/apk/) failu. Varat izvilkt APK failu, izmantojot jebkuru arhivēšanas utilītu, piemēram, WinZip, lai skatītu tā saturu, kas ir apkopotie java klases faili, piemēram, classes.dex. Papildus tiem tajā ir arī šis ARSC fails, kas satur metainformāciju par:

 * XML mezgli
 * Atribūti
 * Resursu ID

Resursi APK failā tiek norādīti ar resursu ID, savukārt atribūtiem izpildlaikā tiek piešķirta vērtība. Android aapt rīks apkopo visus failos definētos resursus izveides laikā un piešķir tiem resursu ID. Pēc tam, kad apkopotajiem resursiem ir piešķirti identifikatori, R.java fails tiek ģenerēts no avota koda, kā arī no resursiem.arsc.

## Atsauces

* [Bināro resursu tabulas struktūra](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


