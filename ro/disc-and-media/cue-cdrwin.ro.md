{
"data":"2023-10-18",
   "keywords":[
"tac",
"fișier cue",
"fișier cue cdrwin cue sheet",
"cum se deschide un fișier cue",
"fişier",
"extensie fișier cue",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier CUE - CDRWIN Cue Sheet",
   "description":"Aflați despre formatul fișierului CUE CDRWIN Cue Sheet și despre API-urile care pot crea și deschide fișiere CUE.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
         "parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## Ce este un fișier CUE?

Un fișier **.CUE**, cunoscut și sub numele de **CDRWIN Cue Sheet**, este un fișier text simplu care conține informații despre melodiile și aspectul unui CD audio sau a unei imagini de disc, de obicei în format BIN sau ISO. Aceste fișiere sunt adesea folosite pentru a descrie structura și conținutul discului, permițând software-ului de inscripționare CD sau software-ului de unitate virtuală să reproducă cu acuratețe discul original.

## Exemplu de fișier CUE

Iată un exemplu despre cum ar putea arăta fișierul ".cue":

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Sheet

CDRWIN Cue Sheet este o variație specifică a formatului de fișier ".cue" utilizat de software-ul CDRWIN. CDRWIN este un software de inscripționare și creație de CD/DVD, iar foile sale ".cue" sunt concepute pentru a fi utilizate cu acest software. Aceste foi ".cue" conțin informații necesare pentru ca CDRWIN să creeze sau să inscripționeze cu precizie CD sau DVD.

Iată câteva detalii cheie specifice foilor de reper CDRWIN:

1. **Unic pentru CDRWIN**: foile ".cue" ale CDRWIN sunt în format proprietar specific software-ului CDRWIN. Deși au similarități cu fișierele standard ".cue", ele sunt adaptate pentru a funcționa cu funcțiile și setările CDRWIN.
    






2. **Interfață ușor de utilizat**: CDRWIN oferă o interfață ușor de utilizat pentru crearea și editarea foilor sale ".cue". Utilizatorii pot adăuga sau modifica informații despre piste, indexuri, goluri și alți parametri într-un mod ușor de utilizat.
    






3. **Tipuri de discuri compatibile**: CDRWIN Cue Sheets sunt utilizate în principal pentru crearea diferitelor tipuri de CD-uri și DVD-uri, inclusiv discuri de date, CD-uri audio, discuri în mod mixt și multe altele. Formatul permite utilizatorilor să specifice tipul și conținutul discului pe care doresc să-l creeze.
    






4. **Control asupra aspectului discului**: CDRWIN Cue Sheets oferă control detaliat asupra aspectului și structurii discului, inclusiv ordinea pistelor, setările de pauză/gap și orice alte preferințe specifice pe care utilizatorul le poate avea.
    






5. **Suport ISO și BIN**: CDRWIN poate funcționa atât cu formatele de imagine de disc ISO, cât și cu BIN. Foaia ".cue" specifică ce fișier imagine este utilizat pentru disc, asigurând sincronizarea corectă între indicii și imagine.
    






6. **Inscripționarea și extragerea**: Aceste foi ".cue" sunt cruciale atunci când inscripționați discuri sau extrageți piese de pe discuri folosind CDRWIN. Acestea ajută la asigurarea faptului că produsul final se potrivește cu aspectul și conținutul dorit.
    






7. **Backup și restaurare**: utilizatorii CDRWIN creează adesea foi ".cue" atunci când fac copii de siguranță ale CD-urilor sau DVD-urilor lor. Aceste foi pot fi utilizate ulterior pentru a restabili conținutul discului, inclusiv aspectul și sincronizarea piesei.

## Cum se deschide fișierul CUE?

CDRWIN Cue Sheets sunt concepute special pentru software-ul CDRWIN, deci sunt de obicei menite să fie deschise și utilizate în CDRWIN.

Programe care deschid sau fac referire la fișiere CUE

- CDRWIN
- Proiecte inteligente IsoBuster
- EZB Systems UltraISO

## Alte fișiere CUE

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.cue**.

**Disc și media**
- [CUE - Cue Sheet File](/ro/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/ro/disc-and-media/cue-cdrwin/)

## Referințe
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

