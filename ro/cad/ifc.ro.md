{
  "date" : "2020-03-16",
  "keywords" :[ "Fișier IFC", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier IFC și despre API-urile care pot crea și deschide fișiere IFC.",
  "title" :"Format fișier IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier IFC?

Fișierele cu extensia IFC se referă la formatul de fișier Industry Foundation Classes (IFC) care stabilește standarde internaționale pentru a importa și exporta obiecte de clădire și proprietățile acestora. Acest format de fișier oferă interoperabilitate între diferite aplicații software. Specificațiile pentru acest format de fișier sunt dezvoltate și menținute de buildingSMART International ca standard de date. Obiectivul final al formatului de fișier IFC este de a îmbunătăți comunicarea, productivitatea, timpul de livrare și calitatea pe tot parcursul ciclului de viață al unei clădiri.

Datorită standardelor stabilite pentru obiectele comune în industria construcțiilor, reduce pierderea de informații în timpul transmiterii de la o aplicație la alta. IFC poate deține date pentru geometrie, calcul, cantități, managementul instalațiilor, prețuri etc. pentru multe profesii diferite (arhitect, electricitate, HVAC, structural, teren etc.).

## Scurt istoric ##

Inițiativa IFC a fost luată în 1994 de Autodesk pentru a sprijini dezvoltarea de aplicații integrate și a inclus companii precum Honeywell, Butler Manufacturing și AT&T. În 1995, calitatea de membru a fost deschisă pentru oricine și numele a fost schimbat în Alianța Internațională pentru Interoperabilitate. Intenția organizației non-profit a fost de a publica Industry Foundation Class (IFC) ca model de produs AEC. În 2005, numele a fost din nou schimbat și buildSMART îl menține acum.

## Format de fișier IFC ##

Formatul de fișier IFC a suferit mai multe modificări în trecut pentru a ajunge la specificațiile formatului de fișier v4. Câteva modificări minore au avut loc din când în când, precum și acestea au fost făcute parte din specificații ca anexe. Mai jos este o listă cu diferite versiuni ale specificațiilor fișierelor care au fost făcute publice în trecut.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (martie 2013) ifcXML2x3 (iunie 2007)
* IFC2x3 (februarie 2006) ifcXML2 pentru IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (iulie 2004)ifcXML2 pentru IFC2x2 (RC1)
* IFC 2x2IFC 2x Addendum 1ifcXML1 pentru IFC2x și
* Addendum IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Cele mai recente versiuni ale specificațiilor de format de fișier IFC sunt întotdeauna disponibile pe site-ul web buildingSMART, iar dezvoltatorul ar trebui să le consulte pentru orice tip de aplicații pe care intenționează să le dezvolte. În momentul scrierii acestui articol, specificațiile versiunii 4 sunt cele mai recente disponibile online.

### Formate de fișiere de date IFC ###

Formatul de fișier IFF acceptă schimbul de date între aplicații folosind diferite formate, după cum este enumerat mai jos:

**IFC:** Acesta este formatul implicit de schimb IFC și utilizează structura fișierului fizic STEP conform ISO 10303-21. Acest format de fișier are extensia de fișier .ifc și este cel mai utilizat format IFC.

**IFC-XML:** Este o versiune în format de fișier XML a IFC care poate fi generată direct de aplicația de trimitere conform structurii ISO 10303-28, numită și STEP-XML. Formatul de fișier IFC-XML este considerat adecvat pentru interoperabilitatea între instrumentele XML. În comparație cu formatul de fișier IFC, IFC-XML este cu 300-400% mai mare ca dimensiune.

**IFC-ZIP:** Este o versiune [ZIP](/ro/compression/zip/) comprimată a IFC sau IFC-XML în care unul dintre aceste fișiere se află în directorul principal al arhivei zip. Acest format comprimă un fișier .ifc cu 60-80% și un fișier XML .ifc cu 90-95%.

### Arhitectura IFC ###

Specificația IFC include termeni, concepte și elemente de specificații de date care provin din utilizarea în cadrul disciplinelor, meseriilor și profesiilor din sectorul industriei de construcții și management al facilităților. Termenii și conceptele utilizează cuvinte simple în limba engleză, elementele de date din specificația datelor urmează o convenție de denumire.

numele elementelor de date pentru tipuri, entități, reguli și funcții încep cu prefixul „Ifc” și continuă cu cuvintele englezești din convenția de denumire CamelCase (fără liniuță de subliniere, prima literă a cuvântului cu majuscule); numele atributelor dintr-o entitate urmează convenția de denumire CamelCase fără prefix; definițiile setului de proprietăți care fac parte din acest standard încep cu prefixul „Pset_” și continuă cu cuvintele englezești din convenția de denumire CamelCase; definițiile setului de cantități care fac parte din acest standard încep cu prefixul „Qto_” și continuă cu cuvintele englezești din convenția de denumire CamelCase.

Arhitectura schemei de date a IFC definește patru straturi conceptuale, fiecare schemă individuală fiind atribuită exact unui strat conceptual.

**Strat de resurse** — cel mai de jos strat include toate schemele individuale care conțin definiții de resurse, acele definiții nu includ un identificator unic la nivel global și nu trebuie utilizate independent de o definiție declarată la un strat superior;

**Core layer** — următorul strat include schema kernelului și schemele de extensie de bază, conținând cele mai generale definiții ale entităților, toate entitățile definite la stratul de bază sau mai sus poartă un id unic la nivel global și opțional informații despre proprietar și istoric;

**Stratul de interoperabilitate** — următorul strat include scheme care conțin definiții de entități care sunt specifice unui produs general, proces sau specializare de resurse utilizate în mai multe discipline, aceste definiții sunt de obicei utilizate pentru schimbul între domenii și partajarea informațiilor de construcție;

**Strat de domeniu** — cel mai înalt nivel include scheme care conțin definiții de entități care sunt specializări ale produselor, proceselor sau resurselor specifice unei anumite discipline, acele definiții sunt de obicei utilizate pentru schimbul intradomeniu și schimbul de informații.

## Referințe ##

* [Cursuri Fundația Industriei - Prin Wikipedia](https://en.wikipedia.org/wiki/Clasuri_Fundația_Industriei)

