{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier VHDX și despre API-urile care pot crea și deschide fișiere VHDX.",
  "title" :"Format de fișier VHDX - Ce este un fișier VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Ce este un fișier VHDX?

Un fișier VHDX este un fișier imagine de disc în formatul de fișier Virtual Hard Disk v2. Conține un întreg sistem de operare care poate fi încărcat și utilizat ca orice mașină normală pentru testarea software-ului sau rularea software-ului care necesită un anumit sistem de operare. Un VHDX, în ciuda faptului că este o imagine de disc completă, este stocat într-un singur fișier. Software-ul pentru mașină virtuală, cum ar fi Parallels Desktop, Windows Virtual Machine și Virtual Box, pot încărca și deschide imaginea de disc.

Fișierul VHDX poate fi convertit în [VHD](/ro/disc-and-media/vhd/) cu Hyper-V Manager sau în [VDI](/ro/disc-and-media/vdi/) cu VirtualBox.

## Format de fișier VHDX - Mai multe informații

Detaliile formatului de fișier VHDX sunt complet documentate și disponibile online ca [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) pe documentația Microsoft. Este o extensie a formatului VHD și include capabilități îmbunătățite. Formatul de fișier VHDX oferă caracteristici suplimentare care sunt disponibile la straturile de fișiere de hard disk virtual și de hard disk virtual. Este mai optimizat și oferă rezultate mai bune pentru configurația și capabilitățile hardware de stocare. Fișierele VHDX pot fi deschise

### Suport pentru hard disk-uri virtuale în VHDX

Acceptă trei tipuri de hard disk virtuale.

1. **Fixed Virtual Hard Disk** - Hard disk virtual cu dimensiune fixă a datelor alocată. Dimensiunea hard disk-ului virtual nu se modifică odată cu adăugarea sau eliminarea datelor.

1. **Dynamic Virtual Hard Disk** - Hard disk virtual cu dimensiunea dinamică a discului. Dimensiunea este în orice moment la fel de mare ca datele reale scrise pe el și metadatele. Dimensiunea fișierului său crește dinamic pe măsură ce datele sunt adăugate sau eliminate din acesta.

1. **Diferencing Virtual Hard Disk** - Reprezintă curentul hard diskului virtual ca un set de blocuri modificate în comparație cu un fișier de hard disk virtual părinte.

## Referințe

* [Specificații de format de fișier VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - de la Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

