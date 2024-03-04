{
  "date": "2021-08-13",
  "keywords": [
"sdi failą",
"sdi failo formatas",
"kas yra sdi failas",
"failą",
"sdi pavyzdys",
"sdi failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie SDI failo formatą ir API, kurios gali kurti ir atidaryti SDI failus.",
  "title": "SDI – „Windows“ sistemos diegimo vaizdo failas",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-lti"
}
},
  "lastmod": "2021-08-13"
}

## Kas yra SDI failas?
Faile su plėtiniu .sdi yra įkrovos blob, įkrovos blob ir dalis blob; dažniausiai naudojamas Windows Embedded Studio, kad sukurtų RAM arba įkrovos diskus, skirtus Windows įkelti ir įdiegti. SDI sutrumpintai reiškia sistemos diegimo vaizdą. Windows Embedded Studio yra programa, naudojama Windows disko vaizdams kurti. Tiesą sakant, šioje programoje yra SDI failų tvarkyklės programa ir komandų eilutės įrankis, vadinamas **sdimgr.exe**, abu gali būti naudojami SDI vaizdams pateikti, kurti ir redaguoti.

## SDI failo formatas
SDI failo formatas plačiai naudojamas norint įjungti virtualų diską sistemai paleisti. Kai kurios Microsoft Windows versijos įgalina **RAM paleidimą**, o tai svarbu įkelti SDI failą į atmintį ir paleisti iš jo. SDI failo formatas taip pat leidžia paleisti tinklą naudojant PXE (Preboot Execution Environment). Jis taip pat naudojamas kietojo disko vaizdavimui.
### SDI failo skyriai
Pats SDI failas gali būti suskirstytas į šiuos skyrius:
- **Boot BLOB**: čia yra tikroji įkrovos programa STARTROM.COM. Tai yra analogiškas standžiojo disko įkrovos sektoriui.
- **Įkelti BLOB**: paprastai jame yra NTLDR ir jį paleidžia įkrovos BLOB.
- **Part BLOB**: čia pateikiamas faktinis įkrovos vykdymo laikas; taip pat apima boot.ini ir ntdetect.com failus, kurie turėtų būti pagrindiniame vykdymo laiko kataloge.
- **Disk BLOB**: tai plokščias HDD vaizdas, prasidedantis MBR. Jis naudojamas kietojo disko vaizdavimui, o ne paleidimui. Taip pat tik Disk BLOB galima montuoti naudojant Microsoft paslaugų programas.


## Nuorodos 

* [Sistemos diegimo vaizdas – Vikipedija](https://en.wikipedia.org/wiki/System_Deployment_Image)



