{
  "date" : "2020-03-16",
  "keywords" :[ "Fișier DXF", "Format fișier", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DXF și despre API-urile care pot crea și deschide fișiere DXF.",
  "title" :"Format fișier DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DXF?

DXF, Drawing Interchange Format sau Drawing Exchange Format, este o reprezentare de date etichetată a desenului AutoCAD. Fiecare element din fișier are un număr întreg de prefix numit cod de grup. Acest cod de grup reprezintă de fapt elementul care urmează și indică semnificația unui element de date pentru un anumit tip de obiect. DXF face posibilă reprezentarea aproape a tuturor informațiilor specificate de utilizator într-un desen.

Formatul de fișier DXF a fost dezvoltat de Autodesk ca format de fișier de date CAD pentru interoperabilitatea datelor între AutoCAD și alte aplicații. Astfel, datele pot fi importate din alte formate în DXF în AutoCAD conform specificațiilor de interoperabilitate a formatului de fișier DXF.

## Scurt istoric ##


Istoria formatului de fișier DXF datează din 1982, când a fost introdus ca parte a AutoCAD 1.0. Versiunile inițiale de AutoCAD acceptă numai formatul de fișier ASCII DXF. Odată cu lansarea 10 a AutoCAD (și mai sus) în 1988, în AutoCAD a fost introdus suport atât pentru formatul de fișier ASCII, cât și pentru formatul binar DXF. În etapele anterioare, Autodesk nu a partajat nicio specificație de format de fișier și, din această cauză, importurile corecte ale fișierelor DXF nu a fost ușoară. Cu toate acestea, Autodesk publică acum specificațiile DXF și sunt disponibile pentru publicul larg.

## Specificații de format de fișier ##

Formatul de fișier DXF utilizează codul grupului și perechile de valori pentru a aranja conținutul în secțiuni. Fiecare secțiune este compusă din înregistrări în care fiecare înregistrare constă dintr-un cod de grup și un articol de date. Fiecare cod de grup și valoare se află pe propria linie în fișierul DXF. Fiecare secțiune începe cu un cod de grup 0 urmat de șirul, SECȚIUNE. Acesta este urmat de un cod de grup 2 și de un șir care indică numele secțiunii (de exemplu, SECȚIUNEA1). Fiecare secțiune este compusă din coduri de grup și valori care îi definesc elementele. O secțiune se termină cu un 0 urmat de șirul ENDSEC.

Formatul de fișier DXF consideră obiectele diferite de entități. Obiectele nu au reprezentare grafică aici, dar entitățile o au. Astfel, intrările în DXF sunt denumite obiecte grafice, în timp ce obiectele obiecte sunt denumite obiecte negrafice. Secțiunile BLOC și ENTITATI ale fișierului DXF conțin Entități, iar utilizarea codurilor de grup în aceste două secțiuni este identică. Sfârșitul unei entități este indicat de următorul grup 0, care începe următoarea entitate sau indică sfârșitul secțiunii.

### Structura fișierului ###

Secțiunile dintr-un fișier DXF sunt aranjate în următoarea ordine:

|Sectiunea|Descriere de baza
---|---|
|Header|Această secțiune conține informații generale despre desen. Este ca și funcționalitatea Setări din telefon, care conține diferitele variabile asociate cu desenul și valorile asociate acestuia. De exemplu, secțiunea Antet va defini ce versiune AutoCAD folosește fișierul DXF (variabila $ACADVER) sau unitatea folosită pentru măsurarea unghiurilor din fișier (variabila $AUNITS)
|Clasuri|Secțiunea CLASE conține informații pentru clasele definite de aplicație ale căror instanțe apar în secțiunile BLOCURI, ENTITĂȚI și OBIECTE ale bazei de date.
|Tabele|Această secțiune conține definiții pentru mai multe tabele diferite, fiecare dintre ele conține un număr de intrări diferite de simbol. De exemplu, [tipul de linie](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) tabelul (LTYPE) definește modelul de liniuțe, puncte, text și simboluri din fișierul DXF și modul în care sunt scalate. Iată o listă completă a tabelelor găsite în această secțiune:<ul><li> Tabelul ID aplicației (APPID).</li><li> Tabel înregistrări bloc (BLOCK_RECORD).</li><li> Tabel de stil de dimensiune (DIMSTYPE).</li><li> Tabel de straturi (LAYER).</li><li> Tabel de tip de linie (LTYPE).</li><li> Tabel cu stil de text (STYLE).</li><li> Tabelul Sistemului de Coordonate al Utilizatorului (UCS).</li><li> Vizualizați (VIEW) tabelul</li><li> Tabelul de configurare viewport (VPORT).</li></ul>
|Blocuri|Această secțiune conține obiectele grafice și entitățile de desen care alcătuiesc fiecare referință de bloc din desen.
|Entități|Această secțiune conține datele obiectului real și entitățile grafice ale desenului. Aceasta poate include date brute – de exemplu, o entitate cerc este definită de grosimea sa, punctul central, raza și direcția de extrudare.
|Obiecte|Aici veți găsi părțile negrafice ale desenului. De exemplu, dicționarele AutoCAD sunt stocate aici.

## Referințe ##

* [Specificații fișier DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF de Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

