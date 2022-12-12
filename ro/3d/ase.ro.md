{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","fișier", "format", "tip fișier", "extensie","ce este un fișier ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier ASE și despre API-urile care pot deschide și crea fișiere ASE.",
  "title" :"ASE - Fișier de export de scenă Autodesk ASCII",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Ce este un fișier ASE?

Un fișier cu extensia .ase este un format de fișier Autodesk ASCII Scene Export, care este o reprezentare ASCII a unei scene, care conține informații 2D sau 3D în timp ce exportați date despre scenă folosind Autodesk. Autodesk oferă opțiuni pentru a include componente de scenă în timpul exportului de date de scenă. Puteți include definiția rețelei împreună cu informații despre vârf și față, descrierea materialului, datele de animație de transformare pentru obiecte, definirea completă a rețelei pentru fiecare n cadre, date de animație pentru camere și lumini și setări de îmbinare IK.

## Format de fișier ASE - Mai multe informații

Fișierele ASE sunt fișiere text stocate în format ASCII care pot fi deschise în orice editor de text. Un fișier ASE poate conține următoarele tipuri de informații furnizate de Autodesk.

### Opțiuni de ieșire

* `Mesh Definition` - Exportă definiția fiecărei rețele, inclusiv informații despre vârf și față pentru obiectele geometrice. În plus, activarea acestei opțiuni activează elementele din caseta de grup Opțiuni rețea, descrisă mai jos.
* `Materiale` - Include descrierea materialului. Dacă un material nu este alocat unui obiect, culoarea lui wireframe este exportată. Toate nivelurile unui arbore de materiale sunt incluse, astfel încât acest lucru poate produce mult text.
* `Transform Animation Keys` - Include datele de animație de transformare pentru obiecte. Dacă obiectul este o cameră țintă sau reflector, aceasta va include date de animație țintă.
* `Mesh animat` - Exportă o definiție completă a rețelei pentru fiecare n cadre. Frecvența este specificată de spinnerul de ieșire a controlerului, descris mai jos. Fiecare bloc conține aceleași informații specificate în caseta de grup Opțiuni de plasă, descrisă mai jos. Activarea acestei funcții poate avea ca rezultat un fișier uriaș, chiar și pentru scene mici.
* `Setări animate pentru cameră/lumină` - Exportă datele de animație pentru camere și lumini, cum ar fi culoarea, intensitatea, scăderea, părtinirea hărții și așa mai departe. Emite un bloc la fiecare n cadre, așa cum este specificat de spinnerul Controller Output.
* `Îmbinari cinematice inverse` - Exportă setările articulației IK în ramura Ierarhie.

### Tipuri de obiecte

Elementele de aici vă permit să specificați ce categorie de obiect doriți să fie incluse în rezultat. Puteți include obiecte geometrice, forme, camere, lumini și obiecte auxiliare.

* Geometric
* Forme
* Camere foto
* Lumini
* Ajutoare

### Opțiuni de plasă

* `Mesh Normals` - Exportă normalele feței și vârfurilor. Normala feței este listată mai întâi, urmată de normalele celor trei vârfuri care susțin fața. Activarea acestei funcții are ca rezultat un fișier mult mai mare.
* `Coordonate de cartografiere` - Exportă o listă de vârfuri și fețe de mapare, conform structurilor TVert și TVFace descrise în kitul de dezvoltare software 3ds Max. Dacă un obiect folosește maparea feței, este exportată o listă de hărți fețe care conține coordonatele UVW pentru fiecare față.
* `Colori vârfuri` - Exportă culorile vârfurilor.

### Ieșire controler

* `Utilizați chei` - Exportă valorile cheilor. Dacă controlerul nu folosește chei, atunci se folosește metoda Force Sample. În cazul controlerelor de transformare, opțiunea Utilizare chei funcționează numai dacă toate controlerele de transformare sunt fie Linear/TCB, fie Bezier. Dacă una dintre pistele de transformare folosește un alt tip de controler, atunci metoda Force Sample este utilizată pentru toate pistele de transformare.
* `Force Samples` - Eșantionează valorile controlerului pe baza frecvenței specificate în Frames per Sample Controller.

## Referințe

* [Autodesk - Exportare în ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

