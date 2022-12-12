{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier TS - Fișier flux de transport video",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Aflați despre ce este un fișier TS și API-urile care pot crea și deschide fișiere TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Ce este un fișier TS?

Un fișier cu extensia .ts este un flux video care stochează datele pe DVD-uri. Folosește algoritmul de compresie MPEG-2 ([.mpeg](/ro/video/mpg/)) pentru a obține eficiență și compatibilitate maximă între diferite tipuri de media, cum ar fi streaming și difuzare pe internet. Formatul de fișier TS a fost creat astfel încât să poată fi redat pe dispozitive cu conexiuni slabe la internet, cum ar fi smart TV.

## Format de fișier TS - Mai multe informații

Datele dintr-un fișier TS sunt similare cu fișierul [MP4](/ro/video/mp4/), dar sunt împărțite în bucăți mici. Fiecare bucată constă dintr-o bucată mică de videoclip, urmată de un pic de sunet și o legendă opțională. Un singur fișier TS este format din multe astfel de bucăți. Pe lângă video, audio și subtitrări, fiecare bucată include și câteva date suplimentare pentru detectarea erorilor în fragment. Din acest motiv, fișierele TS sunt ceva mai mari ca dimensiune.

### De ce să folosiți formatul de fișier TS?

Deci, dacă fișierele TS sunt oarecum mari ca dimensiune, ce avantaj oferă utilizarea lor în locul altor formate de fișiere? Ei bine, în difuzare, bucățile minuscule de video și audio pot fi trimise prin mijloacele de comunicare (prin cablu sau radio) în timp real. Datele suplimentare din bucăți sunt folosite de receptor pentru a omite bucățile predispuse la erori.

În plus, fișierele TS sunt folosite deoarece sistemul de difuzare nu are nevoie de întregul flux pentru a-l reda. Transmisia poate fi preluată și poate fi utilizată în timp real prin asamblarea audio și video.

## Cum să redați fișierele TS?

Ei bine, fișierele TS pot fi deschise și redate în popularul [VideoLAN VLC media player](https://www.videolan.org/vlc/features.html), care este disponibil gratuit pentru descărcare.

## Referințe ##

* [Flux de transport MPEG - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

