{
  "date" : "2020-08-20",
  "keywords" :[ "fișier ttf", "format fișier ttf", "ce este un fișier ttf", "fișier", "exemplu ttf", "extensie fișier ttf", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF – Format de fișier cu font TrueType",
  "description":"Fonturile TrueType (TTF) se bazează pe specificațiile tehnologiei fonturilor digitale concepute inițial de Apple, Inc. Atât Apple, cât și Microsoft au folosit TTF pe sistemele de operare Mac și Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Ce este un fișier TTF?

Un fișier cu extensia .ttf reprezintă fișiere cu fonturi bazate pe tehnologia de fonturi cu specificațiile TrueType. A fost proiectat și lansat inițial de Apple Computer, Inc pentru Mac OS și a fost ulterior adoptat de Microsoft pentru Windows OS. Fonturile TrueType oferă afișare de cea mai înaltă calitate pe ecranele computerelor și imprimantelor fără nicio dependență de rezoluție. Toate aplicațiile moderne care folosesc fonturi pot funcționa cu fișiere TTF. Fișierele cu fonturi TTF sunt disponibile gratuit pe internet și pot fi, de asemenea, convertite în alte formate de fișiere cu fonturi, cum ar fi OTF și WOFF.

## Scurt istoric

Proiectat de Apply Computer, Inc în anii 1980 pentru MacOS, formatul de font TTF a avut ca scop rezolvarea unor limitări tehnice ale formatului Adobe Type 1. Apple a inclus suport pentru fonturile TrueType în Mac în 1991. Obiectivul de design din spatele fonturilor TTF a fost eficiența în stocare și procesare și extensibilitate. Pe baza acestei extensibilități, fonturile existente pot fi convertite în format TrueType.

Microsoft a folosit pentru prima dată fonturile TrueType în Windows 3.1 în aprilie 1992, după ce Apple a fost de acord să licențieze TrueType către Microsoft. A îmbunătățit mecanismul de rasterizare și a îmbunătățit eficiența și performanța acestuia.

## Specificații de format de fișier True Type

Un fișier cu font TrueType este un fișier binar care constă dintr-o secvență de tabele concatenate. Fiecare tabel este o secvență de cuvinte și are un nume cunoscut sub numele de „Tag”. Fiecare etichetă este de tip de date uint32 și constă din patru caractere. Primul tabel din fișier este directorul de fonturi care oferă acces la alte tabele din fișierul de font. Datele fonturilor sunt conținute în alte tabele urmate după tabelul directorului de fonturi. Deoarece fiecare tabel este accesibil prin eticheta sa, tabelele pot apărea în orice ordine în fișier.

Tabelele necesare și numele etichetelor lor sunt prezentate în tabelul următor.

|**Tag**|**Tabel**|
---|---|
|'cmap'| mapare caracter la glif|
|'glyf'| date glif|
|'cap'| antet font|
|'hhea'| antet orizontal|
|'hmtx'| metrici orizontale|
|'loca'| index la locație|
|'maxp'| profil maxim|
|'nume'| denumire|
|'post'| PostScript|

### Tipuri de date
Fonturile TrueType folosesc numere întregi standard și tipuri de date suplimentare, așa cum sunt enumerate în tabelul următor.

|**Tipul de date** | **Descriere** |
---|---|
|scurtFrac| fracție semnată pe 16 biți|
|Fixat| Număr cu virgulă fixă semnat pe 16,16 biți|
|FWord| Număr întreg cu semn de 16 biți care descrie o cantitate în FUnits, cea mai mică distanță măsurabilă în spațiul em.|
|uFWord| Număr întreg fără semn pe 16 biți care descrie o cantitate în FUnits, cea mai mică distanță măsurabilă în spațiul em.|
|F2Dot14| Număr fix semnat pe 16 biți, cu cei 14 biți mici reprezentând fracția.|
|longDateTime| Formatul intern lung al unei date, în secunde, de la 12:00 miezul nopții, 1 ianuarie 1904. Este reprezentat ca un întreg semnat de 64 de biți.|

### Director de fonturi

Primul tabel din fontul TrueType este directorul de fonturi care oferă acces la informațiile necesare pentru accesarea datelor din alte tabele. Mai constă în:

* `Offset subtable` - păstrează evidența tabelelor în font și oferă informații despre offset pentru a accesa fiecare tabel din director
* `Director tabel` - Conține intrări pentru fiecare tabel în font

#### Subtabel de compensare
Subtabelul offset este prezentat mai jos.

|**Tip**|**Nume**|**Descriere**|
---|---|---|
|uint32| tip scaler| O etichetă pentru a indica scalatorul OFA care va fi utilizat pentru a rasteriza acest font; consultați nota de mai jos despre tipul scalerului pentru mai multe informații.|
|uint16| numTables| numărul de mese|
|uint16| interval de căutare| (putere maximă de 2 <= numTables)*16|
|uint16| entrySelector| log2(putere maximă de 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Director tabel
Directorul tabelului vine imediat după subtabelul offset. Structura sa este cea prezentată în tabelul următor.

|**Tip**|**Nume**|**Descriere**|
---|---|---|
|uint32| etichetă| identificator de 4 octeți|
|uint32| checkSum| sumă de control pentru acest tabel|
|uint32| offset| offset de la începutul sfnt|
|uint32| lungime| lungimea acestui tabel în octeți (lungimea reală nu lungimea completată)|

Fiecare tabel dintr-un fișier cu fonturi trebuie să aibă propria sa intrare în directorul tabelului. Intrările dintr-un tabel trebuie sortate în ordine crescătoare după etichetă.


## Referințe
* [Manual de referință pentru font TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Prezentare generală TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

