{
  "date" : "2021-08-13",
  "keywords" :[ "fișier sdi", "format fișier sdi", "ce este un fișier sdi", "fișier", "exemplu sdi", "extensie fișier sdi", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier SDI și despre API-urile care pot crea și deschide fișiere SDI.",
  "title" :"SDI - Fișier imagine de implementare a sistemului Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Ce este un fișier SDI?
Fișierul cu extensia .sdi conține un blob de încărcare, un blob de pornire și un blob parțial; folosit în mod obișnuit de Windows Embedded Studio pentru a crea discuri RAM sau discuri de boot pentru încărcarea și instalarea Windows. SDI este abreviat pentru System Deployment Image. Windows Embedded Studio este un program folosit pentru a crea imagini de disc pentru Windows. De fapt, acest program conține programul SDI File Manager și un instrument de linie de comandă numit **sdimgr.exe**, ambele putând fi folosite pentru a extinde, crea și edita imagini SDI.

## Format de fișier SDI
Formatul de fișier SDI este utilizat pe scară largă pentru a permite utilizarea unui disc virtual pentru pornirea unui sistem. Unele versiuni de Microsoft Windows permit **pornirea RAM**, ceea ce este important pentru a încărca un fișier SDI în memorie și apoi a porni din acesta. Formatul de fișier SDI se activează și pentru pornirea în rețea folosind PXE (Preboot Execution Environment). Este, de asemenea, folosit pentru imagini de hard disk.
### Secțiuni ale fișierului SDI
Fișierul SDI în sine poate fi subdivizat în următoarele secțiuni:
- **Boot BLOB**: Acesta conține programul de pornire real, STARTROM.COM. Acesta este un sector analog cu sectorul de boot al unui hard disk.
- **Load BLOB**: Acesta conține de obicei NTLDR și este lansat de boot-ul BLOB.
- **Partea BLOB**: Acesta conține timpul de pornire real; include, de asemenea, fișierele boot.ini și ntdetect.com care ar trebui să fie localizate în directorul rădăcină al runtime-ului.
- **Disk BLOB**: Aceasta este o imagine HDD plată care începe cu un MBR. Este folosit pentru imagini de hard disk în loc de pornire. De asemenea, numai Disk BLOB pot fi montate cu utilitarele Microsoft.


## Referințe

* [Imagine de implementare a sistemului - de Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


