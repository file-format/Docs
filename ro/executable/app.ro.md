{
"data": "2023-02-02",
  "keywords": [
"fișierul aplicației",
"Ce este un fișier de aplicație",
"fişier",
"cum se deschide fișierul aplicației",
"extensie fișier aplicație",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Aflați despre formatul fișierului APP și despre API-urile care pot crea și deschide fișiere APP.",
"title": "Format fișier APP - pachet de aplicații macOS",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Ce este un fișier APP?

Un fișier .app pe macOS este un tip special de director care conține toate fișierele necesare pentru a rula o anumită aplicație, inclusiv codul executabil, resursele și metadatele. Extensia .app semnalează sistemului de operare că acest director ar trebui tratat ca o singură unitate, mai degrabă decât o colecție de fișiere separate și că poate fi lansat direct din Finder sau Dock.

Finder este aplicația implicită de gestionare a fișierelor pe macOS. Vă permite să răsfoiți și să organizați fișierele și directoarele de pe computer. Dock-ul este o caracteristică a macOS care oferă acces rapid la aplicațiile și documentele utilizate frecvent. Atât Finder, cât și Dock vă permit să lansați aplicații făcând clic pe fișierele lor .app, care vor deschide pachetul de aplicații corespunzător. Când lansați o aplicație, se rulează codul executabil din pachetul .app, făcând aplicația disponibilă pentru utilizare. Fișierul .app este reprezentarea aplicației pe sistemul de fișiere și oferă utilizatorului o modalitate de a accesa și de a lansa aplicația.

Când faceți clic dreapta pe un fișier .app în Finder pe un sistem macOS și selectați "Afișați conținutul pachetului", veți putea vedea structura internă a pachetului de aplicații. Acest lucru este util dacă doriți să accesați resurse sau fișiere utilizate de aplicație sau dacă doriți să inspectați conținutul aplicației în scopuri de depanare. Conținutul pachetului unui fișier .app include de obicei directoare pentru resurse precum imagini și sunete, precum și codul executabil pentru aplicație. Explorând conținutul unui fișier .app, puteți obține o perspectivă mai profundă asupra modului în care este creată aplicația și a ceea ce face.

## Cum se deschide fișierul APP?

Pentru a deschide un fișier .app pe macOS, faceți dublu clic pe fișier în Finder. Aceasta va lansa aplicația conținută în pachetul .app. Dacă aplicația este instalată pe sistemul dvs. și a fost asociată cu tipul de fișier .app, dublu clic pe fișier ar trebui să pornească automat aplicația. Dacă aplicația nu este asociată cu tipul de fișier .app, poate fi necesar să faceți clic dreapta pe fișier și să selectați "Deschide cu" pentru a alege o aplicație adecvată cu care să o deschideți.

Puteți deschide un fișier .app pe Terminal în macOS utilizând comanda "deschidere". Pentru a face acest lucru, navigați la directorul în care se află fișierul .app folosind comanda "cd", apoi executați următoarea comandă:

```
open <AppName>.app 
```

Unde<AppName> este numele aplicației pe care doriți să o lansați. Aceasta va porni aplicația ca și cum ați fi dublu clic pe ea în Finder. Comanda "deschidere" este un utilitar de uz general care poate fi folosit pentru a deschide multe tipuri diferite de fișiere, inclusiv aplicații, documente și directoare. Când utilizați comanda "deschidere" pe un fișier .app, aceasta lansează aplicația conținută în pachet.

## Referințe
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
