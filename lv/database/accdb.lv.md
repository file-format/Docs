{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par ACCDB faila formātu un API, kas var izveidot un atvērt ACCDB failus.",
  "title": "ACCDB faila formāts — Microsoft Access 2007 datu bāzes fails",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-lvb"
}
},
  "lastmod": "2020-11-12"
}

## Kas ir ACCDB fails?

Fails ar paplašinājumu .accdb ir Microsoft Access 2007 datu bāzes fails, kurā lietotāju dati tiek glabāti tabulās. Tas atbalsta uzglabāšanu
pielāgotas veidlapas, SQL vaicājumi un citi dati. ACCDB faili aizstāja [MDB](/database/mdb/) failus pēc tam, kad Microsoft pārgāja uz XML balstītu failu struktūru. ACCDB failus joprojām var pārveidot par MDB ar veco saderību. Tomēr tagad ACCDB ir plaši izmantotais Access datu bāzes faila formāts. Microsoft arī atbalstīja papildu līdzekļus ACCDB formātā, piemēram, iespēju saglabāt failu pielikumus, bināros datus un vairāku vērtību lauku atbalstu.

## ACCDB faila formāts

Tāpat kā MDB, ACCDB faila formātam nav pieejamas publiskas specifikācijas. Microsoft atbalsta programmatisku piekļuvi šiem failiem, izmantojot Open Database Connectivity (ODBC) standartu un Visual Basic for Applications (VBA).

### Ieskats

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. Šķiet, ka ACCDB failos šis indikators atspoguļo faila saderību, nevis tā izveidei izmantotās ACE programmas versiju.

## Atsauces

* [Piekļuves 2016. gada specifikācijas](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Kādu Access faila formātu man vajadzētu izmantot?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


