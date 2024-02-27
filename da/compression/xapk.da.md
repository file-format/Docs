{
  "date": "2021-04-11",
  "keywords": [
"xapk fil",
"xapk filformat",
"hvad er en xapk-fil",
"fil",
"xapk eksempel",
"xapk filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XAPK - Meta Package File Format",
  "description": "Lær om XAPK-filformat og API'er, der kan oprette og åbne XAPK-filer.",
  "linktitle": "XAPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-xap-dak"
}
},
  "lastmod": "2021-04-11"
}

## Hvad er en XAPK fil?

En fil med filtypenavnet .xapk er en komprimeret pakkefil, der bruges til at installere Android-apps på mobile enheder. Det er et containerfilformat, der inkorporerer APK og yderligere tilknyttede filer, der kræves til installationen. Den anden tilknyttede fil er en OBB-fil, der gemmer yderligere filer såsom grafik, mediefiler og appdata, der er nødvendige for at holde applikationen kørende. XAPK-filer understøttes ikke af Google Play og bruges kun til distribution på tredjepartswebsteder for download af Android-apps. Disse kan installeres på en Android-enhed ved hjælp af XAPK Installer.

## XAPK filformat

XAPK-filer komprimeres ved at bruge standardfilformatet [ZIP](/compression/zip/). Disse kan udtrækkes ved hjælp af en standard komprimerings-/dekompressionssoftware såsom WinZIP. Når XAPK-filen er pakket ud til disken, indeholder den følgende filer i mappen.

 * APK - Standardinstallationsfil til installation af applikationen på Android-enheder
 * OBB - Yderligere fil, der indeholder relevante ressourcefiler

## Referencer

* [Android-pakkefil](https://en.wikipedia.org/wiki/Android_application_package)


