{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Format fișier", "Deschidere", "Citire", "Creare", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DWF și despre API-urile care pot crea și deschide fișiere DWF.",
  "title" :"Format fișier DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DWF?

Design Web Format (DWF) reprezintă desen 2D/3D în format comprimat pentru vizualizarea, revizuirea sau imprimarea fișierelor de design. Conține grafică și text ca parte a datelor de proiectare și reduce dimensiunea fișierului datorită formatului său comprimat. Dimensiunea redusă a fișierului face ca distribuția și comunicarea datelor de design bogate să fie eficiente. DWF nu solicită destinatarului să știe despre utilizarea software-ului CAD care a creat desenul original. Conținutul formatului de fișier DWF poate fi simplu și include doar o singură coală sau suficient de complex pentru a avea fonturi, culoare și imagini.

## Scurt istoric ##

Autodesk a introdus formatul de fișier DWF în 1995, ca parte a plug-in-ului Netscape Navigation, WHIP. Formatul a evoluat de la formatul doar 2D pentru a include conținut 3D odată cu trecerea timpului. Multe dintre aplicațiile de la terțe părți folosesc și acest format.

## Format de fișier DWF ##

DWF este un format deschis, securizat, conceput special pentru partajarea datelor bogate de proiectare inginerească. Este independent de software-ul, hardware-ul și sistemul de operare original utilizat pentru a crea acele date de proiectare. Acest lucru permite membrilor echipei care nu folosesc aplicații CAD să participe la procesele digitale prin vizualizarea clădirilor, a GIS sau a proiectelor de produse. O arhivă de fișiere DWF constă din mai multe fișiere XML și binare care sunt împachetate împreună într-o arhivă comprimată creată cu compresie [ZIP](/ro/compression/zip/). Puteți redenumi o extensie de fișier DWF în ZIP și puteți vizualiza conținutul fișierului. Pachetul DWF poate conține multe tipuri de date de proiectare, cum ar fi grafică 2D, grafică 3D, metadatele pachetelor și secțiunilor și alte fișiere de resurse.

**Fișiere de metadate DWF** – fișiere XML care conțin informații referitoare la metadate și structură (autor, titlu, timpul creării, dependențele secțiunilor, ordonarea secțiunilor, descrierile fișierelor de resurse, roluri, tipurile mime etc.) și referitoare la secțiune (pagina informații, metadate de proiectare etc.). Metadatele structurale sunt folosite pentru a crea obiecte logice (colecții de fișiere pentru a reprezenta o parte sau o pagină etc.).

**Fișiere de resurse** – fișiere media sau alte fișiere de conținut care sunt referite din metadatele pachetului/secțiunii și sunt de obicei prezentări ale datelor de proiectare în diferite formate (ZGL, W2D, [JPG](/ro/image/jpeg/), [PNG](/ro/image/png/), AVI, XML, [TXT](/ro/word-processing/txt/), [DOC](/ro/word-processing/doc/), etc.)

### Detalii format fișier ###

Fișierele DWF sunt organizate în trei secțiuni principale, așa cum se arată mai jos.

* Antet de identificare a fișierului
* Bloc de date fișier
* Trailer de terminare a fișierului

#### Antet identificator fișier ####

Antetul de identificare a fișierului permite identificarea fișierelor DWF în funcție de aplicații. De asemenea, identifică ce versiune a specificațiilor DWF a fost utilizată pentru codificarea fișierului. Este un antet de 12 octeți care este aranjat după cum urmează:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Caracter|(|D|W|F|(spațiu)|V|0|0|.|3|0|)

Iată un rezumat al acestui tabel:

* Primii șase octeți ai antetului reprezintă întotdeauna caractere ASCII „(DWF V”
* Următorii 5 octeți conțin informații despre numărul versiunii, de exemplu „00.30” cu valoarea versiunii majore și minore a formatului

Aplicațiile care creează un fișier DWF ar trebui să specifice cel mai mic număr de versiune posibil pe care o aplicație de citire trebuie să o suporte pentru a utiliza corect datele.

#### Bloc de date fișier ####

Blocul de date al fișierului începe la al 13-lea octet al unui fișier DWF și este o serie de perechi opcode și operanzi, ca în tabelul următor.

|Câmp 1|Câmp 2|Câmp 3|Câmp 4|Câmp 5|Câmp 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

Un fișier DWF poate conține perechi opcode-operand ca ASCII lizibil, precum și cod binar sau o combinație a ambelor. Toate operațiunile DWF au o formă de opcode/operand ASCII care poate fi citită, iar majoritatea operațiunilor au, de asemenea, o formă codificată de operand/operand binar. Opcodes sunt pe un singur octet, permițând peste 200 de operațiuni. ASCII extins și binarul extins sunt cazuri excepționale. Valorile Opcodes pot varia de la 0 la 255, cu unele excepții. Cu excepția celor două tipuri speciale de coduri operaționale extinse ASCII și binar extins, un cititor de fișiere trebuie să știe cum să calculeze lungimea operandului.

##### Opcode interzise #####

Reprezentările ASCII pentru următoarele nu pot fi folosite ca opcode:

Următoarele reprezentări ASCII nu pot fi folosite ca opcode:

* Spațiu (0x20)
* Filă (0x09)
* Cratimă (0x2D)
* cifre ASCII 0-9 (0x30 - 0x39)
* Retur transport (0x0D)
* Alimentare linie (0x0A)
* Ghilimele simple (0x27)
* Ghilimele duble (0x22)
* Perioada (0x2E)
* Paranteze (0x28 și 0x29)
* Paranteze (0x7B și 0x7D)
* Paranteze pătrate (0x5B și 0x5D)
* Bară oblică înapoi (0x5C)

#### Trailer de terminare a fișierului ####

Trailer-ul de terminare a fișierului pentru DWF este pur și simplu un opcode special care indică sfârșitul fișierului. Unele aplicații pot stoca date non-DWF în urma codului operațional de terminare. Trailer-ul este prezentat mai jos:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Caracter|(|E|n|d|0|f|D|W|F|)

## Referințe ##

* [DWF - De Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Format de date WHIP](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

