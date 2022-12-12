{
  "date" : "2019-10-11",
  "keywords" :[ "fișier png", "format fișier png", "ce este un fișier png", "fișier", "exemplu png", "extensie fișier png", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PNG - Fișier imagine raster",
  "description":"Aflați despre formatul de fișier PNG și despre API-urile care pot crea și deschide fișiere PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PNG?

Un fișier **PNG** (Portable Network Graphics) este un format de fișier imagine raster care utilizează compresie fără pierderi. Acest format de fișier a fost creat ca înlocuitor al Graphics Interchange Format ([GIF](/ro/image/gif/)) și nu are limitări ale drepturilor de autor. Cu toate acestea, formatul de fișier PNG nu acceptă animații. Formatul de fișier PNG acceptă compresia fără pierderi de imagine, ceea ce îl face popular în rândul utilizatorilor săi. Odată cu trecerea timpului, PNG a evoluat ca unul dintre formatele de fișiere de imagine utilizate pe scară largă.

## Scurt istoric al formatului de fișier PNG

Motivul principal din spatele creării formatului de fișier PNG a fost algoritmul de compresie patentat, Lempel-Ziv-Welch, utilizat în formatul de fișier GIF. Acest lucru împreună cu alte limitări GIF a creat necesitatea înlocuirii formatului de fișier [**GIF**](/ro/image/gif/). Prima propunere și numele pentru formatul de fișier PNG au venit în ianuarie 1995. Evenimentele cheie cu privire la formatele de fișier PNG sunt enumerate mai jos:

* Octombrie 1996: Specificațiile PNG Versiunea 1.0 au fost lansate și mai târziu au apărut ca [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Aceeași a devenit o recomandare W3C în octombrie 1996.
* Decembrie 1998: Versiunea 1.1, cu câteva mici modificări și adăugarea a trei noi bucăți, a fost lansată.
* August 1999: Versiunea 1.2, adăugând o bucată suplimentară, a fost lansată.
* Noiembrie 2003: PNG a devenit un standard internațional (ISO/IEC 15948:2003). Această versiune de PNG diferă doar puțin de versiunea 1.2 și nu adaugă fragmente noi.
* Martie 2004: ISO/IEC 15948:2004

## Comparație funcțională între GIF și PNG

Formatul de fișier PNG a fost conceput pentru a fi simplu și portabil, fără grevări din punct de vedere legal, interschimbabil, flexibil și robust. Următorul tabel listează caracteristicile GIF care sunt moștenite de formatul de fișier PNG pe lângă funcțiile noi.

|Caracteristică|GIF|PNG|
---|---|---|
|Imagini cu index de culoare de până la 256 de culori|Da|Da|
|Suport pentru streaming|Da|Da|
|Transparență|Da|Da|
|Informații auxiliare|Da|Da|
|Independență hardware și platformă|Da|Da|
|Eficient|Da|Da|
|Imagini Truecolor de până la 48 de biți per pixel|Nu|Da|
|Imagini în tonuri de gri de până la 16 biți per pixel|Nu|Da|
|Canal alfa complet (măști generale de transparență)|Nu|Da|
|Informații gama imaginii|Nu|Da|
|Fiabilitate|Nu|Da|
|Prezentare inițială mai rapidă|Nu|Da|

## Structura fișierului PNG

Aproape toate sistemele de operare au suport pentru deschiderea fișierelor PNG. De exemplu, vizualizatorul Microsoft Windows are capacitatea de a deschide fișiere PNG, deoarece sistemul de operare are în mod implicit suportul disponibil ca parte a instalării. Un fișier PNG constă dintr-o „semnătură” PNG urmată de o serie de //bucăți//.

### Antet fișier PNG

Primii opt octeți ai unui fișier PNG conțin întotdeauna următoarele valori (zecimale):

{{{137 80 78 71 13 10 26 10 }}}

Această semnătură indică faptul că restul fișierului conține o singură imagine PNG, constând dintr-o serie de bucăți care încep cu o bucată IHDR și se termină cu o bucată IEND.

### Bucăți ###

Fiecare bucată este formată din patru părți:

**Lungime:** Un întreg fără semn de 4 octeți care indică numărul de octeți din câmpul de date al fragmentului. Lungimea contează doar câmpul de date, nu el însuși, codul de tip chunk sau CRC. Zero este o lungime validă. Deși codificatoarele și decodoarele ar trebui să trateze lungimea ca nesemnată, valoarea acesteia nu trebuie să depășească 231 de octeți.

**Tip de fragment:** Un cod de tip de fragment de 4 octeți. Pentru comoditate în descriere și în examinarea fișierelor PNG, codurile de tip sunt limitate la litere ASCII majuscule și mici (AZ și az sau 65-90 și 97-122 zecimale). Cu toate acestea, codificatoarele și decodificatoarele trebuie să trateze codurile ca valori binare fixe, nu șiruri de caractere. De exemplu, nu ar fi corect să se reprezinte codul de tip IDAT prin echivalentele EBCDIC ale acelor litere. Convențiile suplimentare de denumire pentru tipurile de bucăți sunt discutate în secțiunea următoare.

**Chunk Data:** octeții de date corespunzători tipului de fragment, dacă există. Acest câmp poate fi de lungime zero.

**CRC:** Un CRC de 4 octeți (Verificare a redundanței ciclice) calculat pe octeții precedenți din fragment, inclusiv codul tipului de fragment și câmpurile de date ale blocului, dar fără a include câmpul de lungime. CRC este întotdeauna prezent, chiar și pentru bucăți care nu conțin date.

Lungimea de date a blocului poate fi orice număr de octeți până la maximum; prin urmare, implementatorii nu pot presupune că bucățile sunt aliniate pe orice graniță mai mare decât octeții.

Bucățile pot apărea în orice ordine, sub rezerva restricțiilor impuse fiecărui tip de bucată. (O restricție notabilă este că IHDR trebuie să apară primul și IEND trebuie să apară ultimul; astfel, fragmentul IEND servește ca un marcator de sfârșit de fișier.) Pot apărea mai multe bucăți de același tip, dar numai dacă sunt permise în mod specific pentru acel tip.

#### Tipuri de bucăți

Tipurile de bucăți sunt clasificate în bucăți **Critice** și **Ancillary** pe baza valorii ASCII de 4 octeți, care ține seama de majuscule și minuscule, alocată Tipului de bloc. Toate implementările trebuie să înțeleagă și să redă cu succes bucățile critice standard. O imagine PNG validă trebuie să conțină o bucată IHDR, una sau mai multe bucăți IDAT și o porțiune IEND.

### Compresie

Metoda de compresie PNG 0 (singura metodă de compresie definită în prezent pentru PNG) specifică compresia de dezumflare/umflare cu o fereastră glisantă de cel mult 32768 de octeți. Compresia Deflate este un derivat LZ77 utilizat în zip, gzip, pkzip și în programele conexe. Au fost efectuate cercetări ample pentru a susține statutul său fără brevet. Datele comprimate din fluxul de date zlib sunt stocate ca o serie de blocuri, fiecare dintre acestea putând reprezenta date brute (necomprimate), date comprimate LZ77 codificate cu coduri Huffman fixe sau date comprimate LZ77 codificate cu coduri Huffman personalizate. Un bit marcator din blocul final îl identifică ca ultimul bloc, permițând decodorului să recunoască sfârșitul fluxului de date comprimat.

#### Filtrare pre-compresie

Filtrele de precompresie sunt aplicate pentru a pregăti datele imaginii pentru o compresie optimă. Metoda de filtrare PNG definește cinci tipuri de filtre de bază, după cum urmează:

|Tip filtru|Nume|Valoare estimată|
---|---|---|
|0|Niciuna|Linia de scanare este transmisă nemodificat|
|1|Sub|Transmite diferența dintre fiecare octet și valoarea octetului corespunzător pixelului anterior.|
|2|Sus|Filtrul Up() este la fel ca filtrul Sub() cu excepția faptului că pixelul imediat deasupra pixelului curent, mai degrabă decât doar din stânga acestuia, este folosit ca predictor.|
|3|Medie|Filtrul Average() folosește media celor doi pixeli vecini (stânga și deasupra) pentru a prezice valoarea unui pixel.|
|4|Paeth|Filtrul Paeth() calculează o funcție liniară simplă a celor trei pixeli învecinați (stânga, sus, stânga sus), apoi alege ca predictor pixelul vecin cel mai apropiat de valoarea calculată.|

Algoritmii de filtrare sunt aplicați la „octeți”, nu la pixeli, indiferent de adâncimea de biți sau tipul de culoare al imaginii. Algoritmii de filtrare lucrează pe secvența de octeți formată dintr-o linie de scanare. Dacă imaginea include un canal alfa, datele alfa sunt filtrate în același mod ca și datele imaginii.

Când imaginea este întrețesă, fiecare trecere a modelului de întrețesere este tratată ca o imagine independentă în scopuri de filtrare. Filtrele lucrează pe secvențele de octeți formate din pixelii efectiv transmiși în timpul unei treceri, iar „linia de scanare anterioară” este cea transmisă anterior în aceeași trecere, nu cea adiacentă în imaginea completă. Rețineți că subimaginea transmisă într-o singură trecere este întotdeauna dreptunghiulară, dar are o lățime și/sau înălțime mai mică decât imaginea completă. Filtrarea nu este aplicată când această imagine secundară este goală.

## Referințe ##

* [PNG - Pagina de pornire](http://www.libpng.org/pub/png/)

