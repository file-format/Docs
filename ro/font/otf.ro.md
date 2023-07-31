{
  "date" : "2020-08-20",
  "keywords" :[ "fișier otf", "format fișier otf", "ce este un fișier otf", "fișier", "exemplu otf", "extensie fișier otf", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Format de fișier cu font TrueType",
  "description":"Aflați despre formatul de fișier OTF și despre API-urile care pot crea și deschide fișiere OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Ce este un fișier OTF?

Un fișier cu extensia .otf se referă la formatul de font OpenType. Formatul de font OTF este mai scalabil și extinde caracteristicile existente ale formatelor [TTF](/ro/font/ttf/) pentru tipografia digitală. Dezvoltat de Microsoft și Adobe, OTF combină caracteristicile formatelor de font PostScript și TrueType. Acest lucru face ca formatul OTF să se potrivească sistemelor de scriere majoritare și de aceea este utilizat în mod uniform pe platformele de computer majore. Formatul de font OpenType este acceptat de Mac OS X și Windows 2000 și versiuni ulterioare.

## Scurt istoric

Cerința de fonturi OpenType a apărut ca o cerință pentru un format de font mai expresiv, care ar putea gestiona o tipografie fină. În plus, a avut ca scop satisfacerea cerințelor de comportament complex ale multor sisteme de scriere ale lumii. Microsoft a încercat să licențieze tehnologia avansată de tipografie a Apple, cunoscută sub numele de GX Typography, la începutul anilor 1990. Acest lucru nu a mers bine și, drept urmare, Microsoft a început să-și îmbunătățească tehnologia de fonturi TrueType în 1994. Modificările au inclus și introducerea unui format de font mai potrivit, care îndeplinește și caracteristicile formatelor de font Adobe Type 1 (PostScript).

Adobe, în 1996, sa alăturat Microsoft în eforturile sale de a înlocui atât TrueType de la Apple, cât și propriul său format de font Type 1. Acest lucru a dus la combinarea ambelor formate de fonturi de bază pentru a depăși limitările și pentru a adăuga noi extensii. Această nouă tehnologie a fost introdusă în același an cu numele **OpenType**.

## Specificații pentru formatul fișierului OTF

Specificațiile OTF sunt disponibile public de Microsoft și pot fi consultate din perspectiva dezvoltatorului. La fel ca TTF, folosește aceeași structură de container „sfnt” și este compatibil cu specificațiile TrueType. Datele din interiorul unui fișier de font OpenType sunt utilizate în diferite scopuri, cum ar fi calcularea aspectului textului, definirea glifelor ca contururi TrueType sau Compact Font Format (CFF), furnizarea de hărți de biți monocromatice sau color sau documente SVG ca descrieri alternative de glife și informații despre metadate.

### Tipuri de date OTF
Fișierele OTF folosesc următoarele tipuri de date, care sunt toate în Big Endian.

|Tipul de date| Descriere|
---|---|
|uint8| întreg fără semn pe 8 biți.|
|int8| întreg cu semn pe 8 biți.|
|uint16| întreg fără semn pe 16 biți.|
|int16| întreg cu semn pe 16 biți.|
|uint24| întreg fără semn pe 24 de biți.|
|uint32| întreg fără semn pe 32 de biți.|
|int32| întreg cu semn pe 32 de biți.|
|Fixat| Număr cu virgulă fixă semnat pe 32 de biți (16.16)|
|FWORD| int16 care descrie o cantitate în unități de design de font.|
|UFWORD| uint16 care descrie o cantitate în unități de design de font.|
|F2DOT14| Număr fix semnat pe 16 biți cu cei 14 biți mici de fracție (2.14).|
|LUNGATETIME| Data și ora reprezentate în număr de secunde de la 12:00 miezul nopții, 1 ianuarie 1904, UTC. Valoarea este reprezentată ca un întreg cu semn de 64 de biți.|
|Etichetă| Matrice de patru uint8s (lungime = 32 de biți) utilizată pentru a identifica un tabel, o axă de variație de proiectare, un script, un sistem de limbaj, o caracteristică sau o linie de bază|
|Offset16| Offset scurt la un tabel, la fel ca uint16, offset NULL = 0x0000|
|Offset32| Offset lung la un tabel, la fel ca uint32, offset NULL = 0x00000000|
|Versiune16Dot16| Valoare împachetată pe 32 de biți cu numere de versiuni majore și minore. (Consultați Numerele versiunilor de tabel.)|

### Director de tabele OTF

Un fișier OTF începe cu un director de tabel. Acest director este colecția de nivel superior a tabelelor din fișierul cu fonturi. În funcție de numărul de fonturi dintr-un fișier, directorul tabelului poate fi localizat în locații diferite din fișier. De exemplu, în cazul în care fișierul cu fonturi are un singur font, directorul tabelului începe la octetul 0 al fișierului. În cazul colecțiilor multiple de fonturi OpenType,
începutul directorului tabelului este indicat în TTCHeader.

|Type |Nume |Descriere|
---|---|---|
|uint32 |sfntVersion| 0x00010000 sau 0x4F54544F („OTTO”)|
|uint16| numTables |Numărul de tabele.|
|uint16| searchRange |Puterea maximă de 2 mai mică sau egală cu numTables, ori 16 ((2\**floor(log2(numTables))) * 16, unde „**” este un operator de exponențiere).|
|uint16 |entrySelector Log2 cu puterea maximă de 2 mai mică sau egală cu numTables (log2(searchRange/16), care este egal cu floor(log2(numTables))).|
|uint16 |rangeShift |numTables ori 16, minus searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Matrice de înregistrări de tabel — câte una pentru fiecare tabel de nivel superior din font|


### Înregistrare tabel

Pentru fiecare tabel de nivel superior din font, există o înregistrare de tabel care constă din următoarele câmpuri.

|Tip| Nume| Descriere|
---|---|---|
|Etichetă| tableTag| Identificator tabel.|
|uint32| suma de control| Sumă de control pentru acest tabel.|
|Offset32| offset| Decalaj față de începutul fișierului fontului.|
|uint32| lungime Lungimea acestui tabel.|

Fiecare tabel din fișierul de font OpenType este reprezentat de nume cunoscute ca etichete de tabel. Este obligatoriu ca toate înregistrările din matrice să fie sortate în ordine crescătoare după etichetă.

## Referințe
* [Specificații pentru font OpenType de la Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Prezentare generală TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

