{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Format fișier", "Deschide", "Citește", "Creează", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier HPGL și despre API-urile care pot crea și deschide fișiere HPGL.",
  "title" :"Format de fișiere HPGL - Învățați de la experții în format de fișiere!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Ce este un fișier HPGL?

Un fișier HPGFL (Hewlett-Packard Graphics Language) conține un set de instrucțiuni pentru controlul plotterului dezvoltat de HP. Ploterele HP folosesc acest fișier pentru a desena și imprima conținut vectorial și raster pe hârtie.

### Comanda HPGL

O comandă HPGL constă din următoarele.
* O secțiune de comandă a alfabetului de două caractere
* O secțiune de parametri
* Secțiunea Terminator

Fiecare parametru din fișier trebuie să fie împărțit cu un separator în cazul mai multor parametri.

### Exemplu de comandă HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Sistem de coordonate

Sistemele de coordonate constă din indicatori de măsurare bidimensionali pentru a localiza orice locație specifică. HPGL folosește atât coordonatele Plotterului, cât și sistemul de coordonate utilizator în acest scop.

#### Sistemul de coordonate plotter

Acest sistem de coordonate este utilizat pentru a trasa desene bazate pe mișcarea plotterului. O unitate tipică XY a mișcării minime a plotterului este 0,025 mm. Gama posibilă de desene se modifică în funcție de tipurile de plotter.

#### Sistem de coordonate utilizator

Sistemul de coordonate specificat de utilizator poate fi configurat folosind scara și originea. Acestea sunt convertite în coordonate plotter folosind comanda IP și comanda SC. Coordonatele sistemului plotter sunt utilizate în mod implicit dacă această conversie nu este efectuată.

## Format de fișier HPGL
Fișierele HPGL sunt în format ASCII (fișier text) și încep cu câteva comenzi de configurare. Aceasta setează anumiți parametri pentru plotter pentru trasare. Un fișier HPGL tipic arată după cum urmează.

|Comandă|Sens
---|---|
|IN;|inițializați, începeți o lucrare de plotare|
|IP;|setează punctele de scalare (P1 și P2) la pozițiile lor implicite|
|SP1;|selectați stiloul 1|
|PU0,0;|ridicați stiloul în sus și treceți la punctul de pornire pentru următoarea acțiune|
|PD100,0,100,100,0,100,0,0;|pun Pen Down și treceți la următoarele locații (desenați o casetă în jurul paginii)|
|PU50,50;|Pen Sus și treceți la coordonatele X,Y 50,50|
|CI25;|desenați un cerc cu raza 25|
|SS;|selectați setul de caractere standard|
|DT*,1;|setați delimitarea textului la asterisc și nu le tipăriți (1, adică „adevărat”)|
|PU20,80;|ridicați stiloul și treceți la 20,80|
|LBHello World*;|desenați o etichetă|

## Referințe
* [HPGL de la Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Ghid de referință HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

