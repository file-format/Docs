{
  "date" : "2019-10-11",
  "keywords" :[ "fișier obj", "format fișier obj", "ce este un fișier obj", "fișier", "exemplu obj", "extensie fișier obj", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier OBJ",
  "description":"Aflați despre formatul de fișier OBJ și despre API-urile care pot deschide și crea fișiere OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier OBJ?

Fișierele **OBJ** sunt utilizate de aplicația Advanced Visualizer de la Wavefront pentru a defini și stoca obiectele geometrice. Transmiterea înapoi și înainte a datelor geometrice este posibilă prin fișierele OBJ. Atât geometria poligonală, cum ar fi punctele, liniile, vârfurile de textură, fețele și geometria cu formă liberă (curbe și suprafețe) sunt acceptate de formatul OBJ. Acest format nu acceptă animație sau informații legate de lumină și poziția scenelor.

Un fișier OBJ este de obicei un produs final al procesului de modelare 3D generat de un CAD (Computer Aided Design). Ordinea implicită de stocare a nodurilor este în sens invers acelor de ceasornic evitând declararea explicită a normalelor feței. Deși fișierele OBJ declară informații de scară într-o linie de comentarii, totuși nu au fost declarate unități pentru coordonatele OBJ.

## Istoria formatului 3D OBJ

Wavefront Technologies a creat formatul de fișier OBJ pentru aplicația sa Advanced Visualizer pentru a stoca obiecte geometrice și date 3D. Versiunea sa 2.11 este înlocuită de o versiune nou documentată 3. Formatul de fișier este deschis și a fost implementat de alți furnizori pentru aplicația lor de grafică 3D. Wavefront Technologies a păstrat acest format de fișier open source și neutru.

## Format de fișier OBJ

În obiectele 3D, codificarea geometriei suprafeței este o muncă provocatoare pe care formatul de fișier OBJ a realizat-o foarte bine. Acest format este destul de versatil, deoarece oferă o serie de opțiuni pentru a codifica geometria suprafeței. Următoarele sunt trei formate permise, având propriile beneficii și dezavantaje:

### Teselație cu fețe poligonale

Formatul de fișier OBJ facilitează utilizatorului să teseleze o suprafață de model 3D folosind forme geometrice simple sau complexe. Pentru codificarea geometriei suprafeței unui model, un fișier stochează vârfurile și normala fiecărui poligon. Deși teselația crește grosieritatea modelului, totuși este necesar să se descopere echilibrul corect între dimensiunea unui fișier și calitatea imprimării acestuia.

### Curbă cu formă liberă

Formatul de fișier OBJ permite curbelor de suprafață cu formă liberă definite de utilizator să specifice geometria suprafeței unui model. Deoarece curbele cu formă liberă sunt mai complexe decât fețele poligonale, deoarece, cu puțini parametri matematici, liniile curbe pot fi definite cel mai bine prin curbele cu formă liberă. Prin urmare, cu mai puține date în comparație cu teselațiile poligonale, curbele cu formă liberă au fost folosite pentru a genera o codificare de înaltă calitate a oricărui model 3D fără a extinde dimensiunea fișierului.

### Suprafețe cu formă liberă

Formatul de fișier OBJ specifică, de asemenea, placarea geometriei suprafeței cu patch-uri de suprafață cu formă liberă. Acest tip de petice de suprafață cu formă liberă (NURBS) este foarte potrivit pentru suprafețe fără dimensiuni radiale rigide, cum ar fi caroseria unui camion, aripile elicopterului sau carena unei bărci. Utilizarea suprafețelor cu formă liberă este foarte avantajoasă, deoarece acestea sunt mai precise pentru a menține dimensiunile fișierelor mai mici la o precizie mai mare. Aceste suprafețe sunt o parte esențială a industriei aerospațiale și auto, unde precizia scăzută este neiertătoare.

Următoarele cuvinte cheie sunt aranjate după tipul de date pentru a defini geometria suprafeței.


|Elemente|Instrucțiuni curbe/suprafețe în formă liberă|Atribute curbe/suprafețe în formă liberă
---|---|---|
|p|Punct|parm|Valorile parametrilor|grade|Grad
|l|Line|trim|Bucla de tăiere exterioară|bmat|Matrice de bază
|f|Față|gaura|Bucla interioară de tăiere|pas|Dimensiunea treptei
|curva|Curba|scrv|Curba speciala|cstype|Curba sau tip suprafata
|curv2|curba 2D|sp|Punctul special|**Conectivitate si grupare de suprafete**
|surf|Surface|end|End statement|con|connect
|**Atribute de afișare/redare**|g|Numele grupului
|teșire|Interpolare teșire|shadow_obj|Shadow turning|s|Grup de netezire
|lod|Nivel de detaliu|trace_obj|Ray tracing|mg|Grup de fuzionare
|d_interp|Interpolare dizolvată|ctech|Tehnica de aproximare a curbei|o|Numele obiectului
|c_interp|Interpolarea culorilor|stech|Tehnica de aproximare a suprafetei|
|usemtl|Numele materialului|mtllib|Biblioteca de materiale|
|**Vârfurile geometrice**|
|v|Vârfurile geometrice|vn|Normale de vârf|
|vt|Vârfurile de textură|vp|Vârfurile spațiului parametrilor|

### Culoare și textura

Fișierul OBJ permite stocarea informațiilor de culoare și textură într-un format de fișier asociat numit Material Template Library (MTL). Modelele geometrice multicolore sunt redate folosind aceste două fișiere împreună. Fișierele MTL sunt bazate pe ASCII și facilitează redarea pe computer prin descrierea proprietăților de reflectare a luminii ale unei suprafețe folosind modelul reflexiei Phong. Standardul a fost adoptat de un număr mare de furnizori de software care profită de acesta pentru schimbul de materiale. Formatul MTL este ușor depășit pentru că nu are suport în cele mai recente tehnologii, cum ar fi hărți speculare și paralaxe.

## Referințe

* [Fișier Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

