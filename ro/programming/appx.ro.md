{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Ce este un fișier APPX?",
  "description":"Aflați despre formatul de fișier APPX și despre API-urile care pot crea și deschide fișiere APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Ce este un fișier APPX?

Un fișier APPX este un format de fișier de pachet distribuibil care este utilizat pentru distribuirea și instalarea unei aplicații. A fost introdus cu Windows 8 pentru a fi publicat pe Microsoft Windows Store. Conține toate fișierele necesare pentru a instala o aplicație Windows. Acestea includ metadate, fișiere și informații despre acreditări. Un format de fișier de ambalare mai modern este MSIX, care este în prezent mai frecvent utilizat în comparație cu APPX.

## Format de fișier APPX - Mai multe informații

Fișierele APPX sunt salvate ca fișiere comprimate în format de fișier [ZIP](/ro/compression/zip/). Acest lucru face ca întregul pachet să fie un fișier de arhivă cu dimensiune redusă a fișierului, care este ușor de încărcat în Microsoft Store.

## Cum să vizualizați fișierele într-un fișier APPX?

Pentru a vizualiza conținutul sau fișierele din interiorul unui fișier APPX, trebuie urmați următorii pași.

1. Deoarece fișierele APPX sunt stocate ca fișiere ZIP comprimate, redenumiți fișierul în extensia .zip
1. Utilizați orice instrument de decompresie, cum ar fi 7-Zip, WinZip sau WinRAR pentru a extrage fișierele conținute în fișierul APPX

## Cum se creează un fișier APPX?

Există două metode care pot fi folosite pentru a crea fișiere APPX.

1. Folosind MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) este folosit pentru a crea ambele pachete de aplicații (.msix sau .appx) și fișiere de pachete de aplicații .msixbundle sau .appxbundle). În plus, poate extrage fișiere dintr-un pachet de aplicații. MakeApp.exe este disponibil cu Windows 10 SDK și poate fi utilizat din promptul de comandă.
1. Folosind Microsoft Visual Studio - Dezvoltatorii de obicei [creează fișiere APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) folosind Microsoft Visual Studio. Odată ce dezvoltarea aplicației este completă și aplicația este gata pentru a fi publicată, fișierul pachet APPX poate fi creat prin publicarea acestuia din Visual Studio.

## Referințe

* [Creați un pachet sau un pachet MSIX cu MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Creați fișiere APPX utilizând Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

