{
  "date" : "2021-08-16",
  "keywords" :[ "fișier nrg", "format fișier nrg", "ce este un fișier nrg", "fișier", "exemplu nrg", "extensie fișier nrg", "extensie", "format", "subsol nrg", "fișier format nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier NRG și despre API-urile care pot crea și deschide fișiere NRG.",
  "title" :"NRG - Format fișier imagine disc",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Ce este un fișier NRG?

Un format de fișier imagine care este creat prin utilizarea unui disc optic este considerat un format de fișier NRG. Acest format este creat special de Nero pentru utilitatea Nero Burning Rom. Pentru stocarea imaginilor de disc, acest format este considerat a fi utilizat deoarece este adecvat pentru aceste fișiere specifice. Aceste fișiere pot fi sub forma unei copii exacte a unui CD sau DVD sau pot avea mai multe fișiere care pot fi montate ca disc. Alte formate de fișiere mai populare, cum ar fi formatele de fișiere [ISO](/ro/compression/iso/), sunt cele în care aceste fișiere pot fi convertite în unele utilitare de bază. În cea mai mare parte, fișierele NRG sunt folosite pentru a crea copii de siguranță sau copii ale unor date sau discuri importante.

## Format fișier NRG ##

Acest format de fișier a fost dezvoltat de Nero AG ca format de imagine de disc. Avea proprietatea specifică a utilitarului Nero Burning Rom, deoarece a fost dezvoltat pentru a stoca imagini de disc. Prima sa versiune a fost specificată pentru a stoca valori ca numere întregi pe 32 de biți. Cu toate acestea, a doua versiune a fost lansată și conținea suport pentru numere întregi pe 64 de biți.

## Specificație tehnică ##

La începutul fișierului, acest format nu își stochează datele ca antet. Ca un subsol, este atașat la sfârșitul fișierului. Sub formă de bucăți de IFF, informațiile imaginii sunt stocate. Offset-ul primei bucăți poate fi obținut prin citirea subsolului NRG la ultimii 8 octeți până la 12 octeți ai fișierului. În toate versiunile formatului de fișier NRG, există bucăți, DAOI, text CD, tipul media de informații despre sesiune, informații despre disc, Relo și sfârșitul lanțului atașat cu acesta. Ordinea octeților este big-endian și toate valorile întregi sunt nesemnate în momentul stocării.

### Bucăți principale ###

#### Tac ####

Această foaie cue este disponibilă cu ușurință în toate versiunile formatului de fișiere NRG. Porțiunea **CUEX** înseamnă blocurile de concatenare de dimensiune fixă și fiecare dintre acestea reprezintă punctul cue.

#### Informații DAO ####

Aceste informații sunt prezente și în toate versiunile formatului NRG. Bucățile de **DAOI** stochează informațiile specifice relevante în 2 părți. Prima parte constă numai din datele specifice sesiunii. A doua parte a acestuia doar repetă informațiile gri legate de urmărire și este o singură dată pentru fiecare piesă.

#### CD-text ####

Acesta este disponibil în a doua versiune a NRG. Porțiunea de **CDTX** constă din concatenarea brută a pachetului de CD-text având 18 octeți pentru fiecare.

#### Informații extinse despre traseu ####

Acesta este disponibil în fiecare versiune a formatului de fișier al NRG. Aceste bucăți sunt utilizate pentru stocarea informațiilor de urmărire pentru pista de sesiuni simultan. Aceste date se repetă o singură dată în cazul fiecărei piese.

#### Informații despre sesiune ####

Acesta este, de asemenea, disponibil în fiecare versiune a formatului de fișier al NRG. Informațiile fragmentelor de sesiune trebuie utilizate pentru scanarea rapidă a imaginii sesiunii și apoi numărul de urmărire.

#### Sfârșitul lanțului ####

Bucățile de final înseamnă semnalele că acum nu mai există bucăți care trebuie citite și acest lucru este disponibil și în toate versiunile NRG.


## Referințe ##

* [NRG - de Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


