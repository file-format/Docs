{
"data":"2023-11-09",
   "keywords":[
"grădină zoologică",
"fișier zoo",
"fișier comprimat zoo",
"cum se deschide un fișier zoo",
"fişier",
"extensie fișier zoo",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Fișier ZOO - Ce este un fișier .zoo și cum se deschide?",
   "description":"Aflați despre formatul de fișier ZOO Compressed și despre API-urile care pot crea și deschide fișiere ZOO.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Ce este un fișier ZOO?

Un fișier `.zoo` este un format de arhivă care este folosit pentru a comprima și stoca fișiere și directoare; este similar cu alte formate de arhivă precum `.zip`, `.tar` și `.rar`. Formatul `.zoo` a fost popular în primele zile ale calculului, dar a devenit mai puțin comun în ultimii ani. A fost dezvoltat inițial de **Rahul Dhesi** și a fost folosit în principal pe sisteme Unix și DOS.

Un fișier `.zoo` conține de obicei unul sau mai multe fișiere și directoare care au fost comprimate și arhivate într-un singur fișier. Puteți crea și extrage fișiere `.zoo` folosind diverse instrumente software care acceptă acest format.

Arhivele ZOO au o caracteristică unică care le permite să stocheze mai multe versiuni ale aceluiași fișier, cu condiția ca fiecare versiune să fi fost modificată la o dată diferită. Aceasta înseamnă că utilizatorii ZOO pot salva și accesa iterațiile anterioare ale fișierului direct din arhiva ZOO. Această caracteristică permite utilizatorilor să revină la versiunea anterioară a fișierului sau să compare versiunea mai veche cu una mai recentă, oferind o modalitate convenabilă de a gestiona revizuirile și modificările fișierelor în timp.

## Operațiuni obișnuite ale fișierelor ZOO

Iată câteva operațiuni comune asociate fișierelor `.zoo`:

1. **Crearea unui fișier `.zoo`:** Puteți utiliza un utilitar de linie de comandă precum "zoo" pentru a crea fișierul `.zoo`. De exemplu, următoarea comandă va crea arhiva `.zoo` din director:
    








`zoo a -c archive.zoo directory/`
    








În această comandă, "a" înseamnă "add", "-c" specifică compresia și "archive.zoo" este numele arhivei de ieșire.
    








2. **Extragerea fișierelor dintr-un fișier `.zoo`:** Pentru a extrage conținutul arhivei `.zoo`, puteți folosi o comandă ca aceasta:
    








`zoo e archive.zoo`
    








Această comandă va extrage fișiere din fișierul `archive.zoo`.
    








3. **Afișarea conținutului unui fișier `.zoo`:** Puteți lista conținutul arhivei `.zoo` fără a le extrage folosind opțiunea "l":
    








    








`zoo l archive.zoo`

## Cum se deschide un fișier ZOO?

Programele care deschid fișierele ZOO includ

- **zoo** (gratuit) pentru (Windows, Linux)

## Referințe
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
