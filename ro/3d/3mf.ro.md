{
  "date" : "2019-12-09",
  "keywords" :[ "fișier 3mf", "format fișier 3mf", "ce este un fișier 3mf", "fișier", "exemplu 3mf", "extensie fișier 3mf", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Aflați despre formatul de fișier 3MF și despre API-urile care pot deschide și crea fișiere 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Ce este un fișier 3MF?

3MF, 3D Manufacturing Format, este folosit de aplicații pentru a reda modele de obiecte 3D la o varietate de alte aplicații, platforme, servicii și imprimante. A fost creat pentru a evita limitările și problemele din alte formate de fișiere 3D, cum ar fi [STL](/ro/cad/stl/), pentru a lucra cu cele mai recente versiuni de imprimante 3D. 3MF este un format de fișier relativ nou care a fost dezvoltat și publicat de consorțiul 3MF. Este suficient de bogat pentru a descrie pe deplin un model, reținând informațiile interne, culoarea și alte caracteristici care îl fac extensibil pentru a susține noile inovații în imprimarea 3D. Formatul este extensibil, capabil să fie adoptat pe scară largă și fără probleme care afectează alte formate de fișiere utilizate pe scară largă.

## Scurt istoric al formatului de fișier 3MF

Limitările existente în formatele de fișiere descriptive disponibile, cum ar fi STL și altele, determină mărcile de top să se reunească și să formuleze un format de fișier mai extensibil pentru imprimarea 3D. O considerație importantă a fost modul în care aplicațiile ar trebui să transmită datele modelului către imprimantele 3D. Prin urmare, consorțiul 3MF a luat ființă pentru a susține un nou format de fișier 3D numit 3MF, cu scopul de a-l face suficient de extensibil pentru a satisface nevoile imprimării 3D. Mai multe companii au făcut parte din acest consorțiu, inclusiv Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP și altele. Microsoft și-a donat formatul de fișier 3D în lucru ca punct de plecare pentru dezvoltarea în continuare colaborativă a specificației de către Consorțiul 3MF.

## Format de fișier 3MF - Mai multe informații

3MF este un format de date bazat pe XML – XML comprimat care poate fi citit de om – care include definiții pentru datele legate de fabricarea 3D, inclusiv extensibilitatea de la terți pentru date personalizate. Formatul de fișier 3MF a fost conceput ținând cont de limitările și problemele cu care se confruntă alte formate de fișiere 3D. Acest lucru a condus la formularea formatului de fișier 3MF care este:

* **Complet:** Conținând toate informațiile necesare despre model, material și proprietate într-o singură arhivă
* **Lizibil pentru oameni:** Folosind structuri comune, cum ar fi OPC, [ZIP](/ro/compression/zip/) și XML pentru a ușura dezvoltarea
* **Simplu:** O specificație scurtă și clară, care face dezvoltarea ușoară și validarea rapidă
* **Extensibil:** Utilizarea spațiilor de nume XML permite extensii atât publice, cât și private, menținând în același timp compatibilitatea
* **Fără ambiguitate:** Limbajul clar și testele de conformitate asigură că un fișier este întotdeauna consistent de la digital la fizic
* **Gratuit:** Accesul și implementarea specificației 3MF sunt și vor fi întotdeauna libere de drepturi de autor, brevete și licențe

Specificațiile pentru formatul de fișier 3MF sunt găzduite pe [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) pentru acces public și actualizări continue. Versiunea curentă publicată este 1.2.3 care descrie setul de convenții pentru utilizarea XML și a altor tehnologii disponibile pe scară largă pentru a descrie conținutul și aspectul unuia sau mai multor modele 3D. Dezvoltatorii, care doresc să construiască sisteme pentru procesarea formatelor de fișiere 3MF, se pot referi la aceste specificații în scopul implementării.

## Specificații de format de fișier 3MF

Formatul de fișier 3MF utilizează specificațiile Open Packaging sub formă de arhivă ZIP pentru modelul său fizic. Include un set bine definit de părți și relații care îndeplinesc un anumit scop în document. Acest lucru face ca formatul să urmeze caracteristica pachetului, inclusiv semnăturile digitale și miniaturile.

### Documentul 3MF - O prezentare generală

Un document tipic 3MF arată după cum urmează:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

Sarcina utilă include setul complet de piese necesare procesării componentei modelului 3D. Tot conținutul care urmează să fie utilizat pentru fabricarea unui obiect descris în sarcina utilă 3D TREBUIE să fie conținut în Documentul 3MF. Descrierea fiecărei părți de document, împreună cu starea acesteia, așa cum este necesar sau opțiunea, este prezentată în tabelul următor.


|**Nume**|**Descriere**|**Sursa relației**|**Obligatoriu/Opțional**
--- | --- | --- | ---
|Model 3D|Conține descrierea unuia sau mai multor obiecte 3D pentru fabricație.|Pachet|NECESAR
|Proprietăți de bază|Partea OPC care conține diverse proprietăți ale documentului.|Pachet|OPȚIONAL
|Originea semnăturii digitale|Partea OPC care este rădăcina semnăturilor digitale din pachet.|Pachet|OPȚIONAL
|Semnătură digitală|Părți OPC care conțin fiecare o semnătură digitală.|Originea semnăturii digitale|OPȚIONAL
|Certificat de semnătură digitală|Componente OPC care conțin un certificat de semnătură digitală.|Semnătură digitală|OPȚIONAL
|PrintTicket|Oferă setări pentru a fi utilizate la ieșirea obiectelor 3D în partea de model 3D.|Model 3D|OPȚIONAL
|Minatură|Conține o imagine mică JPEG sau PNG care reprezintă obiectele 3D din pachet sau pachetul ca întreg.|Pachet|OPȚIONAL
|Textură 3D|Conține o textură folosită pentru a aplica culoarea unui obiect 3D în partea Model 3D (disponibilă pentru extensii)|Model 3D|OPȚIONAL
|Piese personalizate|Părți OPC care sunt asociate cu metadate|Pachet|OPȚIONAL

[Părți și relații](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Modele 3D](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Resurse obiect](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Resurse materiale](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) și [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) secțiuni ale specificațiilor documentul oferă informații detaliate despre documentul 3MF.

## Referințe ##

* [Specificații de format de fișier 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - De Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

