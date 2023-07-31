{
  "date" : "2020-08-20",
  "keywords" :[ "fișier cff2", "format fișier cff2", "ce este un fișier cff2", "fișier", "exemplu cff2", "extensie fișier cff2", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Format de fișier compact cu font versiunea 2",
  "description":"Aflați despre formatul fișierului CFF2 și API-urile pentru a crea și deschide fișiere CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Ce este un fișier CFF2?

Formatul de fișier CFF2 este versiunea 2.0 a formatului de fișier CFF și permite stocarea eficientă a contururilor glifelor și a metadatelor similare cu formatul de fișier CFF. CFF2 diferă de CFF prin faptul că este destinat să fie utilizat în contextul unui font OpenType ca tabel „sfnt” cu eticheta CFF2. Nu poate fi folosit ca program independent și depinde de datele din alte tabele OpenType.

## Format de fișier CFF2

[Specificațiile formatului fișierului CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) conține detalii despre aspectul intern al datelor, tipurile de date, tabele și alte informații interne despre formatul fișierului. Acesta poate fi referit pentru referința dezvoltatorului. Unele dintre detaliile despre acestea sunt următoarele.

### Aspect de date

Datele binare ale formatului de fișier CFF2 sunt organizate logic ca un număr de structuri de date separate. Aspectul în cadrul datelor binare este așa cum se arată în tabelul următor.

|Intrare |Comentarii|
---|---|
|Header |Locație fixă|
|Top DICT| Locație fixă|
|INDEX Global Subr| Locație fixă|
|Varianta |Magazin|
|FDSelect |Prezentă numai dacă există mai multe fonturi DICT în Font DICT INDEX.|
|Font DICT INDEX ||
|Matrice de font DICT| Inclus în font DICT INDEX.|
|DICT privat| Unul pe font DICT.|

Doar primele trei structuri se bazează pe locații fixe. Restul sunt atinși prin compensare, iar ordonarea acestora poate fi modificată.

### Tipuri de date

Formatul de fișier CFF2 utilizează următoarele tipuri de date.

|Nume |Interval |Descriere|
---|---|---|
|uint8 |0 până la 255 |număr nesemnat pe 8 biți|
|uint16 |0 la 65535| Număr nesemnat pe 16 biți|
|uint32 |0 la 4294967295| Număr nesemnat pe 32 de biți|
|Decalaj |variază| decalaje de 1, 2, 3 sau 4 octeți (specificate de câmpul OffSize dintr-un tabel Index)|
|OffSize |1 până la 4| Numărul nesemnat de 1 octet specifică dimensiunea unui câmp sau câmpuri Offset|

Stochează toate datele numerice multi-octeți și câmpurile de compensare în ordinea octeților big-endian. Formatul CFF2 nu are octeți de completare, deoarece nu respectă nicio restricție de aliniere.

### Date DICT

Fișierele CFF2 conțin datele din dicționarul fonturilor ca perechi cheie-valoare într-un format compact tokenizat. Cheile de dicționar sunt codificate ca operatori de 1 sau 2 octeți, iar valorile de dicționar sunt codificate ca operanzi numerici de dimensiune variabilă. Există trei structuri care utilizează formatul de date DICT: `Top DICT`, `Font DICT` și `Private DICT`. Un număr de tipuri de operanzi întregi de dimensiuni diferite sunt definite și sunt codificate așa cum se arată în tabelul următor (primul octet al operandului este b0, al doilea este b1 și așa mai departe).

|Dimensiune |interval b0 |Interval de valori |Calcul valorii|
---|---|---|---|
|1 |32 până la 246| -107 la +107 |b0 - 139|
|2 |247 la 250| +108 până la +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 la 254| -1131 la -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 la +32767| b1 << 8 | b2|
|5 |29| -(2^31) până la +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Antet

Datele binare încep cu un antet având formatul prezentat în tabelul de mai jos.

|Type |Nume |Descriere|
---|---|---|
|uint8| majorVersion| Formatați versiunea majoră. Setați la 2.|
|uint8| minorVersion| Formatați versiunea minoră. Setat la zero.|
|uint8| headerSize| Dimensiunea antetului (octeți).|
|uint16| topDictLength| Lungimea structurii Top DICT în octeți.|

## Referințe

* [Format de fișier CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

