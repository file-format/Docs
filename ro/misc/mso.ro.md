{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Fișier de referință pentru macrocomenzi Microsoft Office",
  "description":"Aflați despre fișierul MSO și API-urile care pot crea și deschide fișiere MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Ce este un fișier MSO?

Un fișier MSO este un format de fișier container de date care este creat atunci când un mesaj HTML este trimis folosind Microsoft Outlook. Acest lucru se întâmplă mai ales cu aplicațiile Microsoft Office 2000. În majoritatea cazurilor, mesajul de e-mail este atașat cu numele fișierului **Oledata.mso**. Destinatarul e-mailului, atunci când deschide un astfel de e-mail, poate vizualiza fișierul corect chiar dacă nu are același software instalat. Fișierele MSO se referă la [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Format de fișier Microsoft MSO

Fișierele MSO sunt salvate în Microsoft Compound Document File Format (MCDF), cunoscut și sub numele de Object Linking and Embedding (OLE) sau Component Object Model (COM) format de fișier binar de implementare a fișierelor compuse de stocare structurată.

### Structura formatului fișierului MSO

Structura internă a formatului de fișier a formatului de fișier MSO este bine definită în [Structuri](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) secțiunea documentației MCDF. Tabelul de alocare a fișierelor (FAT) gestionează alocarea sectorului și lanțurile de sector. Conține o matrice de numere de sector pe 32 de biți. Fiecare index din matrice reprezintă un număr de sector, în timp ce valoarea acestuia reprezintă următorul sector din lanț sau o valoare specială.

## Referințe

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

