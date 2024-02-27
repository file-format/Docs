{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FZPZ-filformat - Fritzing-delfil",
  "description": "Lær om, hvad en FZPZ-fil og API'er er, der kan oprette og åbne FZPZ-filer.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-daz"
}
},
  "lastmod": "2022-06-20"
}

## Hvad er en FZPZ fil?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ-filformat - flere oplysninger

FZPZ-filer gemmes på disken som komprimerede [ZIP](/compression/zip/)-arkiver. Du kan omdøbe udvidelsen fra .fzpz til .zip og bruge et hvilket som helst standard dekomprimeringsværktøj såsom WinZIP til at udpakke filerne fra arkivet.

### FZPZ-filstrukturoplysninger

Som nævnt er en FZPZ-fil en arkivfil, der indeholder multiple filer til repræsentation af en del, der bruges i printkort. FZPZ indeholder følgende filer:

 * `Fire SVG-filer` - der repræsenterer delens brødtavle, diagram, PCB og ikonbilleder
 * `FZP-fil` - En XML-fil, der indeholder oplysninger om delens egenskaber, konnektorer og busser

Filerne er normalt navngivet som følger.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## Referencer ##

* [Nye dele med fzpz-udvidelse](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


