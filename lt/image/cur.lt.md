{
  "date": "2021-06-29",
  "keywords": [
"CUR",
"pratęsimas",
"failą",
"formatu",
"vaizdas",
"Nuo įrenginio nepriklausomas taškinis žemėlapis",
"Kursoriaus failo formatas",
"Žymeklis",
"Windows",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CUR – žymeklio failo formatas",
  "description": "Sužinokite apie CUR failo formatą ir API, kurios gali kurti ir atidaryti CUR failus.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cu-ltr"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra CUR failas? ##

CUR failas yra statinis Microsoft Windows žymeklio failo formatas. Iš esmės tai yra stacionarūs vaizdai, visais atžvilgiais identiški ICO (piktogramų) failams, išskyrus plėtinį. Tiek CUR, tiek [ICO](/image/ico/) yra sukurti remiantis nuo įrenginio nepriklausomos bitmap [DIB](/image/dib/) (nuo įrenginio nepriklausomos bitmap) specifikacijos. Numatytasis, taip pat pasirinktinis žymeklis, pvz., Windows pelės žymeklis, skirtas Windows operacinei sistemai, yra saugomi CUR failuose. Tai gali būti rodyklė įprastam naudojimui, besisukantis smėlio laikrodis, rodantis laukimo laikotarpius, arba I juosta, skirta teksto redagavimui. CUR failai pateikiami kartu su pasirinktinių darbalaukio temų diegimo paketu, siekiant užtikrinti, kad Windows žymeklis atitiktų pasirinktinę darbalaukio temą.

## Techninė specifikacija Nr.

CUR failai yra dvejetainiai sistemos failai, kuriuos galima rasti įrenginiuose, kuriuose veikia Microsoft Windows operacinė sistema. CUR rodyklės vaizdai yra skirtingų standartinių dydžių, pvz., 16 × 16, 32 × 32 ir tt CUR failai yra labai panašūs į ICO failus; abu jie susideda iš mažų stacionarių vaizdų. Skiriasi tik CUR ir ICO failų plėtiniai. Be to, viešosios interneto prieigos taško paaiškinimas CUR failo antraštėje skiriasi nuo ICO failo. Viešosios interneto prieigos taškas interpretuoja pikselių poslinkį nuo viršutinio kairiojo kampo iki vietos, kur nukreipiate pelę. Windows sistemos vis dar naudoja CUR failus, tačiau dabar animuoti žymekliai paprastai turi failo plėtinį ANI, o ne CUR.

## Trumpa istorija ##

CUR failas yra pagamintas iš ICO failo. Pirmasis CUR failo formatas buvo įtrauktas į Microsoft Windows 1.0 operacinę sistemą 1981 m., siekiant palengvinti komercinį naudojimą. Netrukus buvo pristatyti daugiau interaktyvių žymeklių, leidžiančių vartotojams keisti savo žymeklio nuostatas iš iš anksto įdiegtų parinkčių. Tačiau paprasta redaguoti CUR failą, net jei neturite pakankamai techninių žinių.


## CUR pavyzdys Nr.

CUR failus galite rasti adresu *C:\Windows\Cursors*:

{{< figure src="../cur.png" alt="CUR failo formatas" >}}

