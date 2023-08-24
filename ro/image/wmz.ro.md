{
  "date" : "2019-10-11",
  "keywords" :[ "fișier wmz", "format fișier wmz", "ce este un fișier wmz", "fișier", "exemplu wmz", "extensie fișier wmz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier WMZ - Metafișier Windows comprimat",
  "description":"Aflați despre formatul de fișier WMZ și despre API-urile care pot crea și deschide fișiere WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Ce este un fișier WMZ?

Un fișier cu extensia .wmz este o versiune comprimată a [WMF](/ro/image/wmf/) și este folosit pentru a stoca metafișiere. Este un fișier de nivel intermediar generat de versiuni mai vechi ale aplicațiilor Microsoft Office și nu este foarte popular utilizat. Fișierele WMZ sunt generate în timpul salvării documentelor în format [HTML](/ro/web/html/). Acestea pot fi, de asemenea, generate în timp ce se trimit documente prin e-mail care conțin clip art-uri încorporate, ecuații etc. Aplicațiile care pot deschide fișiere WMZ includ (dar fără a se limita la) Corel Winzip și Apple Archive Utility.

## Format de fișier WMZ

Fișierele WMZ sunt [Gzip](/ro/compression/gz/) comprimate și conțin [WMF](/ro/image/wmf/) în interior. Gzip folosește algoritmul DEFLATE pentru comprimarea arhivei. GZIP este diferit de formatul de arhivă [ZIP](/ro/compression/zip/), deoarece aplică algoritmul de compresie pentru arhiva completă, mai degrabă decât fișierele individuale. Formatul de fișier este format din:

* Antet fișier
* Anteturi opționale
* Date comprimate
* Subsol fișier

Formatul de fișier GZIP [specificații versiunea 4.3](https://datatracker.ietf.org/doc/html/rfc1952) publicat de Internet Engineering Task Force (IETF) conține informații detaliate despre formatul fișierului.

## Referințe

* [RFC1952: specificația formatului fișierului GZIP](https://datatracker.ietf.org/doc/html/rfc1952), de [IETF](https://www.ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

