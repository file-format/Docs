{
  "date" : "2019-10-11",
  "keywords" :[ "fișier de administrare", "format de fișier de gestionare", "ce este un fișier de administrare", "fișier", "exemplu de administrare", "extensie de fișier de gestionare", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier MNG - Format de fișier grafic de rețea cu imagini multiple",
  "description":"Aflați despre formatul fișierului MNG și despre API-urile care pot crea și deschide fișiere MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier MNG?

Un fișier cu extensia .mng este un format de fișier Multiple-image Network Graphics care este similar cu formatul de imagine [PNG](/ro/image/png/), dar acceptă imagini animate. A fost dezvoltat pentru a evita supraîncărcarea formatului PNG cu caracteristici suplimentare de animații. MNG este, de asemenea, similar cu fișierele [GIF](/ro/image/gif/), dar utilizează mai multă compresie și acceptă funcția alfa completă. Tipul media neoficial MIME pentru fișierele MNG este video/x-mng. Fișierele MNG pot fi deschise în aplicații precum ImageMagik și IrfanView.

## Format de fișier MNG

Formatul de fișier MNG este similar cu cel al PNG și utilizează aceeași structură de fragmente definită în specificațiile PNG. Un decodor MNG trebuie să poată decoda fluxurile de date PNG fără a specifica niciun semnal special pentru instrucțiunile de decodare. MNG grupează mai multe imagini într-un „cadru”, unele imagini fiind folosite ca sprite pentru deplasarea dintr-o locație în alta. Mecanismul permite reutilizarea datelor de imagine fără a le retransmite. [Specificațiile MNG](http://www.libpng.org/pub/mng/spec/) pot fi consultate pentru referința dezvoltatorului.

### Semnătura MNG

Fluxul de date MNG începe cu o semnătură de 8 octeți care conține:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Aceasta este similară cu cea a semnăturii PNG, dar conține MNG în loc de PNG.

### Cadrul MNG

Un cadru MNG constă dintr-o imagine bidimensională a imaginilor mai mici. Fiecare imagine mică poate fi accesată folosind combinația de index de rând și coloană. Formatul este capabil să stocheze date „voxel” tridimensionale care sunt aranjate într-o serie de planuri bidimensionale. Fiecare plan este reprezentat de un flux de date PNG sau Delta-PNG. Fiecare flux de date Delta-PNG definește o imagine ca diferențe față de imaginea PNG părinte. Aceasta oferă o modalitate mult mai compactă de a reprezenta imaginile ulterioare decât utilizarea unui flux de date PNG complet pentru fiecare.

## Referințe ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Format MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

