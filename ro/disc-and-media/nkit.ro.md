{
  "date" : "2022-04-01",
  "keywords" :[ "fișier nkit", "format fișier nkit", "ce este un fișier nkit", "fișier", "exemplu nkit", "extensie fișier nkit", "extensie", "format", "subsol nkit", "fișier formatul nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier NKIT și despre API-urile care pot crea și deschide fișiere NKIT.",
  "title" :"NKIT - Format fișier imagine disc",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Ce este un fișier NKIT?

Un fișier NKIT este o imagine de disc a datelor extrase din jocurile NintendoWii și GameCube. NKIT este pentru formatul Nintendo Toolkit. Fișierul de compresie [ISO](/ro/compression/iso/) rezultat utilizează datele principale ale acestor jocuri pentru a fi rulat cu programe de emulare precum Dolphin, Swiss și Nintendont. NKit vine în formate de fișiere brute (iso) și comprimate (gcz), ambele concepute ținând cont de capacitatea de redare și dimensiunea.

## Format de fișier NKIT

Formatul de fișier NKit este un format fără pierderi și este folosit pentru micșorarea și restaurarea imaginilor Nintendo Wii și GameCube. Formatele sunt disponibile în formatele de fișiere ISO și GCZ pentru fiecare dintre jocurile GameCube și Wii.

|Sistem |Format |Hardware acceptat |Dolphin acceptat |Restaurabil 1:1 |Note|
---|---|---|---|---|---|
|GameCube| nkit.iso| Da |Da| Da |La fel ca iso compacted GameCube|
|GameCube| nkit.gcz| Nu| Da| Da |GCZ este formatul de compresie care poate fi căutat prin blocuri al lui Dolphin|
|Wii| nkit.iso| Nu Da| Da| Formatul RVT-H poate fi redat numai în Dolphin|
|Wii| nkit.gcz| Nu Da| Da| RVT-H în GCZ poate fi redat numai în Dolphin|

### Antet NKIT

Antetul formatului de fișier NKIT este după cum urmează.

|Decalaj |Lungime |Nume|
---|---|---|
|0x200 |0x4 |Antetul NKit „NKIT”|
|0x204 |0x4 |Versiunea NKit „v01”|
|0x208 |0x4 |Imaginea sursă originală CRC32|
|0x20C |0x4 |NKit CRC - face ca fișierul NKit CRC32 să fie egal cu CRC sursă la 0x208 (la 0x4 în GCZ)|
|0x210 |0x4 |Lungimea imaginii sursă|
|0x214 |0x4 |Forced Junk ID (Când ID-ul discului diferă - rar - numai GameCube)|
|0x218 |0x4 |Wii Update partiția CRC32 dacă a fost eliminată la conversie|

## Referințe ##

* [Format de fișier NKIT - de gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

