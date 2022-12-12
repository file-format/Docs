{
  "date" : "2019-10-11",
  "keywords" :[ "fișier djvu", "format fișier djvu", "ce este un fișier djvu", "fișier", "exemplu djvu", "extensie fișier djvu", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier DJVU",
  "description":"Aflați despre formatul de fișier DJVU și despre API-urile care pot crea și deschide fișiere DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DJVU?

DjVu, pronunțat ca „déjà vu”, este un format de fișier grafic destinat documentelor și cărților scanate, în special celor care conțin o combinație de text, desene, imagini și fotografii. A fost dezvoltat de AT&T Labs. Utilizează mai multe tehnici precum separarea stratului de imagine a textului și a imaginilor de fundal, încărcare progresivă, codare aritmetică și compresie cu pierderi pentru imaginile bitonale. Deoarece fișierul DJVU poate conține imagini color, fotografii, text și desene comprimate, dar de înaltă calitate și poate fi salvat în mai puțin spațiu, prin urmare, este folosit pe web ca cărți electronice, manuale, ziare, documente antice etc.

DjVu poate fi clasificat ca alternativă superioară [PDF](/ro/pdf/). Extensiile de fișiere asociate cu DjVu sunt .DJVU sau .DJV. DjVu poate obține rapoarte de compresie cu aproximativ 5 – 10 mai bune decât metodele existente, cum ar fi [JPEG](/ro/image/jpeg/) și [GIF](/ro/image/gif/) pentru documente color și de 3 – 8 ori mai bune decât [TIFF]( /image/tiff/) în documente alb-negru. Documentele scanate la 300 DPI cu full color de până la 25 MB pot fi comprimate până la 30 până la 100 KB. În mod similar, documentele alb-negru pot fi comprimate până la 5 până la 30 KB. Pagina HTML medie poate fi de până la 50 KB, prin urmare, aceste documente pot fi încărcate pe net fără nicio problemă.

## Scurt istoric ##

Tehnologia DjVu a fost dezvoltată în laboratoarele AT&T de către [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3% A9on_Bottou), Patrick Haffner și Paul G din 1996 până în 2001. Formatul de fișier DjVu a trecut prin diferite revizuiri, cea mai recentă fiind din 2005.


|Versiune|Data lansării|Note
---|---|---|
|1–19|1996–1999|Acestea sunt versiunile de dezvoltare.
|20|aprilie 1999|Pagină unică a fost schimbată în formatul cu mai multe pagini.
|23|iulie 2002|buncă CID
|24|februarie 2003|LTAnno bucată
|21|septembrie 1999|Format de stocare indirect înlocuit. Stratul de căutare text a fost adăugat.
|22|aprilie 2001|Orientarea paginii, culoare JB2
|25|mai 2003|bucnă NAVM. A fost adăugat suport pentru marcajele DjVu.
|26|aprilie 2005|Adnotări de text/linie

## Format de fișier DjVu ##

Documentele DjVu sunt fișiere IFF85. Structura oferă o ierarhie de containere care dețin informații într-un fișier DjVu. Aceste recipiente mai sunt numite și „bucăți”. Tipul fragmentului și ID-ul fragmentului descriu modul în care este utilizată fragmentul. Există un antet de 4 octeți urmat de structura IFF. Primii patru octeți ai unui fișier DjVu sunt 0x41 0x54 0x26 0x54. Această secțiune discută diferitele tipuri de documente DjVu și bucățile corespunzătoare din care constau.


|Chunk ID|Utilizare
---|---|
|FORM|Părțimea compusă având primii patru octeți de date ai fragmentului FORM care sunt identificatori secundar.
|FORM:DJVM|Un document DjVu cu mai multe pagini. Bucățiune compozită care conține fragmentul DIRM.
|FORM:DJVU|Document DjVu cu o singură pagină. Bucățiune compusă care conține bucățile care alcătuiesc o pagină într-un document djvu.
|FORM:DJVI|Un fișier DjVu „partajat” care este inclus prin fragmentul INCL. Adnotări comune și dicționar de forme.
|FORM:THUM|Bucățiune compozită care conține bucățile TH44 care sunt miniaturile încorporate.
|DIRM|Informații despre numele paginii pentru documente cu mai multe pagini.
|NAVM|Informații marcaj
|ANTa, ANTz|Adnotări care includ atât setările inițiale de vizualizare, cât și hyperlinkuri suprapuse, casete de text etc.
|TXTa, TXTz|Unicode Text și informații despre aspect.
|Djbz|Tabel cu forme partajate.
|Sjbz|BZZ a comprimat datele bitonale JB2 utilizate pentru a stoca masca.
|FG44|Date IW44 utilizate pentru stocarea primului plan
|BG44|Datele IW44 utilizate pentru stocarea fundalului
|TH44|Datele IW44 utilizate pentru stocarea imaginilor în miniatură încorporate
|WMRM|Date JB2 necesare pentru a elimina un filigran
|FGbz|Date JB2 color. Oferă o culoare pentru fiecare (blit sau formă?) în porțiunea Sjbz corespunzătoare.
|INFO|Informații despre pagina a DjVu
|INCL|ID-ul unui fragment FORM:DJVI inclus.
|BGjp|Fond codificat JPEG
|FGjp|prim-plan codificat JPEG
|Smmr|Mască codificată G4

### DJVU Compresie

O singură imagine este împărțită în mai multe imagini diferite, apoi fiecare imagine este comprimată separat. Pentru crearea unui fișier DjVu imaginea este mai întâi separată în trei imagini, un fundal, un prim plan și o imagine de mască. De obicei, imaginile de fundal și din prim-plan sunt imagini color cu rezoluție mai mică; dar imaginea cu masca este o imagine cu rezoluție mai mare și, de obicei, textul este stocat acolo. După separare, imaginile din prim-plan și de fundal sunt comprimate printr-un algoritm de compresie bazat pe wavelet IW44, în timp ce imaginea masca este comprimată folosind o altă metodă numită JB2.

Metoda de codificare JB2 elimină o mare parte din redundanța din imaginea text prin identificarea formelor identice pe pagină, cum ar fi aparițiile multiple ale unui caracter într-un anumit font. JB2 codifică mai întâi bitmap-ul fiecărei forme unice, profitând de redundanța dintre forme similare. Apoi codifică locațiile în care fiecare formă apare pe pagină. Atât JB2, cât și IW44 se bazează pe un nou tip de codificator aritmetic binar adaptiv numit ZP-coder care elimină orice redundanță rămasă cu câteva procente din limita Shannon. Codificatorul ZP este adaptiv și mai rapid decât alți codificatori aritmetici binari aproximativi.

## Referințe ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Format fișier DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

