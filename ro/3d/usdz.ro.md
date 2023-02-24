{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "fișier usdz", "format fișier usdz", "format fișier", "3d", "descărcare fișier usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Formatul ZIP de descriere universală a scenei",
  "description":"Aflați despre formatul de fișier USDZ și despre API-urile care pot deschide și crea fișiere USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Ce este un fișier USDZ?

Un fișier cu .usdz este o arhivă ZIP necomprimată și necriptată pentru formatul de fișier [USD](/ro/3d/usd/) (Descrierea scenei universale) care conține și proxy pentru fișiere de alte formate (cum ar fi texturi și animații) încorporate în arhiva și le rulează direct cu timpul de execuție USD, fără a fi nevoie de despachetare. Fișierele USDZ sunt pachete al căror design se bazează pe noua abstractizare la nivel Ar a unui pachet. Usdz a fost înregistrat la IANA și are numele de tip media al modelului și un nume de subtip vnd.usd+zip, iar detaliile acestuia pot fi găsite pe [pagina de înregistrare IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Format de fișier USDZ

Fișierele USDZ se bazează pe formatul de fișier ZIP care arhivează fișierele individuale în containerul său. Acest lucru permite receptorului să dezarhiveze conținutul și să folosească fișierele normale de descriere a scenei USD pentru a lucra și a inspecta. Aproape toate sistemele de operare oferă suport încorporat pentru formatele de fișiere ZIP și alegerea acestui format de arhivare față de orice metodă personalizată face ușor ca fișierele USDZ să fie utile ca protocol de transport simplu.

### Constrângeri ZIP

Formatul de fișier USDZ utilizează formatul de fișier ZIP fără nicio „compresie” și „criptare”. Aceasta a fost concepută pentru a îndeplini două cerințe:

* Pentru un pachet deja încărcat în memorie sau ca un singur fișier pe disc, API-ul este disponibil în USD pentru accesarea datelor conținute în imagine
* Nu ar trebui să fie nevoie să extrageți fișiere pe disc sau să alocați mai mult spațiu de stocare heap

Cu USDZ, ambele cerințe sunt îndeplinite, deoarece majoritatea formatelor de imagine permit scheme interne de compresie, rezultând o dimensiune compactă a fișierului.

### Cerințe de aspect

Pachetele USDZ necesită aspectul fișierelor din pachet este ca datele pentru fiecare fișier să înceapă la un multiplu de 64 de octeți de la începutul pachetului. Cu toate acestea, pachetul ar trebui să înceapă cu un fișier nativ [USD](/ro/3d/usd/) în cazul țintirii pachetului cu o referință simplă. Într-un astfel de caz, acest prim fișier USD este denumit Stratul implicit. Clienții care doresc să livreze „conținut care poate fi transmis în flux” ar putea dori să ia în considerare și alte constrângeri de aspect.

## Descărcare fișier USDZ
Deoarece fișierele usdz sunt împachetate cu alte imagini de înaltă calitate și fișiere usd, ele pot ocupa mai mult spațiu de stocare pe disc. Aici puteți găsi un exemplu de fișier USDZ simplu și mai mic pentru descărcare:

- [Sample.usdz](../sample.usdz)

## Referințe

* [Specificații de format de fișier USDZ](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)
