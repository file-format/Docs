{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "fișier", "extensie", "format", "ce este formatul fișierului mod", "muzică", "format fișier mod", "mod vs MP3", "specificație format fișier mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MOD și despre API-urile care pot crea, converti și deschide fișiere MOD.",
  "title" :"MOD - Fișier modul de muzică",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Ce este un fișier MOD?
Un fișier cu extensia .mod este un fișier de modul de muzică creat utilizând formatul standard de modul de muzică, care se bazează pe **formatul de modul Amiga** dezvoltat de Karsten Obarski și lansat cu software-ul **Ultimate Soundtracker** pentru Commodore. Sistemul Amiga. Similar cu un fișier [MIDI](/ro/audio/mid/), acesta constă din modele de note și mostre de sunet, reprezentând diferite instrumente care sunt redate în funcție de note. Fișierele MOD sunt utilizate în special în jocurile video ca muzică de fundal și în subcultura **demoscenă** computerizată.

## Format de fișier MOD

MOD este un format de fișier de calculator folosit ca funcția sa de bază este de a reprezenta muzica și a fost primul format de fișier modul. Fișierele MOD folosesc extensia de fișier .mod, cu excepția **Amiga** care citește antetul unui fișier pentru a determina tipul fișierului, deci nu se bazează pe extensiile de nume de fișier. Un fișier MOD constă dintr-un set de diferite instrumente sub formă de mostre, un număr de modele care specifică cum și când vor fi redate mostrele și o listă cu ce modele trebuie redate în ce ordine.

### Specificații pentru formatul fișierului MOD

Un model de fișier MOD este de fapt proiectat într-o interfață cu utilizatorul secvențatorului ca un tabel cu o coloană pe canal, deci acest tabel are patru coloane (una pentru fiecare canal hardware Amiga. Fiecare coloană are 64 de rânduri).

O celulă din tabel poate provoca una dintre următoarele acțiuni să aibă loc pe canalul coloanei sale atunci când este atins timpul rândului său:

- Porniți un instrument să cânte o notă nouă pe acest canal la un volum dat, eventual cu un efect special aplicat asupra acestuia
- Schimbați volumul sau efectul special aplicat notei curente
- Schimbarea fluxului de model; săriți la o anumită melodie sau o poziție de model sau bucla în interiorul unui model
- Nu face nimic; orice notă existentă redată pe acest canal va continua să fie redată

Un instrument este o singură probă împreună cu o specificație opțională a porțiunii de probă care poate fi repetată pentru a păstra o notă solidă.

### Timpul
Intervalul de timp minim a fost de 0,02 secunde în fișierul MOD original sau un interval de „eliminare verticală” (VSync), deoarece software-ul original folosea sincronizarea VSync a monitorului care rulează la 50 Hz (pentru PAL) sau 60 Hz (pentru NTSC) pentru sincronizare.

## Referințe

* [MOD (format fișier) - De Wikipedia](https://en.wikipedia.org/wiki/MOD_(format_fișier))

