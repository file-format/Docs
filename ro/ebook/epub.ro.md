{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "fișier", "extensie", "format", "Carte electronică", "Carte digitală"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier EPUB și despre API-urile care pot crea și deschide fișiere EPUB.",
  "title" :"Ce este un fișier EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Ce este un fișier EPUB?

Fișierele cu extensia .epub sunt un format de fișier de carte electronică care oferă un format standard de publicație digitală pentru editori și consumatori. Formatul a fost atât de comun până acum încât este acceptat de multe cititoare electronice și aplicații software. De exemplu, pe Mac OS, software-ul preinstalat **Cărți** oferă suport pentru deschiderea unor astfel de fișiere. În plus, există o mulțime de software compatibil disponibile pentru smartphone-uri, tablete și computere. Standardele fișierelor EPUB sunt menținute de [Forumul Internațional de Publicare Digitală](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Versiunea EPUB 3 este, de asemenea, aprobată de Book Industry Study Group (BISG), o asociație lider în comerțul cărții pentru cele mai bune practici standardizate, cercetare, informații și evenimente, pentru ambalarea conținutului.

## Scurt istoric al formatului de fișier EPUB

* **Octombrie 2007** - EPUB 2.0 a fost aprobat
* **Septembrie 2010** - Actualizarea de întreținere a fost lansată
* **Octombrie 2011** - specificațiile EPUB 3.0 au intrat în vigoare
* **Iunie 2014** - A fost lansată o actualizare minoră de întreținere pentru a înlocui versiunea 3.0
* **Ianuarie 2017** - EPUB 3.1 a intrat în vigoare

## Format de fișier EPUB

Formatul de fișier EPUB este o arhivă care poate fi redenumită în extensia [ZIP](/ro/compression/zip/), iar conținutul acesteia poate fi vizualizat prin extragerea arhivei cu orice extractor de arhive. Este un format deschis bazat pe XML și constă din fișiere HTML, imagini, foi de stil CSS și alte elemente. De asemenea, poate fi convertit în PDF, Mobi și în alte câteva formate de fișiere printr-o serie de aplicații software și API-uri.

{{< figure src="../epub.png" alt="Format de fișier EPUB" >}}

**E-Book EPUB deschis cu aplicația Mac OS Books**

Formatul de fișier EPUB se bazează pe următoarele trei standarde deschise.

### Structură publică deschisă (OPS) ###

Un fișier EPUB 2.0 utilizează XHTML 1.1 pentru a construi conținutul unei publicații. În esență, aceasta înseamnă că un fișier EPUB este format din una sau mai multe pagini web. Chiar dacă ai putea include întregul conținut al unei cărți sau ziar într-o singură pagină, este mai bine ca un astfel de fișier să nu depășească 300K, atât din motive de performanță, cât și din motive de compatibilitate. La fel ca în cazul paginilor web obișnuite, stilul și aspectul sunt definite folosind foi de stil în cascadă (CSS). În fișierele EPUB trebuie utilizat un subset (serie limitată de comenzi) de CSS2. Multe dintre noile caracteristici ale CSS3, cum ar fi casetele rotunjite sau umbrele, nu sunt încă disponibile. Pentru compatibilitate inversă, un creator poate folosi și DTBook în loc de XHTML pentru a codifica conținutul.

### Format de ambalare deschis (OPF) ###

Această parte a specificațiilor tratează informații structurale, cum ar fi metadate (cine este autorul și editorul, care este titlul, ..), manifestul (o listă a tuturor fișierelor dintr-un fișier epub) și cuprinsul. Aceste date sunt toate încorporate folosind XML.

### Format container deschis (OCF) ###

Deoarece descrierile de mai sus ar fi trebuit să fie clar, un document EPUB constă dintr-o serie de fișiere. Specificațiile OCF definesc modul în care toate acele fișiere ajung să fie împachetate într-un singur fișier container. Pentru aceasta este folosită compresia ZIP.

## Formate de fișiere imagine acceptate ##

Formatul de fișier EPUB acceptă următoarele formate de fișiere imagine.

* [GIF](/ro/image/gif/)
* [JPG](/ro/image/jpeg/)
* [PNG](/ro/image/png/)
* [SVG](/ro/page-description-language/svg/)

## Referințe ##

* [EPUB - După Wikipedia](https://en.wikipedia.org/wiki/EPUB)

