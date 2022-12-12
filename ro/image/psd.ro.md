{
  "date" : "2019-10-11",
  "keywords" :[ "fișier psd", "format fișier psd", "ce este un fișier psd", "fișier", "exemplu psd", "extensie fișier psd", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Format de fișier imagine Photoshop",
  "description":"Aflați despre formatul de fișier PSD și despre API-urile care pot crea și deschide fișiere PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PSD?

PSD, Photoshop Document, reprezintă formatul nativ de fișier Adobe Photoshop utilizat pentru proiectarea și dezvoltarea grafică. Fișierele PSD pot include straturi de imagine, straturi de ajustare, măști de straturi, adnotări, informații despre fișiere, cuvinte cheie și alte elemente specifice Photoshop. Fișierele Photoshop au extensia implicită ca .PSD și au o înălțime și lățime maximă de 30.000 de pixeli și o limită de lungime de doi gigaocteți.

## Specificații format fișier PSD ##

Datele dintr-un fișier PSD sunt stocate în ordinea octeților big endian. Aceasta implică schimbarea numerelor întregi scurte și lungi atunci când citiți sau scrieți pe platforma Windows. Formatul de fișier Photoshop este împărțit în cinci părți majore. Are mulți marcatori de lungime care pot fi folosiți pentru a trece de la o secțiune la alta. Markerii de lungime sunt de obicei umpluți cu octeți pentru a se rotunji la cel mai apropiat interval de 2 sau 4 octeți. Cele cinci părți majore sunt:

* Antet fișier
* Date despre modul de culoare
* Resurse de imagine
* Informații despre strat și mască
* Date de imagine

Pentru conformitate, datele ar trebui să fie scrise în toate aceste câmpuri din secțiune, deoarece Photoshop poate încerca să citească întreaga secțiune. De asemenea, implică faptul că zerourile să fie scrise în câmpurile omise în timp ce scrieți într-un fișier. Câmpul de lungime din secțiunile delimitate de lungime ar trebui utilizat pentru a decide când să se oprească citirea. În cele mai multe cazuri, câmpul de lungime indică numărul de octeți, nu de înregistrări, care urmează. Următoarele puncte trebuie reținute în timpul citirii unui fișier.

* Valorile din coloana „Lungime” din toate tabelele sunt exprimate în octeți.
* Toate valorile definite ca șir Unicode constau din:
* Un câmp de lungime de 4 octeți, reprezentând numărul de caractere din șir (nu octeți).
* Șirul de valori Unicode, doi octeți per caracter.

### Antet fișier ###

Antetul fișierului conține proprietățile de bază ale imaginii.

|Lungime|Descriere
---|---|
|4|Semnătura: întotdeauna egală cu „8BPS” . Nu încercați să citiți fișierul dacă semnătura nu corespunde acestei valori.
|2|Versiune: întotdeauna egală cu 1. Nu încercați să citiți fișierul dacă versiunea nu corespunde acestei valori. (~*~*PSB~*~* versiunea este 2.)
|6|Rezervat: trebuie să fie zero.
|2|Numărul de canale din imagine, inclusiv canalele alfa. Intervalul acceptat este de la 1 la 56.
|4|Înălțimea imaginii în pixeli. Intervalul acceptat este de la 1 la 30.000.
|4|Lățimea imaginii în pixeli. Intervalul acceptat este de la 1 la 30.000.
|2|Depth: numărul de biți pe canal. Valorile acceptate sunt 1, 8, 16 și 32.
|2|Modul de culoare al fișierului. Valorile acceptate sunt: Bitmap # 0; Tonuri de gri # 1; Indexat # 2; RGB # 3; CMYK # 4; Multicanal # 7; Duoton # 8; Laboratorul #9.

### Secțiunea de date mod culoare ###

Secțiunea de date pentru modul de culoare este structurată după cum urmează:


|Lungime|Descriere
---|---|
|4|Lungimea următoarelor date de culoare
|variabilă|Datele de culoare

Datele modului de culoare sunt disponibile numai pentru culoarea indexată și duoton, așa cum este definit de câmpul de mod din secțiunea Antet fișier. Pentru toate celelalte moduri, această secțiune este reprezentată de valori zero pe 4 octeți. Pentru imaginile color indexate, lungimea este de 768, iar datele de culoare conțin tabelul de culori pentru imagine, în ordinea neintercalată. Pentru imaginile Duotone, datele de culoare conțin specificația duotone (al cărei format nu este documentat). Alte aplicații care citesc fișiere Photoshop pot trata o imagine duotonă ca pe o imagine gri și pot păstra doar conținutul informațiilor biton atunci când citesc și scriu fișierul.

### Secțiunea Resurse de imagine ###

A treia secțiune a fișierului conține resurse de imagine. Începe cu un câmp de lungime, urmat de o serie de blocuri de resurse.


|Lungime|Descriere
---|---|
|4|Lungimea secțiunii de resurse de imagine. Lungimea poate fi zero.
|Variabilă|Resurse de imagine (Blocuri de resurse de imagine)

Resursele de imagine sunt folosite pentru a stoca date non-pixel asociate cu imagini, cum ar fi traseele instrumentului stilou. Acestea sunt denumite blocuri de resurse deoarece dețin date care au fost stocate în resursa Macintosh în versiunile inițiale ale Photoshop. Structura de bază a blocurilor de resurse de imagine este prezentată mai jos:


|Lungime|Descriere
---|---|
|4|Semnătura: „8BIM”
|2|Identificator unic pentru resursă. ID-urile de resurse de imagine conțin o listă de ID-uri de resurse utilizate de Photoshop.
|Variabilă|Nume: șir Pascal, completat pentru a face dimensiunea uniformă (un nume nul este format din doi octeți de 0)
|4|Dimensiunea reală a datelor despre resurse care urmează
|Variabilă|Datele despre resurse, descrise în secțiunile despre tipurile individuale de resurse. Este căptușită pentru a uniformiza dimensiunea.

Resursele de imagine folosesc mai multe numere de identificare standard.

### Informații despre strat și mască ###

A patra secțiune a unui fișier Photoshop conține informații despre straturi și măști, cum ar fi numărul de straturi, canalele din straturi, intervalele de amestecare, tastele straturilor de ajustare, straturile de efecte și parametrii măștii. Dacă nu există straturi sau măști, această secțiune este reprezentată de un câmp de 4 octeți cu zero. O atenție deosebită trebuie acordată lungimii secțiunilor în timpul citirii acestei secțiuni din cauza valorilor zero. Aranjamentul secțiunii Layer și Mask este după cum urmează:


|Lungime|Descriere
---|---|
|4|Lungimea stratului și secțiunea de informații despre mască. (Lungimea PSB este de 8 octeți.)
|Variabilă|Informații despre strat
|Variabilă|Informații globale despre mască de strat
|Variabilă|Serii de blocuri etichetate care conţin diverse tipuri de date.

#### Informații despre strat ####

Următorul tabel arată organizarea la nivel înalt a informațiilor de nivel.


|Lungime|Descriere
---|---|
|4|Lungimea secțiunii de informații despre straturi, rotunjită la un multiplu de 2. (lungimea PSB este de 8 octeți.)
|2|Număr de straturi. Dacă este un număr negativ, valoarea sa absolută este numărul de straturi, iar primul canal alfa conține datele de transparență pentru rezultatul îmbinat.
|Variabilă|Informații despre fiecare strat. A se vedea înregistrările stratului descrie structura acestor informații pentru fiecare strat.
|Variabilă|Datele imaginii canalului. Conține una sau mai multe înregistrări de date de imagine pentru fiecare strat. Straturile sunt în aceeași ordine ca și în informațiile despre strat

### Date imagine ###

Datele de pixeli ale imaginii sunt conținute în secțiunea Date de imagine a fișierului. Aranjarea datelor în secțiunea Date de imagine este în ordine plană, adică mai întâi toate datele roșii, apoi toate datele verzi etc. Fiecare plan este stocat în ordinea liniei de scanare, fără octeți de blocare. Secțiunea de date a imaginii este aranjată într-un format după cum se arată în tabelul următor.

|Lungime|Descriere
---|---|
|2|Metoda de comprimare: *0 = date brute de imagine * 1 = RLE comprimate, datele imaginii încep cu numărătoarea de octeți pentru toate liniile de scanare (rânduri * canale), fiecare număr fiind stocat ca valoare de doi octeți. Urmează datele comprimate RLE, fiecare linie de scanare comprimată separat. Compresia RLE este același algoritm de compresie folosit de rutina ROM Macintosh PackBits și standardul TIFF. *2 = ZIP fără predicție *3 = ZIP cu predicție.
|Variabilă|Datele imaginii. Ordine plană = RRR GGG BBB etc.

## Referințe ##

* [Specificații de format de fișier PSD - de Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Format de fișier Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

