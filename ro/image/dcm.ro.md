{
  "date" : "2019-10-11",
  "keywords" :[ "fișier dcm", "format fișier dcm", "ce este un fișier dcm", "fișier", "exemplu dcm", "extensie fișier dcm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier DCM - Fișier digital cu informații medicale",
  "description":"Aflați despre formatul de fișier DCM și despre API-urile care pot crea și deschide fișiere DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Ce este un fișier DCM?

Fișierele cu extensia .dcm reprezintă o imagine digitală care stochează informații medicale ale pacienților, cum ar fi RMN-uri, scanări CT și imagini cu ultrasunete. Fișierele DCM utilizează formatul de fișier imagine [DICOM](/ro/image/dicom/) (Imagini digitale și comunicații în medicină) și pot include informații despre pacient pentru referință. A fost dezvoltat de [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) și a fost menit să standardizeze formatul fișierului de imagistică pentru distribuirea și vizualizarea imaginilor medicale.

## Format de fișier DCM

Fișierele DCM stochează informații în format de imagine DICOM. Aceste fișiere stochează setul de date, care este informații din lumea reală, care reprezintă o instanță SOP legată de un DICOM IOD. Metainformațiile fișierului DICOM sunt stocate în fișier, urmate de fluxul de octeți al setului de date real.

### Informații meta fișier DICOM ##

Fiecare fișier DICOM include un antet de informații de identificare pentru setul de date încapsulat, care constă din:
* Un preambul de fișier de 128 de octeți
* Prefix DICOM de 4 octeți
* Elemente meta fisiere

Acest antet este obligatoriu pentru fiecare fișier DICOM.

### Elemente meta fișiere ###
|Nume atribut|Etichetă|Tip| Descrierea atributului
---|---|---|---|
|Preambulul fișierului|Fără câmpuri de etichetă sau lungime|1|Un câmp fix de 128 de octeți disponibil pentru utilizarea profilului aplicației sau a implementării specificate. Dacă nu sunt utilizați de un profil de aplicație sau de o implementare specifică, toți octeții vor fi setați la 00H. Cititorii sau actualizatorii setului de fișiere nu se vor baza pe conținutul acestui Preambul pentru a determina dacă acest fișier este sau nu un fișier DICOM.
|Prefix DICOM|Fără câmpuri de etichetă sau lungime|1|Patru octeți care conțin șirul de caractere „DICM”. Acest prefix este destinat să fie utilizat pentru a recunoaște că acest fișier este sau nu un fișier DICOM.
|Lungimea grupului de meta informații ale fișierului|(0002,0000)|1|Numărul de octeți care urmează acestui metaelement de fișier (sfârșitul câmpului Valoare) până la și inclusiv ultimul metaelement de fișier al metainformațiilor de fișier din grupul 2
|Versiune fișier meta informații|(0002,0001)|1|Acesta este un câmp de doi octeți în care fiecare bit identifică o versiune a acestui antet cu informații meta fișier. În versiunea 1, valoarea primului octet este 00H, iar a doua valoare a octetului este 01H. Implementările care citesc fișiere cu informații meta în care acest atribut are bitul 0 (lsb) al celui de-al doilea octet setat la 1 pot interpreta meta informațiile fișierului așa cum este specificat în acest versiunea PS3.10. Toți ceilalți biți nu trebuie verificați.
|Media Storage SOP Class UID|(0002,0002)|1|Identifică în mod unic clasa SOP asociată cu setul de date. UID-urile clasei SOP permise pentru stocarea media sunt specificate în PS3.4 - Profiluri de aplicație de stocare media.
|UID al instanței SOP de stocare media|(0002,0003)|1|Identifică în mod unic instanța SOP asociată cu setul de date plasat în fișier și urmând Metainformațiile fișierului.
|Transfer Syntax UID|(0002,0010)|1|Identifică unic sintaxa de transfer utilizată pentru a codifica următorul set de date. Această sintaxă de transfer nu se aplică metainformațiilor fișierului.
|UID Clasa de implementare|(0002,0012)|1|Identifică în mod unic implementarea care a scris acest fișier și conținutul acestuia. Oferă o identificare fără ambiguitate a tipului de implementare care a scris ultima dată fișierul în cazul unor probleme de schimb.
|Numele versiunii de implementare|(0002,0013)|3|Identifică o versiune pentru un UID al clasei de implementare (0002,0012) utilizând până la 16 caractere ale repertoriului.
|Titlul entității aplicației sursă|(0002,0016)|3|Titlul entității aplicației DICOM (AE) al AE care a scris conținutul acestui fișier (sau l-a actualizat ultima dată). Dacă este utilizat, permite urmărirea sursei erorilor în cazul unor probleme de schimb media.
|UID-ul creatorului de informații private|(0002,0100)|3|UID-ul creatorului informațiilor private (0002,0102).
|Informații private|(0002,0102)|1C|Conține informații private plasate în metainformații fișierului. Creatorul va fi identificat în (0002,0100). Obligatoriu dacă este prezent UID pentru creatorul de informații private (0002,0100).

### Încapsularea setului de date ###

Un fișier DICOM conține un singur set de date care reprezintă o singură instanță SOP legată de o singură clasă SOP. UID-ul de sintaxă de transfer al metainformațiilor fișierului DICOM va defini sintaxa de transfer utilizată pentru a codifica setul de date.

### Suport pentru informații de gestionare a fișierelor ###

Stratul de format media oferă următoarele informații de gestionare a fișierelor, dacă este necesar pentru un anumit profil de aplicație DICOM.

* Identificarea proprietarului conținutului fișierului

* Statistici de acces la fișiere (de exemplu, data și ora creării)

* Controlul accesului la fișiere de aplicație

* Controlul accesului la medii fizice (de exemplu, protejare la scriere)

## Referințe ##
* [Standard DICOM](https://www.dicomstandard.org/current/)
* [Format de fișier DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

