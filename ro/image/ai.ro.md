{
  "date" : "2021-01-21",
  "keywords" :[ "fișier ai", "format fișier ai", "ce este un fișier ai", "fișier", "exemplu ai", "extensie fișier ai", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI – Fișier ilustrativ Adobe Illustrator",
  "description":"Aflați despre formatul de fișier AI și despre API-urile care pot crea și deschide fișiere AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Ce este un fișier AI?

Un fișier cu o extensie .ai este un fișier Adobe Illustrator Artwork care conține grafică vectorială într-o singură pagină. folosește puncte pentru a crea căi de afișare a datelor de imagine, protejând astfel de pierderea calității imaginii dacă este mărită. Formatul de fișier AI se bazează pe formatul de fișier PGF, care este similar cu fișierele AI. Formatul AI își găsește utilizarea majoră pentru logo-uri și suporturi de imprimare, iar versiunile sale inițiale au fost considerate similare cu cea a fișierelor [EPS](/ro/image/eps/). Fișierele AI pot fi deschise cu instrumentele Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro și CorelDraw Graphics.

## Format de fișier AI

AI este formatul de fișier proprietar al Adobe Illustrator și folosește abordarea cu cale dublă similară cu PGF pentru salvarea fișierelor compatibile cu EPS. [Specificațiile formatului de fișier Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) oferă o informație detaliată referința dezvoltatorului pentru detalii interne ale acestui format de fișier. Toate documentele (fișierele) create de Adobe Illustrator sunt documente în limbaj PostScript și au două părți principale conforme cu Convențiile de Structurare a Documentelor: un `prolog` și un `script`.

### Prolog

Secțiunea prolog încapsulează informațiile necesare pentru interpretarea fișierului. Un exemplu ar fi caseta de delimitare care conține toate semnele de pe pagină. De asemenea, conține informații despre resurse, cum ar fi fonturile și definițiile procedurilor. Aceste resurse sunt grupate logic în seturi numite procsets și conțin metode explicite de inițializare și terminare a procedurilor lor.

### Script

Elementele grafice de pe pagină sunt descrise de script. Un script conține referințe la operatorii și procedurile din prolog, împreună cu operanzi și date. Cele trei secțiuni logice ale unui script includ:

* Setup Sequence - care inițializează și activează resursele definite în prolog
* Secvență de operatori descriptivi
* Trailer care dezactivează resurse

Operatorii din script sunt secvențe de elemente grafice scrise în limbajul definit de procsets din prolog. Aceste secvențe constau din colecții de elemente de date, definiții de atribute grafice și apeluri la procedurile definite în procese.

### Etichete obiect

Etichetele obiectelor sunt folosite pentru a atașa informații personalizate la un obiect de artă Adobe Illustrator. Etichetele constau din:

* Identificator de etichetă
* Tipul etichetei
* Date

## Referințe
* [Specificații de format de fișier Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Format de fișier AI de PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

