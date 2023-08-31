{
  "date" : "2020-01-10",
  "keywords" :[ "fișier otg", "format fișier otg", "ce este un fișier otg", "fișier", "exemplu otg", "extensie fișier otg", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument Drawing Template File Format",
  "description":"Aflați despre formatul de fișier OTG și despre API-urile care pot crea și deschide fișiere OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Ce este un fișier OTG?

Un fișier OTG este un șablon de desen care este creat folosind standardul OpenDocument care urmează OASIS Office Applications [specificația 1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Reprezintă organizarea implicită a elementelor de desen pentru o imagine vectorială care poate fi folosită pentru a îmbunătăți și mai mult conținutul fișierului. Fișierele OTF sunt ca orice alte fișiere bazate pe format OpenDocument care se bazează pe formatul XML pentru a reprezenta conținutul documentului. Fișierele OTF pot fi vizualizate prin deschiderea lor în orice editor de text sau XML standard.

## Specificații pentru formatul fișierului OTG ##

Formatul de fișier OTG se bazează pe formatul OpenDocument XML care are o schemă bine stabilită. Structura fiecărei componente a unui format OpenDocument este reprezentată de un element care are atribute asociate și este comună pentru toate tipurile de documente, cum ar fi documentul text, foaia de calcul sau un desen. OTG, fiind un șablon de desen, utilizează în mod extensiv specificațiile de conținut grafic care includ:

* Caracteristici îmbunătățite ale paginii pentru aplicații grafice
* Desenarea formelor
* Rame
* Forme 3D
* Formă personalizată
* Forme de prezentare
* Animații de prezentare
* Animații de prezentare SMIL
* Evenimente de prezentare
* Câmpuri de text prezente
* Conținutul documentului de prezentare

### Funcții îmbunătățite ale paginii pentru aplicații grafice ###
#### Fișă Master ####

Elementul Fișă Master este un șablon pentru generarea automată a paginilor de fișe pentru aplicațiile care acceptă tipărirea unor astfel de pagini.
Atributele care pot fi asociate cu `<style:handout-master> ` element sunt:

|Aspect|Atribut|Descriere
---|---|---|
|Aspect pagină de prezentare|prezentare:presentation-page-layout-name|Legături către `<style:presentation-page-layout>`  atribut
|Aspect pagină|`style:nume-aspect-pagină` | Specifică un aspect de pagină care conține dimensiunile, chenarul și orientarea paginii principale a fișei.
|Stilul paginii|`draw:style-name`|Atribuie atribute de formatare suplimentare unei pagini de master a fișei prin alocarea unui stil de pagină de desen.|
|Declarație antet| `prezentare:use-header-name`| Specifică numele declarației câmpului antet care este utilizat pentru toate câmpurile antet care sunt afișate pe pagina principală a fișei.
|Declarație de subsol| presentation:use-footer-name|Specifică numele declarației câmpului de subsol care este utilizat pentru toate câmpurile de subsol care sunt afișate pe pagina principală a fișei.
|Declarație de dată și oră|use-date-time-name|Specifică numele declarației câmpului dată-oră care este utilizată pentru toate câmpurile dată-oră care sunt afișate pe pagina principală a fișei.

### Desenarea formelor ###
Formatul OpenDocument acceptă mai multe forme de desen care pot fi folosite de orice tip de document.

|Forma|Atribute asociate| elemente
---|---|---|
Dreptunghi - `<draw:rect> `|Poziție, Dimensiune, Stil, Strat, Index Z, ID, ID subtitrare, Ancoră text, fundal tabel, poziția finală a desenului, Colțuri rotunjite|Titlu, Descriere lungă, Ascultători de evenimente, Puncte de lipire, Text
Linia `<draw:line> `|Stil, Layer, Z-Index, ID, Caption ID și Transformare, Ancoră text, fundal tabel, poziția finală a desenului, Punct de început, Punct final|Titlu, Descriere lungă, Ascultători de evenimente, Puncte de lipire, Text
Polilinie `<draw:polyline> `| Poziție, Dimensiune, Casetă de vizualizare, Stil, Strat, Index Z, ID, ID-ul subtitrării și Transformare, Ancora text, fundalul tabelului, poziția finală a desenului, Puncte| Titlu, descriere lungă, ascultători de evenimente, puncte de lipire, text
Poligonul `<draw:polygon> `|Poziție, Dimensiune, Casetă de vizualizare, Stil, Strat, Index Z, ID, ID-ul subtitrării și Transformare, Ancoră text, fundal tabel, poziție finală a desenului, Puncte|Titlu, Descriere lungă, Ascultători de evenimente, Puncte de lipire, Text
|Poligon regulat `<draw:regular-polygon> `|Poziție, Dimensiune, Stil, Strat, Index Z, ID, ID-ul subtitrării și Transformare, Ancora textului, fundalul tabelului, poziția finală a desenului, Concav, Colțuri, Claritate|Titlu, Descriere lungă, Ascultători de evenimente, Puncte de lipire, Text
|Calea `<draw:path> `|Poziție, Dimensiune, Casetă de vizualizare, Stil, Strat, Index Z, ID, ID-ul subtitrării și Transformare, Ancora textului, fundalul tabelului, poziția finală a desenului, Datele căii| Titlu, descriere lungă, ascultători de evenimente, puncte de lipire, text

### Rame ###
Un cadru, într-un document de desen este un container dreptunghiular care conține casete de text, imagini sau obiecte. Cadrele acceptă funcții suplimentare, cum ar fi contururi, hărți imagine și hyperlinkuri. Un cadru poate conține atât un obiect cât și o imagine, permițând astfel să aveți mai multe redări ale unui obiect. Aplicațiile redă elementul respectiv pe baza celui mai bun suport.

Ramele pot conține:
* Casete de text
* Obiecte reprezentate fie în format OpenDocument, fie într-un format binar specific obiectului
* Imagini
* Applet-uri
* Plug-in-uri
* Rame plutitoare

Un cadru este conținut într-un document, așa cum se arată mai jos.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referințe ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

