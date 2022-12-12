{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "fișier", "extensie", "format", "audio", "smaf", "extensie mmf", "fișiere mmf", "fișier de muzică mobil", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MMF și despre API-urile care pot crea și deschide fișiere MMF.",
  "title" :"MMF – Format fișier de muzică mobil",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Ce este un fișier MMF?

MMF este o extensie de fișier asociată cu un fișier SMAF. MMF înseamnă Fișier de muzică mobilă, în timp ce SMAF înseamnă Format de aplicație mobilă pentru muzică sintetică. Fișierele MMF dintr-un smartphone conțin tonuri de apel de sistem, sunet și pot conține, de asemenea, grafică și afișare text. MMF conține în plus trei tipuri de parametri ai instrumentului, inclusiv FM, PCM și Stream PCM. Aceste formate de fișiere sunt compatibile cu platforma de sistem Windows. Fișierele MMF sunt clasificate ca fișiere de date. De obicei, Microsoft Mail acceptă fișiere MMF. Fișierul cu sufix MMF poate fi copiat pe orice dispozitiv mobil sau platformă de sistem.

În plus, aceste fișiere sunt mult mai mici în comparație cu fișierele în format MIDI standard. Fișierele [WAV](/ro/audio/wav/) și [MID](/ro/audio/mid/) pot fi convertite în format MMF care pot fi apoi partajate și distribuite ca conținut audio. Aceste fișiere pot fi primite prin e-mail direct pe telefoane și PC.


## Scurt istoric al formatului de fișier MMF

Yamaha a dezvoltat instrumente SMAF ca fișiere de sunet, astfel încât smartphone-urile să poată stoca un număr mai mare de tonuri de apel unice. Yamaha a introdus SMAF odată cu producerea chipurilor lor de sunet MA-1, MA-2, MA-3, MA-5 și MA-7 LSI. Toate aceste formate devin destul de familiare în rândul telefoanelor mobile de pe piața din Asia de Est la începutul anului 2000.

La nivel internațional, formatul MMF a fost autorizat de Samsung. Cu ajutorul formatului MMF, Samsung a reușit să conceapă o gamă largă de tonuri de apel polifonice care să fie folosite în smartphone-urile Samsung.

Yamaha a vrut să facă formatul și mai popular și astfel, pe fișierele oficiale Yamaha SMAF, a publicat mai multe instrumente compatibile cu acest format. Cu aceasta, utilizatorii pot acum reda cu ușurință fișiere MMF pe computerele lor.


## Specificații pentru formatul fișierului MMF ##

Fișierele MMF sunt clasificate în secțiuni de date. O structură prefixată în jurul unui 8 octeți este folosită pentru a descrie fiecare segment.
Eticheta de 4 octeți include CNTI, OPDA, MSTR, MTR și ATR. Dimensiunea datelor plus 8 octeți este dimensiunea fragmentului; întreaga dimensiune a fișierului este calculată prin însumarea tuturor dimensiunilor bucăților. Dacă un fișier nu a fost deteriorat, dimensiunea însumată a fișierului ar trebui să fie aceeași cu dimensiunea antetului principal.

### Antet ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Iată un exemplu de fișier MMF:

![](../mmf.png)

## Referințe

* [MMF - De Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

