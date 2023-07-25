{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PDF/UA",
  "description":"Aflați despre formatul de fișier PDF/UA și despre API-urile care pot crea și deschide fișiere PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Ce este fișierul PDF/UA? #

PDF/UA a fost publicat ca [Standard ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) în august 2012 și este de departe prima definiție completă a unui set de cerințe pentru documentele PDF accesibile universal. Termenul „accesibil universal” se referă la înțelegerea faptului că informațiile conținute într-un document [PDF](/ro/pdf/) ar trebui să fie accesibile în mod egal și independent pentru toată lumea în general și pentru persoanele cu dizabilități în special. Introducerea standardului PDF/UA poate fi considerată un pas major pentru crearea de instrumente și aplicații pentru a crea și a citi conținut PDF.

## Cerințe de format de fișier ##

PDF/UA are la bază anumite cerințe clare care acționează ca esență a acestui standard. În esență, acestea se bazează pe etichetarea PDF-urilor, ceea ce înseamnă că toate documentele PDF/UA trebuie etichetate corect. De asemenea, necesită ca etichetele să fie adecvate din punct de vedere semantic și în ordine logică. Acest lucru asigură că documentul final creat cu specificațiile PDF/UA este mai fiabil și mai accesibil. Acest lucru îi poate aduce pe autorii PDF să se întrebe dacă trebuie să știe totul despre toate aceste cerințe? Din fericire, nu este așa, deoarece instrumentele de conformitate PDF/UA își asumă responsabilitatea pentru adăugarea și păstrarea accesibilității PDF-ului.

Cerințele de format de fișier pentru PDF/UA sunt următoarele.

* Conținutul este clasificat în unul din două moduri: conținut semnificativ și artefacte, cum ar fi elementele decorative ale paginii. Tot conținutul semnificativ trebuie să fie etichetat și integrat în structura arborelui tuturor etichetelor dintr-un document. Artefactele, pe de altă parte, trebuie doar marcate ca atare.
* Conținutul semnificativ trebuie să fie marcat cu etichete și, împreună cu celelalte etichete din document, să creeze un arbore de structură complet.
* Conținutul semnificativ trebuie să fie marcat cu etichetele semantice adecvate.
* Structura arborelui creat de etichetele documentului trebuie să reflecte ordinea logică de citire a documentului.
* Pot fi utilizate numai etichetele standard definite în PDF 1.7; dacă sunt folosite alte etichete, o intrare de atribuire a rolului trebuie să înregistreze ce etichetă standard reprezintă fiecare.
* Informațiile nu pot fi transmise numai folosind mijloace vizuale (de exemplu, contrast, culoare sau poziția pe pagină).
* Nu este permis niciun conținut care pâlpâie, clipește sau clipește, fie ca efecte controlate de JavaScript, fie ca parte a oricăror videoclipuri încorporate în PDF.
* Trebuie dat un titlu de document, iar documentul trebuie configurat astfel încât titlul (mai degrabă decât numele fișierului) să apară în titlul ferestrei.
* Limba întregului conținut trebuie notă, iar schimbările de limbă trebuie marcate explicit ca atare.

## Conformitate PDF/UA ##

Standardul PDF/UA definește specificațiile pentru conținut, cititori și tehnologie de asistență. Aceste trei aspecte sunt legate între ele în funcție de conținutul documentului. Cerințele de conformitate pentru fiecare dintre acestea sunt menționate mai jos.

## Fișiere conforme ##

Fișierele conforme cu standardul PDF/UA ar trebui să conțină funcții care sunt valide conform [specificațiilor PDF 1.7](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). Cu toate acestea, funcțiile care sunt interzise în mod specific de PDF/UA ar trebui excluse.

## Cititori conformi ##

Un cititor conform trebuie să respecte regulile specificate de specificațiile PDF 1.7. Mai exact, ar trebui să sprijine:

* toate etichetele, atributele și valorile cheie specificate pentru accesibilitate. De asemenea, ar trebui să aibă capacitatea de a procesa și reprezenta semnături digitale, adnotări și conținut opțional.
* procesează și reprezintă semnături digitale, adnotări și Conținut Opțional
* navigați în document printr-o varietate de mijloace

## Tehnologie de asistență conformă ##

O tehnologie de asistență conformă este obligată să accepte caracteristicile PDF/UA. Acestea includ, de exemplu, caracteristici ale conținutului și ale cititorului și ar trebui să permită navigarea după etichete de pagină, structura documentului sau schiță. De asemenea, ar trebui să permită utilizatorului să suprascrie zoom-ul implicit de navigare.

## Referințe ##

* [PDF/UA - Prin Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA pe scurt](https://pdfa.org/pdfua-in-a-nutshell/)

