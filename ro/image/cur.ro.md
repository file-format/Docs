{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extensie", "fișier", "format", "imagine", "Bitmap independent de dispozitiv", "Format fișier cursor", "Cursor", "Windows", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR – Formatul fișierului cursor",
  "description":"Aflați despre formatul fișierului CUR și despre API-urile care pot crea și deschide fișiere CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier CUR? ##

Un fișier CUR este un format de fișier cursor static Microsoft Windows. Practic, ele sunt imagini staționare identice cu fișierele ICO (pictograme) din toate punctele de vedere, cu excepția extensiei. Atât CUR, cât și [ICO](/ro/image/ico/) sunt stabilite pe baza specificației Bitmap independent de dispozitiv [DIB](/ro/image/dib/) (Device-Independent Bitmap). Implicit, precum și cursorul personalizat, cum ar fi indicatorul mouse-ului Windows pentru sistemul de operare Windows, sunt stocate în fișierele CUR. Poate fi o săgeată pentru utilizare normală, o clepsidră care se rotește pentru a demonstra perioadele de așteptare sau o bară I pentru editarea textului. Fișierele CUR vin împreună cu pachetul de instalare al temelor personalizate de desktop pentru a se asigura că cursorul Windows se potrivește cu tema personalizată de desktop.

## Specificație tehnică ##

Fișierele CUR sunt fișiere de sistem binare care pot fi găsite pe dispozitivele care funcționează pe sistemul de operare Microsoft Windows. Imaginile pointer CUR vin în diferite dimensiuni standard, cum ar fi 16×16, 32×32 etc. Fișierele CUR sunt foarte asemănătoare cu fișierele ICO; ambele constau din mici imagini staţionare. Doar extensia fișierelor CUR și ICO sunt diferite. În plus, explicația unui hotspot din antetul fișierului CUR este diferită de fișierul ICO. Hotspot-ul interpretează decalajul pixelilor din colțul din stânga sus până la locul în care îndreptați mouse-ul. Sistemele Windows încă folosesc fișierele CUR, dar acum cursoarele animate au de obicei extensia de fișier ANI în loc de CUR.

## Scurt istoric ##

Fișierul CUR este realizat din fișierul ICO. Primul format de fișier CUR a fost încorporat în sistemul de operare Microsoft Windows 1.0 în 1981 pentru a ușura utilizarea comercială. În curând au fost introduse mai multe cursore interactive, permițând utilizatorilor să-și modifice preferințele de cursor din opțiunile preinstalate disponibile. Cu toate acestea, este ușor să editați un fișier CUR pe cont propriu, chiar dacă aveți cunoștințe tehnice insuficiente.


## Exemplu CUR ##

Fișierele CUR pot fi găsite la *C:\Windows\Cursors*:

{{< figure src="../cur.png" alt="Format de fișier CUR" >}}

