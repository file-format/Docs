{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier WHL - Fișier pachet Python Wheel",
  "description":"Aflați despre formatul de fișier WHL și despre API-urile care pot crea și deschide fișiere WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Ce este un fișier WHL?

Un fișier WHL (Wheel) este un fișier de pachet de distribuție salvat în formatul roată Python. Este o instalare în format standard a distribuțiilor Python și conține toate fișierele și metadatele necesare pentru instalare. Fișierul WHL conține, de asemenea, informații despre versiunile și platformele Python acceptate de acest fișier roată. Similar cu un fișier de configurare [MSI](/ro/executable/msi/), formatul de fișier WHL este un format gata de instalare care permite rularea pachetului de instalare fără a construi distribuția sursă.

## Format de fișier WHL

Formatul de fișier WHL este o arhivă [ZIP](/ro/compression/zip/) (.zip) care conține toate fișierele de instalare și metadatele cerute de instalatori pentru instalarea unui pachet. Aceste fișiere WHL pot fi extrase folosind opțiunea de dezarhivare sau aplicații software standard de decompresie, cum ar fi WinZIP și WinRAR.

### Convenția privind numele fișierelor WHL

Un fișier WHL este denumit conform următoarei convenții.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Un exemplu de nume de fișier WHL este următorul.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `criptografia` este numele pachetului.
* `2.9.2` este versiunea pachetului de criptografie. O versiune este un șir compatibil cu PEP 440, cum ar fi 2.9.2, 3.4 sau 3.9.0.a3.
* `cp35` este eticheta Python și denotă implementarea Python și versiunea pe care o cere roata.
* `abi3` este eticheta ABI. ABI înseamnă interfață binară a aplicației.
* `macosx_10_9_x86_64` este eticheta platformei, care se întâmplă să fie o gură plină.

## Referințe

* [Ce sunt roțile Python și de ce ar trebui să îți pese?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

