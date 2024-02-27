{
  "date": "2019-10-11",
  "keywords": [
"xpm fil",
"xpm filformat",
"hvad er en xpm-fil",
"fil",
"xpm eksempel",
"xpm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM - X PixMap filformat",
  "description": "Lær om XPM-filformat og API'er, der kan oprette og åbne XPM-filer.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-dam"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en XPM fil?

En fil med filtypen .xpm er et billedfilformat, der blev brugt af X Windows-systemet. Det understøtter gennemsigtige pixels og er normalt rettet mod at skabe ikon-pixmaps. Det understøtter monokrome, gra-skala og farve pixmap-data. Disse er designet til at kunne redigeres i hånden og kan inkluderes i [C](/programming/c/)-koden. Til dette formål er XPM-filer i almindeligt tekstfilformat og følger C-programmeringssprogets syntaks. XPM-filer kan åbnes med en række forskellige billedvisningsprogrammer som f.eks
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView og Canvas X.

## XPM filformat

XPM-filformatet bruger C-syntaks, for at disse kan integreres i C- og C++-programmer. Den består af følgende seks forskellige sektioner.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

Sektionerne er faktisk en række strenge som følger.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Følgende er detaljerne i hvert afsnit.

`<Values> ` - Denne sektion er en streng, der indeholder fire eller seks heltal, der er i basis 10 og svarer til:

 * pixmap bredde og højde
 * antal farver
 * antal tegn pr. pixel
 * valgfri hotspot-koordinater og XPMEXT-tag

`<Colors> ` - Denne sektion indeholder lige så mange strenge, som der er farver. Hver streng er som følger:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Denne sektion er sammensat af<height> strenge og<width> \*<chars_per_pixel> tegn. Hver<chars_per_pixel> længdestrengen skal være en af de tidligere definerede grupper i<Colors> afsnit.

`<Extension> ` - Udvidelsessektionen skal mærkes, hvis den ikke er tom, i<Values> afsnit. Det kan bestå af flere<Extension> underafsnit, der kan være af følgende to typer:

 * en enkeltstående streng sammensat som følger: XPMEXT<extension-name><extension-data>
 * eller en blok sammensat af flere strenge:XPMEXT<extension-name><related extension-data composed of several strings>

## Referencer

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)

* [XPM-manual](http://www.xfree86.org/current/xpm.pdf)


