{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Limba încorporată Maya", "fișier", "extensie", "format fișier", "Maya 3D", "Ghid de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL – Format de fișier în limbă încorporată Maya",
  "description":"Aflați despre formatul fișierului MEL și despre API-urile care pot crea și deschide fișiere MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Ce este un fișier MEL?

Un fișier cu extensia .mel (Maya Embedded Language) este un limbaj de scripting care este folosit de Autodesk Maya pentru a crea interfețe grafice. Vă permite să automatizați crearea de elemente grafice folosind scripturi executabile în plus față de interfața grafică Maya. MEL vă permite să creați interfețe grafice fără a învăța programarea. Acest lucru se realizează prin crearea de macrocomenzi și acțiuni personalizate care accelerează sarcinile repetitive. Aceste proceduri și scripturi vă permit să creați modele personalizate, animații, dinamică și randare a sarcinilor. Autodesk Maya 2020 poate fi folosit pentru a deschide și vizualiza conținutul unui fișier EML.

## Format de fișier MEL - Mai multe informații

Un [manual de referință](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) al programatorului este disponibil pentru dezvoltatori în secțiunea de documentație a lui Maya. MEL se bazează pe comenzi de scripting shell, similare cu UINX, pentru a realiza lucruri. Comenzile bazate pe scripturi o fac irelevantă pentru programarea convențională și orientată pe obiecte (OOP), rezultând în nicio utilizare a structurilor de date, apelarea funcțiilor sau utilizarea OOP ca în alte limbi.

Câteva puncte cheie despre MEL sunt următoarele.

`Comentarii` - Fiecare instrucțiune din MEL trebuie să se încheie cu punct și virgulă (;), chiar și la sfârșitul unui bloc.

`Returning Values` - Anunțarea unei expresii care returnează o valoare nu imprimă automat valoarea în MEL. În schimb, provoacă o eroare.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Comenzi pentru Creare, Editare și Ștergere` - Aceeași comandă este folosită pentru a crea lucruri, a edita lucruri sau a interoga informații despre lucruri existente. Cu toate acestea, un flag controlează ceea ce face comanda (creați, editați sau interogați).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - Sintaxa funcției returnează automat o valoare. Pentru a obține o valoare returnată folosind sintaxa comenzii, trebuie să includeți comanda între ghilimele.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referințe

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

