{
  "date" : "2021-02-10",
  "keywords" :[ "fișier jpf", "format fișier jpf", "ce este un fișier jpf", "fișier", "exemplu jpf", "extensie fișier jpf", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPF - Format fișier imagine",
  "description":"Aflați despre formatul de fișier JPF și despre API-urile care pot crea și deschide fișiere JPF.",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Ce este un fișier JPF? ##

Un fișier cu extensia .jpf este o extensie a sistemului de codare a imaginilor JPEG 2000 ISO/IEC 15444 și este denumit Partea 2 ISO/IEC 15444-2. Acesta definește și specifică un set de metode de compresie fără pierderi (conservare a biților) și cu pierderi pentru codificarea imaginilor statice digitale cu tonuri continue, bi-nivel, în scară de gri, color sau imagini cu mai multe componente. Prima parte a ISO/IEC 15444-1 se referă la [JP2](/ro/image/jp2/) care utilizează tehnologia wavelet pentru a codifica conținut fără pierderi și este baza pentru formatele de fișiere imagine JPEG 2000. Formatul de fișier JPF nu a primit o recepție caldă din cauza utilizării extinse a formatului JPEG. Fișierele JPF pot fi deschise cu aplicații de imagine populare, cum ar fi Adobe Photoshop 2020, Adobe Illustrator 2020 și CorelDraw Graphics Suite 2020.

## Scurt istoric

În 2000, comitetul Joint Photographic Experts Group a proiectat JP2 cu obiectivul de a-și îmbunătăți propriul standard JPEG bazat pe transformarea cosinusului discret cu această nouă metodă bazată pe wavelet. Comitetul JPEG și-a propus să ofere metodele de bază fără taxe de licență. În licența JP2 câștigând concurență între 20 de companii, acestea au câștigat cu o mustață. JPEG 2000 a fost declarat ca standard ISO, deși majoritatea browserelor web nu sunt pregătite să dea o mână de ajutor JPEG 2000 din 2017. În 2004, formatul ISO/IEC 15444-2 a fost acceptat public ca extensie a formatului de fișier JP2.

## Format de fișier JPF

Formatul de fișier JPF definește procesele de decodare extinse pentru conversia datelor de imagine comprimate pentru reconstrucție. Este un format de fișier extins care specifică sintaxa fluxului de cod extins care conține informații pentru interpretarea datelor de imagine comprimate. Acest standard extins specifică un container pentru stocarea metadatelor imaginii și oferă îndrumări cu privire la procesele extinse de codare pentru conversia datelor de imagine sursă în date de imagine comprimate.

### Organizarea fișierelor

JPF este formatul formal de fișier de stocare atunci când fișierele JPX sunt stocate în sistemele de fișiere ale computerului. În plus, alte Recomandări/Standarde Internaționale pot defini alte casete pentru utilizare în fișierele JPX. Cu toate acestea, toate informațiile conținute într-un fișier JPX trebuie să fie în format casetă; Fluxurile de octeți care nu sunt în format casetă nu vor fi găsite în fișier. Structura binară a unei casete dintr-un fișier JPX este identică cu cea definită în formatul de fișier [JP2](/ro/image/jp2/).

## Referințe ##

* [Prezentare generală despre JPEG 2000](https://jpeg.org/jpeg2000/)
* [ISO/IEC 15444-2:2004](https://www.iso.org/standard/33160.html)

