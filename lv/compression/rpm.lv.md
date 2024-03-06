{
  "date": "2021-04-08",
  "keywords": [
"rpm fails",
"rpm faila formāts",
"kas ir rpm fails",
"failu",
"apgr./min piemērs",
"rpm faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RPM — Red Hat pakotņu pārvaldnieka fails",
  "description": "Uzziniet par RPM faila formātu un API, kas var izveidot un atvērt RPM failus.",
  "linktitle": "RPM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rp-lvm"
}
},
  "lastmod": "2021-04-09"
}

## Kas ir RPM fails?

Fails ar paplašinājumu .rpm ir Red Hat Linux operētājsistēmas pakotne programmu instalēšanai Linux sistēmās. Red Hat pakotņu pārvaldnieks izmanto RPM faila formātu un ir bezmaksas atvērtā koda pakotņu pārvaldības sistēma. Lai gan RPM failus var izmantot tādus, kādi tie ir programmu instalēšanai, tos var pārvērst citos pakotņu formātos, piemēram, [DEB](/compression/deb/), izmantojot Debian programmu Alien.

## RPM faila formāts

RPM fails ir binārs fails, kas var saturēt failu kopu. Vairumā gadījumu RPM faili ir bināri RPM, kas ir programmatūras apkopotie izpildāmie faili. RPM failā var būt avota RPM (SRPM), ko var izmantot, lai izveidotu pakotni no avota koda. RPM faila formāts sastāv no četrām sadaļām.

 * Svins — tas identificē failu kā RPM failu
 * Paraksts — to var izmantot, lai nodrošinātu integritāti un/vai autentiskumu
 * Galvene — satur metadatus, tostarp pakotnes nosaukumu, versiju, arhitektūru, failu sarakstu utt.
 * Failu arhīvs — pazīstams arī kā lietderīgā slodze, kas parasti ir cpio formātā, saspiests ar [GZIP] (/compression/gz/)

## Atsauces

* [RPM — Wikipedia](https://rpm.org)

* [RPM dokumentācija](https://rpm.org/documentation.html)


