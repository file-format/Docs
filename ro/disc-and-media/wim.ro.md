{
  "date" : "2021-08-11",
  "keywords" :[ "fișier wim", "format fișier wim", "ce este un fișier wim", "fișier", "exemplu wim", "extensie fișier wim", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier WIM și despre API-urile care pot crea și deschide fișiere WIM.",
  "title" :"WIM - Fișier cu format de imagine Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Ce este un fișier WIM?
Fișierele cu extensii .wim au fost văzute pentru prima dată în Windows Vista. WIM aparține unui format de imagine bazat pe fișiere care a fost introdus de obicei în Microsoft Windows Vista. Permite implementarea unei singure imagini de disc pe diferite platforme de computer. Fișierele WIM sunt utilizate pentru a gestiona fișiere precum actualizări, drivere și componente fără a reporni imaginea sistemului de operare. Fișierul AQ WIM conține un set de fișiere și metadate asociate care sunt foarte similare cu alte formate de fișiere de disc.

## Formate de fișiere WIM
Formatul de fișier WIM nu este ca formatele bazate pe sector, cum ar fi VHD sau IS, de fapt, este un fișier bazat, ceea ce înseamnă că unitatea fundamentală de informații dintr-un WIM este un fișier. Beneficiul de bază de a fi bazat pe fișiere este că stocarea într-o singură instanță a unui fișier la care se face referire de mai multe ori în arborele sistemului de fișiere și independența hardware. Reduce costul general de deschidere și închidere a diferitelor fișiere individual, deoarece fișierele sunt stocate într-un singur WIM. fişier. Fișierele WIM pot stoca mai multe imagini de disc, la care se face referire fie prin numele lor unic, fie prin indexul lor numeric.
### Suport pentru algoritmi de compresie
WIM acceptă următoarele familii de algoritmi de compresie în viteză descendentă și raport ascendent:
- XPRESS
- LZX
- LZMS
- Compresie solidă.
Primele trei familii sunt bazate pe LZ77, în timp ce Solid-compression a fost introdusă împreună cu LZMS în WIMGAPI Windows 8 și DISM Windows 8.1.
### Instrumente pentru formatul de fișier WIM
Următoarele instrumente sunt de obicei compatibile cu formatul de fișier WIM:

- **ImageX**: un instrument de linie de comandă folosit pentru a edita, crea și implementa imagini de disc Windows în formatul de imagine Windows. Împreună cu WIMGAPI relevant, este distribuit ca parte a setului gratuit de instalare automată Windows. Începând cu Windows Vista, Windows Setup utilizează WAIK API pentru a instala Windows.
- **DISM**: un instrument introdus în Windows 7 și Windows Server 2008 R2 care poate efectua sarcini legate de service pe o imagine de instalare Windows, fie că este o imagine online sau o imagine offline dintr-un folder sau fișier WIM. acest instrument a fost capabil să monteze și să demonteze imagini, să adauge un driver de dispozitiv la o imagine offline și să interogheze driverele de dispozitiv instalate într-o imagine offline.
 




## Referințe


* [Format Windows Imaging - de Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


