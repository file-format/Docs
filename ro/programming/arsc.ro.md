{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","ce este un fișier arsc","cum se deschide fișierul arsc", "extensie", "fișier", "fișier arsc","format fișier arsc", "extensie fișier arsc" ,"Exemplu de fișier arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - fișierul tabelului resurselor pachetului Android",
  "description":"Aflați despre formatul de fișier ARSC și despre API-urile care pot crea și deschide fișierul ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Ce este un fișier ARSC?

Un fișier ARSC este un fișier tabel de resurse Android care conține lista de resurse a aplicației într-un format de tabel. Acesta conține informații precum numele resurselor, proprietățile și ID-urile. Fișierele ARSC fac parte din pachetele APK care sunt utilizate pentru a instala aceste aplicații Android. Toate resursele, cum ar fi imagini, machete, stiluri și șiruri, dintr-o aplicație Android sunt convertite în fișiere binare atunci când fișierul APK este generat. Fișierul ARSC este, de asemenea, generat la același, care conține lista tuturor resurselor compilate ale programului și ID-urile acestora.

## Format de fișier ARSC

Fișierele de extensie .arsc sunt fișiere binare generate după ce compilatorul, cum ar fi ANT (Eclipse) sau Gradle (AS), compilează codul aplicației Android pentru a produce fișierul [APK](/ro/compression/apk/). Puteți extrage fișierul APK folosind orice utilitar de arhivare, cum ar fi WinZip, pentru a vedea conținutul acestuia, care sunt fișierele de clasă Java compilate, adică classes.dex. În plus față de acestea, conține și acest fișier ARSC care conține metainformații despre:

* Nodurile XML
* Atributele
* ID-urile resurselor

Resursele dintr-un fișier APK sunt referite prin ID-urile resurselor, în timp ce atributele sunt rezolvate la o valoare în timpul execuției. Instrumentul Android aapt colectează toate resursele definite în fișiere în timpul construirii și le atribuie ID-uri de resurse. După ce identificatorii sunt alocați resurselor compilate, este generat un fișier R.java din codul sursă, precum și din fișierul resources.arsc.

## Referințe

* [Structura tabelului de resurse binare](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

