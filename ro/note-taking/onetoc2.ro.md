{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Format de fișier Microsoft OneNote",
  "description":"Aflați despre formatul de fișier ONETOC2 și despre API-urile care pot crea și deschide fișiere ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este ONETOC2? ##

Cei care au lucrat cu aplicația [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) este posibil să fi observat prezența fișierelor .onetoc2 în folderul notebook-ului. Microsoft OneNote creează un fișier binar .onetoc2 ca Cuprins pentru a păstra un index despre ordonarea diferitelor secțiuni de luare de note într-un caiet. Un blocnotes este o colecție de fișiere secțiuni care sunt stocate în același director. Fișierul .onetoc2 utilizează o colecție de proprietăți pentru a specifica setări, cum ar fi ordinea secțiunilor din blocnotes și culoarea blocnotesului.

Când creați un blocnotes în OneNote 2016, acesta este salvat automat în noul format de fișier 2010-2016. Veți avea nevoie de acest format dacă doriți ca toate funcțiile din OneNote 2016, cum ar fi ecuațiile matematice și notele legate, să funcționeze corect.

## Format de fișier ONETOC2 ##

Formatul de fișier .onetoc2 este reprezentat ca format de fișier OneNote Revision Store și este o colecție de structuri care specifică un depozit de revizii organizat în spații obiect cu referințe încrucișate, care conține obiecte cu seturi de proprietăți și conțin un jurnal de tranzacții pentru a asigura integritatea fișierului în asincrone. scrie. Specificațiile complete pentru formatul de fișier .onetoc2 sunt disponibile [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) și pot fi consultate pentru dezvoltarea aplicațiilor .

### Structura fișierului ###

Un fișier de stocare a versiunilor TREBUIE să înceapă cu o structură **Header**. Restul fișierului este împărțit în blocuri de octeți, unde dimensiunea și structura fiecărui bloc sunt specificate de câmpul care face referire la el. Un bloc este accesibil dacă este referit de structura **Header** sau dacă este referit de un câmp dintr-un alt bloc accesibil. Datele din afara structurii **Header** și orice blocuri accesibile TREBUIE ignorate.

Toate structurile sunt aliniate pe granițele de 1 octet. Toate numerele întregi sunt semnate, dacă nu se specifică altfel. Toate câmpurile sunt [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), dacă nu se specifică altfel.

#### Antet ####

Antetul fișierului .ONE cuprinde bucăți care conțin diferite ID-uri și câmpuri unice pentru reprezentarea informațiilor despre fișier, după cum urmează:

`guidFileType (16 octeți):` Un GUID care specifică tipul fișierului de stocare a reviziilor. TREBUIE să fie una dintre valorile din tabelul următor.

|Format fișier|Valoare
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Un GUID care specifică identitatea acestui fișier de stocare a versiunilor. TREBUIE să fie unic la nivel global.

`guidLegacyFileVersion (16 octeți):` TREBUIE să fie „{00000000-0000-0000-0000-000000000000}” și TREBUIE ignorat.

`guidFileFormat (16 octeți):` Un GUID care specifică că fișierul este un fișier de stocare a reviziilor. TREBUIE să fie „{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 octeți):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de tipul fișierului.

|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.


|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.
:


|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un întreg fără semn. TREBUIE să fie una dintre valorile din următorul tabel, în funcție de formatul de fișier al acestui fișier.


|Format fișier|Valoare
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Referințe ##

* [[MS-ONESTORE] - Format de fișier OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

