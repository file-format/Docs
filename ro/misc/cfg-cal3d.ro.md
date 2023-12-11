{
"data": "2023-09-27",
  "keywords": [
"cfg",
"fișier cfg",
"cfg cal3d model configuration file",
"Ce este un fișier cfg",
"cum se deschide fișierul cfg",
"fişier",
"extensie fișier cfg",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier CFG - Fișier de configurare model Cal3D",
  "description":"Aflați despre formatul fișierului de configurare a modelului CFG Cal3D și despre API-urile care pot crea și deschide fișiere CFG.",
  "linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
      "parent": "misc"
}
},
"lastmod": "2023-09-27"
}

## Ce este un fișier CFG?

Un fișier de configurare a modelului Cal3D este un fișier bazat pe text folosit de biblioteca Cal3D, care este un set de instrumente open-source pentru animația personajelor. Acest fișier servește ca model pentru asamblarea unui model tridimensional (3D). Include referiri la diferite componente ale modelului, cum ar fi structura scheletului, materialele, animațiile și multe altele. În esență, acționează ca un document central care ajută la organizarea și definirea modului în care toate părțile modelului 3D se potrivesc împreună în cadrul Cal3D.

Cal3D este o bibliotecă de animație scheletică folosită adesea în grafica computerizată și dezvoltarea jocurilor. Pentru a lucra cu modele Cal3D, de obicei trebuie să creați un fișier de configurare care să descrie structura modelului, materialele, animațiile și alte atribute. Mai jos este un exemplu despre cum ar putea arăta un fișier de configurare a modelului Cal3D.

```
<MODEL>
  <HEADER MAGIC="C3D" VERSION="1050" />

  <!-- Skeleton -->
  <SKELETON>
    <BONE ID="0" NAME="Root">
      <TRANSLATION>0.0 0.0 0.0</TRANSLATION>
      <ROTATION>0.0 0.0 0.0</ROTATION>
      <SCALE>1.0 1.0 1.0</SCALE>
    </BONE>
    <!-- Add more bone definitions here -->
  </SKELETON>

  <!-- Mesh -->
  <MESH>
    <SUBMESH>
      <MATERIAL>MATERIAL_NAME</MATERIAL>
      <VERTEX>
        <!-- Vertex data for the first vertex -->
        <POSITION>0.0 0.0 0.0</POSITION>
        <NORMAL>0.0 0.0 1.0</NORMAL>
        <TEXCOORD>0.0 0.0</TEXCOORD>
        <!-- Add more vertices here -->
      </VERTEX>
      <FACE>
        <!-- Face data for the first face -->
        <VERTEXID>0 1 2</VERTEXID>
        <!-- Add more faces here -->
      </FACE>
      <!-- Add more submeshes here -->
    </SUBMESH>
  </MESH>

  <!-- Animation -->
  <ANIMATION>
    <SKELETON>
      <!-- Define animations and keyframes here -->
    </SKELETON>
  </ANIMATION>

</MODEL>
```

## Cal3D

Cal3D este o bibliotecă de animație de caractere open-source folosită în grafica 3D pe computer și dezvoltarea jocurilor. Oferă instrumente și funcționalități pentru crearea și animarea personajelor sau modelelor 3D. Cal3D este adesea folosit pentru a aduce animații de personaje realiste în aplicații și jocuri interactive.

Caracteristicile și componentele cheie ale Cal3D includ:

1. **Mesh:** Componenta plasă definește geometria 3D a unui caracter sau obiect, inclusiv vârfuri, normale și coordonatele texturii. Formează reprezentarea vizuală a modelului.

2. **Schelet:** Cal3D permite crearea unei ierarhii de schelet pentru modelele de caractere. Acest schelet definește structura osoasă și fiecare os poate fi asociat cu o porțiune a plasei. Scheletele sunt cruciale pentru animarea personajelor prin manipularea oaselor.

3. **Materiale:** Materialele definesc modul în care ar trebui să apară suprafața modelului atunci când este redată. Aceasta include informații despre texturi, shadere și alte proprietăți de randare.

4. **Animări:** Cal3D acceptă diverse tehnici de animație care pot fi aplicate scheletului. Aceste animații definesc modul în care oasele se mișcă în timp pentru a crea animații realiste ale personajelor, cum ar fi mersul pe jos, alergarea sau efectuarea altor acțiuni.

5. **Fișiere de configurare:** Pentru a utiliza Cal3D în mod eficient, modelele sunt adesea însoțite de fișiere de configurare în format text simplu. Aceste fișiere descriu structura modelului, inclusiv ierarhia oaselor, datele rețelei, materialele și informațiile de animație. Fișierele de configurare servesc drept referințe pentru Cal3D pentru a încărca și a interacționa corect cu modelul.

## Formate de fișiere utilizate de Cal3D

Cal3D utilizează mai multe formate de fișiere în scopuri diferite, cum ar fi stocarea datelor de model, animații și informații de configurare. Iată câteva dintre formatele de fișiere comune utilizate de Cal3D:

1. **Fișiere de model binar Cal3D (.cmf):** Aceste fișiere stochează reprezentarea binară a modelelor 3D, inclusiv geometria rețelei, ierarhia osoasă și materialele. Fișierele CMF sunt folosite pentru a încărca și a reda eficient modelele Cal3D în aplicații.

1. **Fișiere model XML Cal3D (.cmx):** fișiere bazate pe XML care stochează reprezentarea textuală a modelelor Cal3D. Acestea conțin informații despre structura modelului, animații, materiale și multe altele. Fișierele [CMX](/ro/image/cmx/) sunt adesea folosite pentru editare și depanare mai ușor de citit de om.

1. **Fișiere de animație Cal3D (.caf):** Aceste fișiere stochează date de animație, inclusiv cadre cheie și transformări osoase. Fișierele CAF sunt esențiale pentru definirea modului în care personajele sau obiectele ar trebui să se miște și să se anime într-un model Cal3D.

1. **Cal3D Morph Target Files (.crf):** Folosit pentru a defini ținte morph, care permit expresii faciale și alte deformații non-scheletice ale rețelei.

1. **Fișiere de materiale Cal3D (.cfm):** Aceste fișiere stochează informații despre materiale pentru modelele Cal3D. Acestea specifică modul în care suprafața modelului ar trebui să fie umbrită, inclusiv referințele de textură, shadere și proprietățile de randare.

1. **Cal3D Skeleton Files (.csf):** Fișierele Skeleton stochează informații despre ierarhia osoasă și structura unui model Cal3D. Ele definesc modul în care oasele sunt conectate și parentale în schelet.

1. **Fișiere de configurare Cal3D (.cfg):** Aceste fișiere text simplu servesc ca fișiere de configurare pentru modelele Cal3D. Acestea conțin referințe la diferite componente ale modelului, inclusiv ierarhia osoasă, date de plasă, materiale și animații. Fișierele de configurare ajută Cal3D să încarce și să utilizeze corect modelul.

1. **Formate de imagine:** Deși nu sunt specifice pentru Cal3D, formate de fișiere imagine cum ar fi [JPEG](/ro/image/jpeg/), [PNG](/ro/image/png/), [BMP](/ro/image/bmp/ ), sau [TGA](/ro/image/tga/) sunt utilizate în mod obișnuit pentru texturi aplicate modelelor Cal3D.

## Cum se deschide fișierul CFG?

Programele care deschid fișiere CFG includ

- Cal3dViewer
- Microsoft Notepad
- Apple TextEdit
- Orice editor de text

## Alte fișiere CFG

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.cfg**.

**Setari**
- [CFG - Celestia Configuration File](/ro/settings/cfg-celestia/)
- [CFG - Fișier de conexiune la server Citrix](/ro/settings/cfg-citrix/)
- [CFG - Fișier de configurare MAME](/ro/settings/cfg-mame/)
- [CFG - Fișier de configurare LightWave](/ro/settings/cfg-lightwave/)

**Joc**
- [CFG - Wesnoth Markup Language File](/ro/game/cfg-wesnoth/)
- [CFG - Fișier de configurare MUGEN](/ro/game/cfg-mugen/)
- [CFG - Fișier de configurare a motorului sursă](/ro/game/cfg-sourceengine/)

**Sistem și diverse**
- [CFG - Fișier CFG](/ro/system/cfg/)
- [CFG - Fișier de configurare a modelului Cal3D](/ro/misc/cfg-cal3d/)

## Referințe
* [CAL3D](https://github.com/mp3butcher/Cal3D)
