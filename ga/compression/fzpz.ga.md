{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid FZPZ - Comhad Cuid Fritzing",
  "description": "Foghlaim faoi cad is comhad FZPZ agus APIs ann ar féidir comhaid FZPZ a chruthú agus a oscailt.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-gaz"
}
},
  "lastmod": "2022-06-20"
}

## Cad is comhad FZPZ ann?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## Formáid Chomhaid FZPZ - Tuilleadh Eolais

Déantar comhaid FZPZ a shábháil ar diosca mar chartlanna chomhbhrúite [ZIP](/compression/zip/). Is féidir leat an síneadh a athainmniú ó .fzpz go .zip agus úsáid a bhaint as aon ghnáthfhóntas dí-chomhbhrú ar nós WinZIP chun na comhaid a bhaint as an gcartlann.

### Eolas faoin Struchtúr Comhad FZPZ

Mar a luadh, is comhad cartlainne é comhad FZPZ ina bhfuil comhaid iolraithe chun cuid a úsáidtear i gclár ciorcad priontáilte a léiriú. Tá na comhaid seo a leanas san FZPZ:

 * `Ceithre chomhad SVG` - a sheasann do chlár arán, scéimreach, íomhánna PCB agus deilbhíní
 * `Comhad FZP` - Comhad XML ina bhfuil faisnéis faoi airíonna, nascóirí agus busanna na coda

De ghnáth ainmnítear na comhaid mar seo a leanas.

 * páirt.comhad.fzp
 * svg.breadboard.comhad.svg
 * svg.icon.comhad.svg
 * svg.pbc.comhad.svg
 * svg.schematic.comhad.svg

## Tagairtí ##

* [Páirteanna nua le síneadh fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


