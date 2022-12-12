{
  "date" : "2021-06-30",
  "keywords" :[ "fișier msi", "format fișier MSI", "ce este un fișier msi", "fișier", "exemplu msi", "extensie fișier msi", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier MSI și despre API-urile care pot crea și deschide fișiere MSI.",
  "title" :"MSI – fișierul pachetului de instalare Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Ce este un fișier MSI?
Un fișier MSI folosit pentru a instala și lansa programe Windows; un pachet complet pentru Microsoft Windows care conține informații de instalare pentru un program software tipic, inclusiv fișiere esențiale de instalat și informații despre locația de instalare. Fișierele MSI pot conține, de asemenea, pachetul pentru actualizări de software. Fișierele MSI sunt similare cu [EXE](/ro/executable/exe/), dar EXE uneori poate să nu includă informațiile de instalare, iar programul software poate rula direct la executarea fișierului EXE.

## Format de fișier MSI
Windows Installer este de fapt o API (Application Programming Interface) și o componentă software a Microsoft Windows folosită pentru instalarea, eliminarea și întreținerea unui program software. Informațiile de instalare și fișierele opționale sunt împachetate ca pachete de instalare și baze de date relativ relaționale structurate ca stocări structurate COM; bine cunoscut sub numele de **fișiere MSI**, având extensia de fișier .msi. Pachetele cu extensia de fișier **.mst** conțin **Scripturi de transformare** din Windows Installer, fișierele cu extensia **.msm** conțin **Module de îmbinare** și extensia de fișier **.pcp** este folosit pentru **Proprietăți de creare a corecțiilor**. Windows Installer devine mai avansat după ce a avut modificări semnificative față de versiunile sale anterioare, Setup API. Un cadru GUI și generarea automată a secvenței de dezinstalare sunt noile caracteristici ale Windows Installer. A fost considerat acum ca o alternativă la cadrele de instalare executabile autonome.

### Structura logică a pachetelor MSI
Un pachet desemnează instalarea unuia sau mai multor produse complete și este, în general, identificat printr-un **GUID**. Un produs este alcătuit din una sau mai multe componente și grupat în diferite caracteristici. Windows Installer nu gestionează dependențele dintre diferite produse simultan. Structura logică a pachetelor constă din următoarele elemente:

- **Produse**: un singur program, instalat, de lucru sau un set de programe multiple combinate împreună este un produs. Un produs este identificat printr-un GUID unic.
- **Caracteristici**: poate conține orice număr de componente și alte subfuncții. Pachetele mai mici pot consta dintr-o singură caracteristică.
- **Componente**: Componenta este tratată de Windows Installer ca o unitate; poate conține fișiere de program, foldere, chei de registry, componente COM și comenzi rapide.
- **Key Paths**: o cale cheie este un anumit fișier, sursă de date ODBC sau cheie de registry pe care autorul pachetului o specifică ca fiind critică pentru o anumită componentă.

## Referințe

* [Windows Installer - de la Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


