{
  "date" : "2019-10-11",
  "keywords" :[ "fișier emz", "format fișier emz", "ce este un fișier emz", "fișier", "exemplu emz", "extensie fișier emz", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier EMZ - Un meta fișier îmbunătățit comprimat Windows",
  "description":"Aflați despre formatul de fișier EMZ și despre API-urile care pot crea și deschide fișiere EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Ce este un fișier EMZ?

Un fișier cu extensia .emz este un container comprimat de metafile îmbunătățit (fișier [EMF](/ro/image/emf/)). Acestea sunt comprimate folosind tehnica de compresie [GZIP](/ro/compression/gz/), care este metoda de compresie folosită în mod obișnuit pe sistemele de operare UNIX și LINUX. Deconectați ZIP (/ro/compression/zip/), GZIP comprimă arhiva ca întreg în loc să comprima fișierele individuale. Fișierele EMZ au dimensiuni mai mici în comparație cu fișierele EMF și ajută la transferul rapid în timpul partajării online a fișierelor. Unele dintre aplicațiile care pot deschide fișiere EMZ includ Microsoft Visio 2019, Microsoft Office 2019, XnView MP și File Viewer Plus.

## Format de fișier EMZ

Fișierele EMZ sunt [Gzip](/ro/compression/gz/) comprimate și conțin [EMF](/ro/image/emf/) în interior. Gzip folosește algoritmul DEFLATE pentru comprimarea arhivei și este diferit în aplicarea compresiei. Un fișier EMZ poate fi decomprimat utilizând utilitare de compresie GZip, cum ar fi GNU Zip. Formatul de fișier este format din:

* Antet fișier
* Anteturi opționale
* Date comprimate
* Subsol fișier

Formatul de fișier GZIP [specificații versiunea 4.3](https://datatracker.ietf.org/doc/html/rfc1952) publicat de Internet Engineering Task Force (IETF) conține informații detaliate despre formatul fișierului.

## Referințe

* [RFC1952: specificația formatului fișierului GZIP](https://datatracker.ietf.org/doc/html/rfc1952), de [IETF](https://www.ietf.org/)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

