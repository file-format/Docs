{
  "date": "2021-02-25",
  "keywords": [
"bdf failą",
"bdf failo formatas",
"kas yra bdf failas",
"failą",
"bdf pavyzdys",
"bdf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "BDF – Glyph Bitmap platinimo formatas",
  "description": "Sužinokite apie BDF failo formatą ir API, kurios gali kurti ir atidaryti BDF failus.",
  "linktitle": "BDF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-bd-ltf"
}
},
  "lastmod": "2021-02-25"
}

## Kas yra BDF failas?
BDF failai yra žmonėms suprantama forma ir paprastai platinami ASCII koduotėje. Failas prasideda visuotine informacija, susijusia su visu šriftu, o po to pateikiama informacija ir atskirų glifų bitų žemėlapiai. Jame esantys duomenys rodomi vieno dydžio orientacijos šriftui. Metrika, kurią reikia naudoti daugiau nei viena kryptimi, gali būti įtraukta į vieną failą. BDF faile kiekvienas elementas yra atskiroje failo teksto eilutėje. Tarpai naudojami elementams atskirti eilutėje.

## BDF failo formatas
BDF šortai, skirti Glyph Bitmap platinimo formatui; Adobe priklauso failo formatas, skirtas bitmap tipo šriftams išsaugoti. Turinys pateikiamas kaip tekstinis failas, skirtas skaityti kompiuteriu ir žmogui. BDF ypač naudojamas Unix X Window aplinkoje. Jis buvo plačiai pakeistas PCF šrifto formatu, kuris turėtų būti efektyvesnis, ir OpenType bei TrueType šriftais.
### BDF failo struktūra
BDF šrifto failą sudaro trys skyriai:

- visuotinė sekcija, taikoma visiems šrifto glifams.
- skyrius su atskiru įrašu kiekvienam glifui.
- ENDFONT pareiškimas.

## Pavyzdys
Čia yra šrifto pavyzdys, kuriame yra vienas ASCII didžiosios raidės A glifas. Jos visuotinės deklaracijos prasideda STARTFONT eilute ir baigiasi CHARS eilute
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Nuorodos
 * [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
 * [Glyph Bitmap Distribution Format (BDF) specifikacija](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

