{
  "date" : "2019-10-11",
  "keywords" :[ "fișier osm", "ce este un fișier osm", "fișier", "exemplu osm", "extensie fișier osm", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM – Format de fișier OpenStreetMap",
  "description":"Aflați despre formatul de fișier OSM și despre API-urile care pot crea și deschide fișiere OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier OSM?

OpenStreetMap (OSM) este o colecție uriașă de depozite de informații geografice oferite voluntar în diferite tipuri de fișiere, folosind diferite scheme de codare pentru a converti aceste date în biți și octeți. OSM este un efort de colaborare pentru crearea unei hărți a lumii editabile gratuit. Rezultatul principal al acestui efort de colaborare sunt mai degrabă datele geografice decât harta în sine. Constrângerile privind utilizarea sau disponibilitatea informațiilor geografice în mare parte a lumii declanșează necesitatea creării unui OSM. Datele disponibile de la OSM sunt gata să înlocuiască Google Maps pentru aplicațiile clasice (Facebook, Craigslist etc.) și datele implicite pentru aplicațiile receptorului GPS.^^ ^^Deși calitatea datelor este diversă în întreaga lume, totuși datele OpenStreetMap pot fi comparate convenabil cu brevetele. surse de date.

## Scurt istoric ##

Inspirat de succesul Wikipedia, în 2004, Steve Coast, un antreprenor britanic, a creat acest proiect comunitar de cartografiere a lumii în Marea Britanie. Inițial s-a concentrat pe cartografierea Regatului Unit. Fundația OpenStreetMap a fost înființată pentru prima dată în aprilie 2006 pentru a sprijini evoluția, extinderea și circulația geospațială liberă pentru oricine. În decembrie 2006, Yahoo a ajutat OpenStreetMap cu fotografia sa aeriană pentru producția de hărți. Datele complete de drum pentru Țările de Jos și datele de drum principal pentru India și China au fost contribuite la OSM în aprilie 2007 de către Automotive Navigation Data (AND). În decembrie 2007, Universitatea Oxford a fost cea mai proeminentă organizație care a integrat datele OpenStreetMap în site-ul lor principal. De atunci, peste 2 milioane de utilizatori înregistrați contribuie cu date în acest proiect folosind dispozitive GPS, fotografii aeriene și sondaje manuale. Datele contribuite de această comunitate sunt puse la dispoziție sub Licența Open Database. O organizație non-profit, înregistrată în Anglia, OpenStreetMap Foundation a întreținut site-ul OSM.

## Format de fișier OSM ##

Există o mulțime de moduri și formate de fișiere de a stoca date geografice, dar formatul de fișier **OSM** este limitat la OpenStreetMap. OSM este un format standard conceput special pentru a fi transportat cu ușurință pe internet. Un format ordonat structurat, codificat în XML constituie fișierul .osm. În OpenStreetMap există patru elemente pivot pentru a stoca structura de date topologice:

{{< figure src="../OSM.png" alt="Format de fișier OSM" >}}


|Noduri|Căi|Relații|Etichete
---|---|---|---|
|<ul><li> Reprezintă poziția geografică stocată ca perechi de latitudine și longitudine.</li><li> Folosit pentru a reprezenta caracteristici ale hărții fără dimensiune, cum ar fi vârfurile muntoase.</li></ul> |<ul><li> Liste sortate de noduri, care semnifică o polilinie sau un poligon</li><li> Reprezentați caracteristici liniare, cum ar fi drumuri și râuri și zone, cum ar fi zonele de parcare, junglele și parcuri.</li></ul> |<ul><li> Listele sortate de noduri și căi reprezintă relația lor ca bariere și viraje pe drumuri, autostrăzile se întind pe diferite căi existente și zone cu găuri.</li></ul> |<ul><li> Stocați metadate despre obiectele hărții.* Întotdeauna atașat la orice nod, cale sau o relație</li></ul>


Etichetele sunt folosite pentru a caracteriza caracteristicile fizice ale solului (clădiri și drumuri etc.) în OpenStreetMap. Fiecare etichetă se referă la o caracteristică geografică a caracteristicii reprezentate de acel nod sau relație specifică. În acest sistem de etichetare gratuit, pentru a descrie o caracteristică, un număr nelimitat de atribute poate fi inclus într-o hartă. Combinațiile specifice de chei și valori aprobate de utilizatorii înregistrați acționează ca standarde informale pentru etichetele utilizate frecvent. Cu toate acestea, noi etichete pot fi create ori de câte ori aspecte noi necesită analizarea atributelor nemapate anterior ale caracteristicilor. Majoritatea funcțiilor folosesc doar un număr mic de etichete pentru descriere.

Trei tipuri de fișiere sunt folosite de OSM pentru a-și stoca datele principale.

OSM gestionează toate aceste fișiere cu informații despre detaliile lor de formatare. Dar aceleași obiecte interne sunt produse de aceste fișiere. Pentru fișierele de date, marcajul vizibil pe obiectele OSM este întotdeauna adevărat, ceea ce nu este cazul pentru fișierele de istoric și modificare.

În uz obișnuit, există o diversitate în formatele de fișiere OSM. Formatele de fișier definesc codificarea conținutului pe disc sau fir în biți și octeți. OSM este capabil să citească și să scrie maximum din aceste formate.

**XML**

Formatul original OSM este bazat pe XML. Datele returnate ale API-ului principal al bazei de date OSM sunt în format XML.

**PBF**

Codificarea protocolului tampon se află în format binar și unul dintre cele mai compacte formate.

**O5M/O5C**

Format binar bazat pe un format mai simplu, dar relativ mai puțin utilizat. OSM poate citi, dar nu poate scrie acest format.

**OPL**

Un format simplu propus pentru utilizare cu instrumentele standard de linie de comandă UNIX. Aproape de fișierele CSV, permite o entitate OSM pe o singură linie.

**DEBUG**

Un format bazat pe text destinat să creeze pentru depanare. OSM poate scrie acest format, dar nu poate citi.

**GAURĂ NEAGRĂ**

Un format fals care elimină toate datele. OSM poate scrie acest format, dar nu poate citi.

## Stocare de date OSM ##

Baza de date principală **PostgreSQL** a OSM păstrează copia principală a datelor OSM cu extensia PostGIS. Pentru fiecare primitivă de date, baza de date principală menține un tabel ale cărui rânduri stochează obiecte individuale. Toate editările actualizează această bază de date și toate celelalte formate sunt formate folosind această bază de date. Sunt create numeroase pool-uri de baze de date descărcabile pentru a transfera date dintr-un loc în altul. Două formate, unul folosind XML și altul folosind Protocol Buffer Binary Format (PBF) definesc aceste pool-uri. Datele complete sunt stocate într-un fișier numit planet.osm

## Comprimarea în fișierele OSM ##

Formatele bazate pe text (XML, OPL și Debug) folosesc opțional compresia gzip sau bzip2.

## Referințe ##

* [Manual de formate de fișiere OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Învățați OSM](https://learnosm.org/en/osm-data/getting-data/)

