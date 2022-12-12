{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "fișier", "format fișier", "Limba de descriere a paginii", "Scalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier SVG și despre API-urile care pot crea și deschide fișiere SVG.",
  "title" :"Ce este un fișier SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Ce este un fișier SVG? ##

Un fișier SVG este un fișier grafică vectorială scalară care utilizează formatul de text bazat pe XML pentru a descrie aspectul unei imagini. Cuvântul scalabil se referă la faptul că SVG-ul poate fi scalat la diferite dimensiuni fără a pierde calitatea. Descrierea pe bază de text a unor astfel de fișiere le face independente de rezoluție. Este unul dintre cele mai utilizate formate pentru a construi un site web și a imprima grafică pentru a obține scalabilitate. Formatul poate fi folosit doar pentru grafică bidimensională. Fișierele SVG pot fi vizualizate/deschise în aproape toate browserele moderne, inclusiv Chrome, Internet Explorer, Firefox și Safari.

## Scurt istoric ##

Specificațiile SVG sunt disponibile ca standard deschis de World Wide Web Consortium (W3C) din 1999. Înainte de aceasta, specificațiile de format de fișiere similare în șase formate diferite au fost trimise la W3C până în 1998. O actualizare a fost aplicată specificațiilor în 2011 și a fost versiunea 1.1. . În 2016, SVG 2 a fost publicat ca versiune mai nouă, incluzând funcții în plus față de cele din SVG 1.1.

## Specificații de format de fișier ##

Modelul SVG Document Object Model (DOM) pune bazele tuturor specificațiilor și interfețelor care corespund anumitor secțiuni ale specificațiilor. Vizionatorii SVG trebuie să implementeze interfețele SVG DOM așa cum sunt definite în specificațiile W3C. DOM-ul său expune mai multe interfețe pentru diferite tipuri de date și elemente.

### Forme SVG ###

SVG are câteva elemente de formă predefinite care pot fi folosite de dezvoltatori:

* Dreptunghi<rect>
* Cercul<circle>
* Elipsa<ellipse>
* Linie<line>
* Polilinie<polyline>
* Poligon<polygon>
* Cale<path>

Pe baza acestor forme și specificații, zonele funcționale ale SVG sunt următoarele.

**Traiuri** - Căile sunt folosite pentru a reprezenta contururi de forme simple și compuse. Codările sunt folosite pentru a defini natura operațiunii. De exemplu, M este folosit pentru Mutare la, L este folosit pentru Line To, Z este folosit pentru a închide o cale și așa mai departe.

**Forme de bază** - Pot fi desenate căi drepte și căi formate dintr-o serie de segmente de linie dreaptă conectate (polilinii), precum și poligoane închise, cercuri și elipse. Dreptunghiurile și dreptunghiurile rotunjite sunt, de asemenea, elemente standard.

**Text** - Reprezentarea textului este exprimată ca date de caracter XML în care pot fi aplicate textului multe efecte vizuale. Specificațiile permit gestionarea textului bidirecțional, textului vertical și a caracterelor de-a lungul unui traseu curbat.

**Pictură** - Formele pot fi umplute și/sau conturate cu o culoare, un gradient sau un model, permițând capacitatea de a le face opace sau de a avea orice grad de transparență. Caracteristicile de sfârșit de linie, cum ar fi vârfurile de săgeți sau simbolurile care apar la vârfurile unui poligon, sunt reprezentate de Markeri.

**Culoare** - specificațiile SVG permit aplicarea culorilor tuturor elementelor SVG vizibile, fie direct, fie prin umplere, contur sau alte proprietăți. Diferite codificări de culoare pot fi utilizate pentru specificarea, cum ar fi negru sau albastru, reprezentare hexagonală, zecimală sau ca procente din forma RGB.

**Degrade și modele** - Formele dintr-un fișier SVG pot fi umplute sau conturate cu culori solide, degrade sau modele repetate.

**Efecte de filtru** - Este de fapt o serie de operațiuni grafice care sunt aplicate unei grafice vectoriale surse date pentru a produce un rezultat modificat.

**Interactivitate** - Utilizatorii pot interacționa cu fișierele SVG schimbând focalizarea, clicurile mouse-ului, derulând sau mărind imaginea. Interactivitatea permite imaginilor SVG să interacționeze cu utilizatorii în multe moduri diferite, așa cum s-a menționat mai sus.

**Legare** - Este posibil ca imaginile SVG să aibă hyperlinkuri către alte documente. Acest lucru se realizează prin XML Linking Language sau XLink. Acest lucru permite crearea unor stări de vizualizare specifice care sunt utilizate pentru a mări / micșora o anumită zonă sau pentru a limita vizualizarea la un anumit element.

**Scriptare** - Similar cu HTML, toate aspectele unui document SVG sunt accesibile pentru manipulare folosind scripturi. Obiectele SVG DOM oferă îndrumări pentru realizarea acestui lucru folosind elementul și atributul SVG. Scripturile sunt incluse în elemente de etichetă `script` și pot rula ca răspuns la evenimentele indicator, tastatură sau document, după cum este necesar.

**Animation** - Elementele DOM<animate> ,<animateMotion> și<animateColor> vă permite să includeți animație pentru conținutul SVG. Desigur, acest lucru nu este realizabil fără utilizarea scripturilor și cronometrelor încorporate. Aceste animații pot fi continue și pot fi puse în buclă, precum și repetate, răspunzând în același timp la evenimentele utilizatorului.

**Fonturi** - Textul din SVG poate face referire la fișiere de fonturi externe, cum ar fi fonturile de sistem. În absența unor astfel de fonturi, textul în format SVG nu va fi redat la ieșire. Acest lucru poate fi depășit prin încorporarea glifelor necesare într-un astfel de fișier ca un font care este apoi redat folosind<text> element.

## Exemple ##
Următoarele rânduri arată cum este reprezentat un cerc folosind scriptul SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Următoarele rânduri de cod arată cum se utilizează<text> bloc pentru redarea textului în SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referințe ##

* [Specificații W3C SVG](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

