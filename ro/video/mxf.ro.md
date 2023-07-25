{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Format de schimb de materiale",
  "keywords" :[ "MXF", "video matroska", "format mkv", "cum se redă fișiere MXF", "SMPTE", "multimedia", "video"],
  "description":"Aflați despre formatul de fișier MXF și despre API-urile care pot crea și deschide fișiere MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Ce este un fișier MXF?

Un fișier cu extensia .mxf este un format de container multimedia care conține medii video și audio digitale, împreună cu informații despre metadate despre fișier. Urmează standardul SMPTE (Society of Motion Picture and Television Engineers), care este o asociație globală de profesioniști din inginerie, tehnologie și directori care lucrează în industria mass-media și a divertismentului. Fișierele MXF pot fi convertite în alte formate de fișiere, cum ar fi [AVI](/ro/video/avi/) sau [MOV](/ro/video/mov/).

## Format de fișier MXF

Fișierele MXF sunt de fapt fișiere binare care constau dintr-o secvență de octeți într-un format definit. Aplicațiile de decodare trebuie să respecte acest format pentru a-l înțelege și a extrage informații din acesta. Formatul permite adăugarea de elemente noi fără a întrerupe compatibilitatea cu înapoi folosind codarea KLV, care este descrisă mai jos.

* Cheie – identificatorul elementului, o etichetă universală SMPTE (UL)
* Lungime – lungimea datelor care este codificarea cu lungime variabilă utilizată pentru a reduce cantitatea de spațiu necesară pentru acest articol
* Valoare – valoarea reală a elementului.

### Specificații de format SMPTE

Formatul de fișier MXF a fost definit de următoarele specificații SMPTE.

* SMPTE ST 377-1:2011. Televiziune — Format de schimb de materiale (MXF) — Specificație de format de fișier
* SMPTE ST 377-2 (lucrări în curs din ianuarie 2012). Sintaxa extensiei codificate KLV pentru MXF.
* SMPTE ST 378:2004 (Arhivat 2010). Televiziune — Format de schimb de materiale (MXF) — Model operațional 1a (un singur articol, un singur pachet)
* SMPTE ST 379-1:2009. Format de schimb de materiale (MXF) — Container generic MXF
* SMPTE ST 379-2:2010. Format de schimb de materiale (MXF) -- MXF Constrained Generic Container
* SMPTE ST 380:2004. Televiziune — Format de schimb de materiale (MXF) — Schema de metadate descriptive-1 (Standard, Dinamic)
* SMPTE ST 381-1:2005. Televiziune — Format de schimb de materiale (MXF) — Maparea fluxurilor MPEG în containerul generic MXF (dinamic)
* SMPTE ST 381-2:2011. Format de schimb de materiale (MXF) — Maparea fluxurilor MPEG în containerul generic MXF constrâns
* SMPTE ST 382:2007. Format de schimb de materiale (MXF) — Maparea fluxurilor AES3 și a sunetului de difuzare a valului la containerul generic MXF
* SMPTE ST 383:2008. Televiziune — Format de schimb de materiale (MXF) — Maparea datelor DV-DIF la containerul generic MXF
* SMPTE ST 384:2005. Televiziune — Format de schimb de materiale (MXF) — Maparea imaginilor necomprimate în containerul generic MXF
* SMPTE ST 385:2004. Televiziune — Format de schimb de materiale (MXF) — Maparea esenței și metadatelor SDTI-CP în containerul generic MXF
* SMPTE ST 386:2004 (Arhivat 2010). Televiziune — Format de schimb de materiale (MXF) — Maparea datelor de esență tip D-10 la containerul generic MXF
* SMPTE ST 387:2004 (Arhivat 2010). Televiziune — Format de schimb de materiale (MXF) — Maparea datelor de esență tip D-11 la containerul generic MXF
* SMPTE ST 388:2004 (Arhivat 2010). Televiziune — Format de schimb de materiale (MXF) — Maparea audio codificat A-law în containerul generic MXF
* SMPTE ST 389:2005. Televiziune — Format de schimb de materiale (MXF) — Element de sistem de redare inversă a containerului generic MXF
* SMPTE ST 390:2011. Televiziune — Format de schimb de materiale (MXF) — Model operațional specializat „Atom” (Reprezentare simplificată a unui singur articol)
* SMPTE ST 391:2004 (Arhivat 2010). Televiziune — Format de schimb de materiale (MXF) — Model operațional 1b (articol unic, pachete grupate)
* SMPTE ST 392:2004. Televiziune — Format de schimb de materiale (MXF) — Model operațional 2a (Articole din lista de redare, pachet unic)
* SMPTE ST 393:2004. Televiziune — Format de schimb de materiale (MXF) — Model operațional 2b (Elemente din listă de redare, pachete grupate)
* SMPTE ST 394:2006. Televiziune — Format de schimb de materiale (MXF) — Schema de sistem 1 pentru containerul generic MXF
* SMPTE ST 405:2006. Televiziune — Format de schimb de materiale (MXF) — Elemente și elemente de date individuale pentru schema 1 de sistem generic de containere MXF
* SMPTE ST 407:2006. Televiziune — MXF — Modele operaționale 3a și 3b
* SMPTE ST 408:2006. Televiziune — MXF — Modele operaționale 1c, 2c și 3c
* SMPTE ST 410: 2008. Material Exchange Format - Generic Stream Partition.
* SMPTE ST 422:2006. Format de schimb de materiale — Maparea fluxurilor de cod JPEG2000 în containerul generic MXF
* SMPTE ST 429.4:2006. Ambalare D-Cinema — Aplicație MXF JPEG 2000
* SMPTE ST 429.5:2006. D-Cinema Packaging — Fișier de urmărire cu text temporizat
* SMPTE ST 429.6:2006. D-Cinema Packaging — Criptare MXF Track File Essence
* SMPTE ST 434:2006. Format de schimb de materiale — Codificare XML pentru metadate și informații despre structura fișierului
* SMPTE ST 436:2006. Televiziune — Mapări MXF pentru linii VBI și pachete de date auxiliare
* SMPTE ST 2019-4:2009. Maparea unităților de codare VC-3 în containerul generic MXF
* SMPTE ST 2037:2009. Maparea VC-1 în containerul generic MXF
* SMPTE RP 2008:2008. Format de schimb de materiale — Maparea fluxurilor AVC în containerul generic MXF
* SMPTE RP 2057:2011. Transport de metadate pe bază de text în MXF
* SMPTE EG 41:2004. Format de schimb de materiale (MXF) — Ghid de inginerie. Notă: Acest document nu mai era listat pe site-ul web SMPTE când a fost consultat în ianuarie 2012.
* SMPTE EG 42:2004. Format de schimb de materiale (MXF) — Metadate descriptive MXF
* SMPTE RDD 3:2008. Specificație de interoperabilitate e-VTR MXF
* SMPTE RDD 9-2009. Specificația de interoperabilitate MXF a produselor Sony MPEG Long GOP
* Meniul foii de calcul pentru registrul de metadate SMPTE.

### Metadate structurale MXF

Metadatele structurale sunt fundamentale într-un fișier MXF, deoarece conțin informații utile despre conținutul fișierului. Metadatele MXF conțin informații precum rata de cadre, dimensiunea cadrului, data creării fișierului și data modificării personalizate. Metadatele structurale descriu structura și capacitățile unui fișier MXF, care include descrierea tehnică a diferitelor componente esențiale și transmiterea modului în care este compusă cronologia de ieșire.

## Referințe

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Raport de progres](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Biblioteca OpenSource C++ pentru MXF](http://www.freemxf.org/)

