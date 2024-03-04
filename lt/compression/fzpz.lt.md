{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FZPZ failo formatas – fritzing dalies failas",
  "description": "Sužinokite, kas yra FZPZ failas ir API, kurios gali kurti ir atidaryti FZPZ failus.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-ltz"
}
},
  "lastmod": "2022-06-20"
}

## Kas yra FZPZ failas?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ failo formatas – daugiau informacijos

FZPZ failai išsaugomi diske kaip suspausti [ZIP](/compression/zip/) archyvai. Galite pervardyti plėtinį iš .fzpz į .zip ir naudoti bet kurią standartinę išskleidimo priemonę, pvz., WinZIP, kad išskleistumėte failus iš archyvo.

### FZPZ failo struktūros informacija

Kaip minėta, FZPZ failas yra archyvo failas, kuriame yra daug failų, skirtų spausdintinėje plokštėje naudojamai daliai pavaizduoti. FZPZ yra šie failai:

 * Keturi SVG failai – atspindi dalies duonos lentą, schemą, PCB ir piktogramų vaizdus
 * FZP failas – XML failas, kuriame yra informacijos apie dalies savybes, jungtis ir magistrales.

Failai paprastai vadinami taip.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## Nuorodos Nr.

* [Naujos dalys su fzpz plėtiniu](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


