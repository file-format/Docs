{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "fișier", "extensie", "format fișier", "Aspect pagină", "PostScript încapsulat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier EPS și despre API-urile care pot crea și deschide fișiere EPS.",
  "title" :"Format fișier EPS - Fișier PostScript încapsulat",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier EPS?

Un fișier .eps este un fișier imagine care este salvat pe disc în format de fișier Postscript încapsulat. Poate conține orice combinație de text, grafică și imagini. Fișierele EPS pot include, de asemenea, o imagine de previzualizare bitmap încapsulată în interior pentru afișare de către aplicațiile care pot deschide astfel de fișiere.

## Scurt istoric al formatului de fișiere EPS

O privire rapidă asupra formatului de fișier EPS din perspectiva istoricului dezvăluie următoarele informații:

* Prima versiune de EPS a fost lansată de Adobe cândva între 1985 și 1988
* Versiunea 2.0 a specificației EPS a fost publicată în ianuarie 1989
* Specificația pentru versiunea 3.0 a EPS a fost publicată ca document separat în 1992; aceasta este cea mai recentă versiune publicată.

EPS, în combinație cu mecanismul de extensie Open Structuring Conventions descris în clauza 9 din Specificația Adobe pentru convențiile de structurare a documentelor în limbajul PostScript, a format baza versiunilor timpurii ale formatului de fișier Adobe Illustrator Artwork.

## Format de fișier EPS

EPS este un format proprietar, dar documentat public, iar specificațiile formatului de fișier EPS sunt disponibile public pentru referință de către dezvoltatori. EPS este un format de fișier conform [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) și respectă toate regulile stabilite de DSC. DSC este un format de fișier special pentru documentele PostScript de la Adobe. Orice aplicație care pretinde că poate citi fișiere EPS ar trebui să fie compatibilă cu DSC.

Un fișier EPS este format din două secțiuni principale, așa cum este explicat mai jos.

### Imagine de previzualizare ###

Un fișier EPS tipic conține o imagine de previzualizare într-un format destinat utilizării convenabile într-un flux de lucru care implică mai multe sisteme sau aplicații. Intenția unei previzualizări este de a avea o imagine într-un format pe care majoritatea aplicațiilor grafice îl pot reda; o previzualizare are de obicei o rezoluție mai mică, în dimensiuni de pixeli și/sau în adâncime de biți. Fișierul de previzualizare poate fi într-unul dintre mai multe formate. Specificația pentru EPS_3 enumeră trei formate de previzualizare „specifice dispozitivului”:

* pentru Apple Macintosh, o imagine PICT așa cum este utilizată de aplicația QuickDraw
* pentru computerele DOS, un bitmap TIFF
* Windows Metafile.

PICT și Windows Metafile pot încorpora atât date bitmap, cât și grafică vectorială. În plus, specificația definește o reprezentare foarte simplă, independentă de dispozitiv, pentru o imagine de previzualizare încorporată bitmap. Această reprezentare este cunoscută sub denumirea de format de interschimb PostScript Encapsulat (EPSI).

O previzualizare EPSI este un bitmap reprezentat ca ASCII hexazecimal, cuprins între câteva comentarii PostScript pentru identificare și destinat să fie simplu și ușor de transportat. Pentru a distinge fișierele EPS cu diferite formate de previzualizare, în specificația EPS au fost recomandate diferite extensii de fișiere DOS și tipuri de fișiere Macintosh.

### Cod PostScript

Formatul de fișier EPS trebuie să includă cel puțin următoarele:

* un comentariu de antet, %!PS-Adobe-3.0 EPSF-3.0
* și un comentariu pentru caseta de delimitare, %%BoundingBox: llx lly urx ury, care descrie limitele ilustrației. Aceste patru argumente corespund colțurilor din stânga jos (llx, lly) și din dreapta sus (urx, ury) ale casetei de delimitare.

Un fișier EPS nu poate folosi niciunul dintre următorii operatori:

* dispozitiv cu bandă,
* cleardictstack
* copiaza pagina
* ștergere pagină
* exitserver
* cadru dispozitiv
* grestoreall
* initclip
* initgraphics
* initmatrix
* părăsi
* benzi de randare
* setglobal
* setpagedevice
* setshared
* începe munca.

## Conversia EPS în alte formate de fișiere

Fișierele EPS pot fi convertite în formate standard de imagine, cum ar fi [JPG](/ro/image/jpeg/), [PNG](/ro/image/png/), [TIFF](/ro/image/tiff/) și [PDF](/ro/pdf/) folosind diferite aplicații, de exemplu Adobe Illustrator, Photoshop și PaintShop Pro.

Din cauza unei [vulnerabilitati de securitate](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) în fișierele EPS, Office 2016, Office 2013, Office 2010 și Office 365 au dezactivat capacitatea de a insera fișiere EPS în documentele Office.

## Referințe

* [Encapsulated PostScript - De Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

