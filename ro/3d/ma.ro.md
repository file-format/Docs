{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "fișier ma", "format fișier ma", "format fișier", "3d", "descărcare fișier ma", "fișier .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier MA și despre API-urile care pot deschide și crea fișiere MA.",
  "title" :"Format fișier MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Ce este un fișier MA?

Un fișier cu extensia .ma este un fișier proiect 3D creat cu aplicația Autodesk Maya. Conține o listă mare de comenzi textuale pentru a specifica informații despre fișier. Un fișier **.ma** poate fi deschis și editat în orice editor de text pentru a remedia orice problemă cu comenzile în cazul în care un fișier este corupt. Aceste fișiere conțin informații pentru definirea informațiilor despre scena 3D, cum ar fi geometria, iluminarea, animația și randarea.

## Format de fișier MA

Fișierele MA sunt salvate pe disc în format text ASCII, spre deosebire de fișierele MB care sunt salvate în format binar pe disc. O referință detaliată pentru formatul de fișier MA este disponibilă în [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) și poate fi referită pentru referința dezvoltatorului.

### Antet fișier MA

Antetul fișierului MA începe cu o secțiune de comentarii care oferă informații despre crearea fișierului și data modificării. Cititorii de fișiere Maya ignoră acest bloc, deoarece este folosit doar în scop informativ. Un antet trebuie să înceapă cu primele șase caractere ca „//Maya”.

Antetul fișierului ASCII arată după cum urmează.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Referințe la fișiere

Secțiunea cu referințe la fișiere a unui fișier .ma conține informații despre toate celelalte fișiere Maya la care se face referire în acest fișier. Fiecare fișier referit poate fi citit folosind o singură comandă de fișier care este conținută în același fișier. Sintaxa comenzii fișier atunci când este utilizată pentru referință este:

```
file -r -rpr prefixString fileName;
```
sau

```
file -r -ns nameSpace fileName
```
Iată un exemplu de șir.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Acest exemplu arată că obiectul soare conținut în fișierul `solar` ar fi accesibil în acest fișier folosind numele "solar_sun".

### Cerințe

Secțiunea de cerințe a unui fișier .ma constă dintr-o serie de comenzi obligatorii și îi transmite informații despre mai, cum ar fi informații despre versiune și plugin, care sunt necesare pentru a citi fișierele. Un exemplu de secțiune de cerințe este după cum urmează.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Următoarea secțiune specifică cerințele. Acesta constă dintr-o serie de comenzi necesită. Această secțiune a fișierului îi spune Mayei ce software este necesar pentru a încărca corect fișierul. Mai exact, ce versiune de Maya și ce plug-in-uri.

## Descărcarea fișierului MA
Este puțin greu să găsiți și să descărcați fișierul MA al unui model 3d. Prin urmare, puteți descărca un exemplu de fișier MA de aici:

- [Sample.ma](../sample.ma)


## Referințe

* [Organizarea fișierelor Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

