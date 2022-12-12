{
  "date" : "2019-10-11",
  "keywords" :[ "fișier apng", "format fișier apng", "ce este un fișier apng", "fișier", "exemplu apng", "extensie fișier apng", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier APNG - Fișier grafic de rețea portabil animat",
  "description":"Aflați despre formatul fișierului APNG și despre API-urile care pot crea și deschide fișiere APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier APNG?

Un fișier cu extensia .apng (Animated Portable Network Graphics) este un format grafic raster și este o extensie neoficială a Portable Network Graphic ([PNG](/ro/image/png/) ). Este compus din mai multe cadre (fiecare din imaginea PNG) care reprezintă o secvență de animație. Acest lucru oferă o vizualizare similară cu un fișier [GIF](/ro/image/gif/). Fișierele APNG acceptă imagini pe 24 de biți și transparență pe 8 biți. APNG este compatibil cu fișierele GIF neanimate. Fișierele APNG folosesc aceeași extensie .png și pot fi deschise de aplicații precum Mozilla Firefox, Chrome cu suport APNG, aplicații iMessage pentru iOS 10.

## Scurt istoric

* Specificațiile APNG au fost create în 2004 pentru a oferi suport pentru imagini PNG animate
* Decodoarele APNG au fost dezvoltate cu dimensiuni mult mai mici și folosind partea din spate a decodorului PNG
* După deliberări continue, a fost formulat un nou tip MIME image/apng păstrând extensia la fel ca .png în loc de .apng
* APNG a fost respins oficial de grupul PNG pe 20 aprilie 2007 din cauza uniformității sale față de imaginile PNG, având în același timp specificații diferite

## Format de fișier APNG

Fișierele APNG sunt stocate ca fișiere binare pe disc și utilizează specificațiile extinse ale PNG pentru imagini animate. Primul cadru al unui fișier APNG este un flux PNG normal care poate fi citit de decodoarele PNG pentru afișare. Formatul de fișier APNG urmează specificațiile PNG, iar datele sunt stocate în segmente numite bucăți. Cu toate acestea, APNG a introdus următoarele bucăți noi:

`Animation Control Chunk (acTL)` - Indică faptul că acest fișier este un fișier PNG animat, mai degrabă decât un fișier PNG normal. Acționează ca un marker și vine înaintea fragmentului IDAT. Conține, de asemenea, numărul de cadre și informații despre orele pentru care animațiile sunt în buclă

`Frame Control Chunk` - Apare la începutul fiecărei informații și metadate, cum ar fi dimensiuni, poziție, aplicarea transparenței și informații de înlocuire cu cadrul precedent sau următor, odată ce acesta este încheiat.

`Frame Data Chunk` - Stochează conținutul cadrului și începe cu un număr de secvență. Acest număr de secvență are aceeași structură ca și fragmentul IDAT al imaginii implicite.

{{< figure src="../APNG.png" alt="Format de fișier PNG animat - APNG" >}}

APNG este compatibil cu PNG, deoarece specificațiile laterale au fost proiectate în așa fel încât o aplicație care citește un fișier PNG ar trebui să ignore pur și simplu bucățile pe care nu le înțelege. Specificațiile referitoare la adâncimea de biți, tipul de culoare, compresia, filtrele, metodele de întrețesere și informațiile despre paletă sunt utilizate la fel ca cele ale formatului PNG implicit.

## APNG vs GIF

Cu GIF-ul deja instalat și utilizat de-a lungul unei perioade lungi de timp, s-ar putea să vă întrebați cum este APNG diferit de GIF. Urmează un set de comparații între APNG și GIF, care oferă o scurtă idee despre ambele formate de fișiere.

||APNG|GIF|
---|---|---|
|Publicat|2004|1987|
|Adancime culoare|24 biti|8 biti|
|Frame Rate|Nelimitat|10 cadre pe secundă|
|Transparență|Complet și parțial|Complet|
|Compresie|Foarte bine|Bine|

## Referințe

* [Format fișier APNG](https://en.wikipedia.org/wiki/APNG)
* [Specificații oficiale de format PNG](https://www.w3.org/TR/PNG/)

