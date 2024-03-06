{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FZPZ faila formāts - Fritzing Part File",
  "description": "Uzziniet, kas ir FZPZ fails un API, kas var izveidot un atvērt FZPZ failus.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-lvz"
}
},
  "lastmod": "2022-06-20"
}

## Kas ir FZPZ fails?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ faila formāts — vairāk informācijas

FZPZ faili tiek saglabāti diskā kā saspiesti [ZIP](/compression/zip/) arhīvi. Varat pārdēvēt paplašinājumu no .fzpz uz .zip un izmantot jebkuru standarta dekompresijas utilītu, piemēram, WinZIP, lai izvilktu failus no arhīva.

### FZPZ faila struktūras informācija

Kā minēts, FZPZ fails ir arhīva fails, kurā ir vairāki faili, kas attēlo iespiedshēmas platē izmantoto daļu. FZPZ satur šādus failus:

 * Četri SVG faili - kas attēlo daļas maizes paneli, shēmu, PCB un ikonu attēlus
 * FZP fails — XML fails, kas satur informāciju par daļas rekvizītiem, savienotājiem un kopnēm.

Faili parasti tiek nosaukti šādi.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## Atsauces Nr.

* [Jaunas daļas ar fzpz paplašinājumu](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


