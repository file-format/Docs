{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier VPK - Format de fișier al pachetului de aplicații PlayStation Vita",
  "description":"Aflați despre formatul de fișier VPK și despre API-urile care pot crea și deschide fișiere VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Ce este un fișier VPK?

Un fișier cu extensia .vpk este un fișier de pachet de arhivă comprimat care este utilizat pentru a instala aplicații terță parte pe consola de jocuri Sony PlayStation Vita. Aceste fișiere pot fi instalate numai pe jailbreak Vita PlayStation de HENkaku, care a permis PS Vita și PSTV să utilizeze conținut personalizat creat de utilizator. Un fișier de arhivă VPK conține tot conținutul care alcătuiește jocul, inclusiv imagini precum fișierele [PNG](/ro/image/png/), fișierele de setare precum [.bin](/ro/disc-and-media/bin/) și orice configurații în format de fișier [XML](/ro/web/xml/).

## Format de fișier VPK

Fișierele VPK sunt salvate pe disc ca arhive standard comprimate [ZIP](/ro/compression/zip/). Acestea pot conține mai multe foldere și alte fișiere asociate pentru aplicațiile terță parte care urmează să fie instalate pe Vita Gaming Console. Pentru a vizualiza conținutul fișierului pachet VPK, redenumiți extensia acestuia din .vpu în .zip și extrageți conținutul utilizând utilitare standard de decompresie, cum ar fi WinZip sau WinRAR.

Valvesoftware are informații detaliate despre [formatul fișierului VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) care pot fi referite din perspectiva dezvoltatorului.

## Cum se instalează fișierele VPK?

Fișierele VPK pot fi instalate din utilitarul de linie de comandă VPK.exe. Pe sistemul de operare Windows, fișierele pot fi aruncate în fișierul vpk.exe, care returnează un \*.vpk care conține toate fișierele împachetate. Alternativ, instrumentul de linie de comandă poate fi utilizat după cum urmează.

### Creați VPK și adăugați fișiere

```
vpk <dirname>
```

### Extrageți fișierele VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referințe

* [Format de fișier VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Fișiere VPK](https://developer.valvesoftware.com/wiki/VPK)

