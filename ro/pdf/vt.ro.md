{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PDF/VT",
  "description":"Aflați despre formatul de fișier PDF/VT și despre API-urile care pot crea și deschide fișiere PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Ce este PDF/VT? #

PDF/VT, publicat ca [ISO 16612-2](https://www.iso.org/standard/46428.html) în august 2010 ca standard, este conceput pentru a permite tipărirea documentelor variabile (VDP) într-o varietate de medii. Standardul face ca informațiile variabile și imprimarea tranzacțională să fie baza pentru standard. Imprimarea datelor variabile este utilizată atunci când o parte din informații este diferită pentru fiecare destinatar al conținutului. Imprimarea tranzacțională include facturi, extrase de cont și alte documente care combină informațiile de facturare cu informații de marketing. Acest lucru are ca rezultat o combinație de procesare îmbunătățită a imaginilor, textului și a altor tipuri de conținut. PDF/VT permite gestionarea fiabilă și dinamică a paginilor pentru datele de tipărire High Volume Transactional Output (HVTO) prin utilizarea conceptului de metadate ale părții documentului (DPM). Fișierele PDF/VT pot fi deschise în Adobe Acrobat Viewer fără a fi nevoie să adăugați nicio altă componentă.

## Ierarhia părților documentului ##

Ierarhia părții documentului (DPart) este ca o structură arborescentă a nodurilor părții documentului care se bazează pe toate paginile documentului. Elementele acestui arbore se numesc noduri DPart. Fiecare nod intern conține alte noduri DPart și fiecare nod frunză specifică una sau mai multe pagini pentru un destinatar. În esență, ierarhia DPart specifică secvența și relația documentelor sau părților de documente dintr-un fișier PDF/VT. Structura arborescentă a nodurilor DPart reprezintă cu ușurință conținutul intern al unui document PDF/VT, deoarece poate conține sub-documente pentru mulți destinatari și fiecare parte a documentului corespunde paginilor pentru un singur destinatar. Ierarhia DPart este necesară în fișierele PDF/VT.

## Metadatele părții documentului (DPM) ##

Metadatele părții documentului (DPM) sunt asociate fiecărui nod din ierarhia părții documentului și pot fi utilizate pentru a comunica informații despre subdocumentul și părțile acestuia ale unui anumit destinatar. În special, DPM poate conține informații despre proprietăți sau informații despre destinatari într-o formă codificată.

## Niveluri de conformitate ##

PDF/VT este conferit următoarelor trei niveluri de conformitate. Toate acestea se bazează pe [PDF](/ro/pdf/) 1.6.

* `PDF/VT-1` - Se bazează pe PDF/X-4 și conține toate resursele necesare pentru redarea unui document PDF.
* `PDF/VT-2` - Proiectate pentru schimbul de fișiere multiple, documentele PDF/VT-2 pot face referire la intenții de ieșire externă, conținut extern sau ambele. Un document PDF/VT și toate fișierele PDF la care se face referire și intențiile de ieșire externă sunt denumite în mod colectiv un set de fișiere PDF/VT-2. Acrobat 9 și acceptă această caracteristică.
* `PDF/VT-2s` - Suporta PDF/VT-2 streaming live. Acest lucru permite procesarea secțiunilor segmentate de date.

## Referințe ##

* [PDF/VT - După Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [Tehnologie grafică ISO 16612-2](https://www.iso.org/standard/46428.html)

