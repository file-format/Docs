{
"data": "2023-05-16",
  "keywords": [
"fișier sami",
"Ce este un fișier sami",
"exemplu de fișier sami",
"fişier",
"extensie de fișier sami",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fișier SAMI - fișier de schimb de subtitrări și metadate",
  "description":"Aflați despre formatul SAMI și despre API-urile care pot crea și deschide fișiere SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Ce este un fișier SAMI?

Un fișier cu extensia ".sami" se referă de obicei la un fișier de schimb de subtitrări și metadate (SAMI). SAMI este un format de subtitrare folosit pentru afișarea subtitrărilor sau a subtitrărilor în videoclipuri. A fost dezvoltat inițial de Microsoft pentru Windows Media Player.

Fișierele SAMI conțin informații de sincronizare și conținut text pentru subtitrări sau subtitrări, permițându-le să fie sincronizate cu o redare video. Formatul acceptă opțiuni de formatare de bază, cum ar fi stilul fontului, culoarea și poziționarea subtitrarilor pe ecran.

Fișierele SAMI sunt de obicei fișiere text simplu și pot fi deschise și editate folosind un editor de text. Conținutul unui fișier SAMI include de obicei o secțiune antet care oferă informații despre fișier, urmată de intrări individuale de subtitrare cu timpul și textul respectiv.

Iată un exemplu despre cum ar putea arăta un fișier SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Fișierele SAMI sunt utilizate în mod obișnuit împreună cu playere video sau playere media care acceptă afișarea subtitrarilor, cum ar fi Windows Media Player sau VLC Media Player. Playerul citește fișierul SAMI și sincronizează subtitrările cu conținutul video, permițând spectatorilor să citească subtitrările în timp ce vizionează videoclipul.

## Etichete HTML acceptate

Fișierele SAMI (Subtitles And Metadata Interchange) acceptă un set limitat de etichete asemănătoare HTML pentru formatarea și stilizarea subtitrărilor. Iată câteva dintre etichetele utilizate în mod obișnuit acceptate de SAMI:

-``<SAMI> :`` Elementul rădăcină care încapsulează întregul fișier SAMI.
-``<HEAD> :`` Conține informații de antet pentru fișierul SAMI.
<html>-``<TITLE> :`` Specifică titlul fișierului SAMI. </html>
-``<BODY> :`` Include intrările de subtitrare și informațiile de sincronizare ale acestora.
-``<SYNC> :`` Reprezintă un punct de sincronizare pentru o intrare de subtitrare. Specifică momentul în care ar trebui să fie afișat subtitrarea.
-``<P> :`` Include conținutul textului real al unui subtitrare. Este de obicei folosit în cadrul unui<SYNC> bloc.
<html>- `` <FONT>:`` Definește proprietățile fontului pentru textul inclus. Atribute precum Culoare, Față, Dimensiune și Stil pot fi folosite pentru a modifica aspectul fontului.</font>
-``<BR> :`` Inserează o întrerupere de linie într-un subtitrare.
<html>- `` <B>:`` Redă textul inclus cu aldine.</b>
<html>- `` <I>:`` Redă textul inclus cu caractere cursive.</i>
<html>- `` <U>:`` Redă textul inclus subliniat.</u>
-``<C> :`` Specifică poziția sau alinierea textului de subtitrare pe ecran. Acceptă atribute precum Centru, Mijloc, Stânga, Dreapta, Sus, Jos și combinațiile acestora.
-``<LANG> :`` Specifică codul de limbă pentru textul subtitrării. Ajută la identificarea limbii subtitrarilor.

Acestea sunt câteva dintre etichetele de bază acceptate de fișierele SAMI. Este important să rețineți că SAMI nu acceptă întreaga gamă de etichete și atribute HTML. Etichetele acceptate sunt axate în primul rând pe stilarea și poziționarea subtitrărilor, mai degrabă decât să ofere structurarea extinsă a documentelor sau interactivitate.

## Referințe
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

