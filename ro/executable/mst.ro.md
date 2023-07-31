{
  "date" : "2021-06-30",
  "keywords" :[ "fișier mst", "format fișier mst", "ce este un fișier mst", "fișier", "exemplu mst", "extensie fișier mst", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier MST și despre API-urile care pot crea și deschide fișiere MST.",
  "title" :"MST - Fișier pachet de instalare Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Ce este un fișier MST?
Fișierele cu extensia .mst sunt folosite pentru a transforma conținutul unui pachet MSI. Ele sunt utilizate în mod obișnuit de administratorii de sistem pentru a aplica setările personalizate unui fișier MSI existent. Fișierele MST sunt utilizate împreună cu pachetul original MSI în sistemele lor de distribuție a software-ului, cum ar fi politicile de grup. Fișierele MST sunt utilizate în general în dezvoltarea și testarea software-ului pentru configurarea versiunilor lor în curs de dezvoltare ale software-ului.

## Format de fișier MST
Un fișier MST sau Transform este utilizat pentru a colecta opțiunile de instalare pentru programele care utilizează Microsoft Windows Installer într-un fișier. Aceste fișiere sunt utilizate în mod obișnuit pe linia de comandă a programului de instalare (MSIEXEC.EXE) sau utilizate într-o politică de grup de instalare a software-ului; într-un domeniu Microsoft Active Directory. Fișierele MST pot fi utilizate și cu programe de instalare executabile încapsulate. Un caz general este că cineva dorește să transmită parametrii liniei de comandă programului de instalare înfășurat. Pentru a face acest lucru, aveți nevoie de un fișier MST care adaugă proprietatea WRAPPED_ARGUMENTS la tabelul de proprietăți. Aceste fișiere nu pot fi create sau editate folosind editori generali. Instrumente specifice sunt disponibile în acest scop.

### Cum se utilizează fișierele MST?
Fișierele MST pot fi generate utilizând diverse instrumente, iar Ocra este în general folosit pentru a genera fișiere MST. Apoi setările pot fi personalizate în funcție de nevoi și le pot salva într-o anumită locație. După aceea, fișierele MST pot fi utilizate împreună cu fișierele MSI. Dacă doriți să testați aceste fișiere; utilizați următoarea sintaxă pe linia de comandă

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
Proprietatea ### TRANSFORMS

De asemenea, puteți utiliza proprietatea **TRANSFORMS** a programului de instalare Windows, care este de fapt o listă a transformărilor pe care le aplică programul de instalare la instalarea pachetului. Programul de instalare execută transformările în aceeași ordine în care sunt listate în proprietatea TRANSFORM. Transformările pot fi specificate după numele fișierului cu extensia .mst sau calea completă. Pentru a specifica mai multe transformări, separați fiecare nume de fișier sau un punct și virgulă, ca exemplul următor.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referințe

* [Fișiere de transformare MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [proprietatea TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


