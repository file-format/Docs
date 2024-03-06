{
  "date": "2022-02-16",
  "keywords": [
"obb failu",
"obb faila formātā",
"kas ir Obb fails",
"failu",
"obb piemērs",
"obb faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBB faila formāts — Android necaurspīdīgs binārais blob fails",
  "description": "Uzziniet par OBB failu formātu un API, kas var izveidot un atvērt OBB failus.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ob-lvb"
}
},
  "lastmod": "2022-02-16"
}

## Kas ir OBB fails?

OBB fails ir paplašināšanas fails, kas satur papildu datus, kas ir papildus Android [APK](/compression/apk/) failam. Google Play veikalā nav atļauts izmantot Android APK failu, kura izmērs pārsniedz 100 MB. Taču dažām lietojumprogrammām papildus APK failiem var būt nepieciešama augstas izšķirtspējas grafika, multivides faili vai citi lieli līdzekļi. Šeit tiek izmantoti OBB failu tipi. Google Play ļauj pievienot šos paplašināšanas failus kā papildinājumu APK failam.

## OBB faila formāts

OBB faili tiek saglabāti kā bināri faili kopā ar APK failiem. Kad OBB failiem tiek pievienots APK, Google Play mitina paplašināšanas failus savā serverī, un no izstrādātāja netiek iekasēta papildu maksa. Kad lietotne tiek lejupielādēta instalēšanai, šie papildu faili tiek saglabāti ierīces koplietotajā krātuvē SD kartē vai USB montējamā nodalījumā.

OBB faili tiek lejupielādēti un instalēti pēc lejupielādes. Bet dažos gadījumos tie tiek lejupielādēti instalēšanai, kad lietojumprogramma tiek palaista pirmo reizi.

### OBB maksimālais faila lielums

Google Play veikals ļauj augšupielādēt OBB paplašināšanas failus, kuru lielums nepārsniedz 2 GB. Liela izmēra failus ieteicams augšupielādēt kā saspiestus [ZIP](/compression/zip/) failus efektīvai augšupielādei, izmantojot internetu.

Šos paplašināšanas failus var mitināt vai nu kā **galveno** primāro paplašināšanas failu papildu resursiem, kas nepieciešami lietotnei, vai kā izvēles ielāpu paplašināšanas failu, kas paredzēts nelieliem galvenā paplašināšanas faila atjauninājumiem.

## Atsauces

* [Android izstrādātāji — paplašināšanas faili](https://developer.android.com/google/play/expansion-files)


