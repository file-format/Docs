{
"data":"2023-10-11",
   "keywords":[
"mtl",
"fișier mtl",
"mtl obj material template library file",
"cum se deschide un fișier mtl",
"fişier",
"extensie fișier mtl",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format de fișier MTL - Fișier de bibliotecă de șabloane de materiale OBJ",
   "description":"Aflați despre formatul de fișier MTL OBJ Material Template Library și despre API-urile care pot crea și deschide fișiere MTL.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Ce este un fișier MTL?

Fișierul MTL, prescurtare de la **Material Template Library**, este un format de fișier însoțitor utilizat în grafica și modelare pe computer 3D. Este adesea asociat cu **formatul de fișier OBJ Wavefront**, care este un format comun pentru stocarea modelelor 3D și a materialelor și texturilor asociate acestora.

## Biblioteca de șabloane de materiale

Iată informații importante despre fișierele MTL:

1. **Definiții materiale**: fișierul ".mtl" conține definiții pentru materiale care sunt aplicate obiectelor 3D în fișierul OBJ corespunzător. Fiecare definiție de material specifică diferite proprietăți, cum ar fi hărțile de culoare, strălucire, transparență și texturi.
    





2. **Format bazat pe text**: fișierele ".mtl" sunt de obicei fișiere text simplu, ceea ce înseamnă că pot fi editate cu ușurință cu editorul de text. Fiecare definiție de material constă dintr-un set de declarații, iar aceste declarații definesc atributele materialului.
    





3. **Texture Mapping**: Una dintre funcțiile esențiale ale unui fișier ".mtl" este de a defini modul în care texturile (fișierele imagine) sunt mapate pe suprafețele modelului 3D. Specifică calea fișierului de textură și modul în care ar trebui să fie împachetat sau aplicat modelului.
    





4. **Exemple de instrucțiuni MTL**: Iată câteva exemple de declarații pe care le puteți găsi într-un fișier ".mtl":
    





- `newmtl MaterialName`: Aceasta definește materialul nou cu numele "MaterialName".
- `Ka rgb`: Culoarea ambientală a materialului, specificată în valori RGB.
- `Kd rgb`: Culoarea difuză a materialului, specificată în valori RGB.
- `Ks rgb`: Culoarea speculară a materialului, specificată în valori RGB.
- "Valoare Ns": strălucire sau exponent specular al materialului.
- `map_Kd texturefile.jpg`: Specifică harta texturii difuze pentru material.
5. **Materiale multiple**: Un fișier OBJ poate face referire la mai multe materiale și fiecare material este definit în fișierul ".mtl". Acest lucru permite modele 3D complexe cu materiale diferite aplicate pe diferite părți.
    





6. **Compatibilitate**: fișierele ".mtl" sunt acceptate pe scară largă de software-ul de modelare 3D și de motoarele de randare, făcând posibilă transferul modelelor 3D și materialelor acestora între diferite aplicații software.

## Cum se deschide un fișier MTL?

Fișierele MTL sunt fișiere bazate pe text, astfel încât acestea pot fi deschise cu orice editor de text, inclusiv

- Notepad (Windows)
- Notepad++ (Windows)
- Codul Visual Studio
- Text sublim
- Atom
- TextEdit (macOS)

Programele care deschid sau fac referire la fișiere MTL includ

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Ghepard3D

**SubTip:** Fișiere de imagine 3D

## Referințe
* [Fișier Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

