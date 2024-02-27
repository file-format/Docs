{
  "date": "2021-08-10",
  "keywords": [
".ovf-fil",
"filformat",
"hvad er en .ovf-fil",
"fil",
"filtypenavn"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om, hvad et .ovf-filformat og API'er er, der kan oprette og åbne OVF-filer.",
  "title": "OVF-filformat - Åbn virtualiseringsfil",
  "linktitle": "OVF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-daf"
}
},
  "lastmod": "2022-01-03"
}

## Hvad er OVF fil?

En OVF-fil er en tekstfil, der indeholder information om pakning og distribution af en software, der kører på en virtuel maskine. Den er formateret i henhold til [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf), der beskriver alle kravene (såsom sikkerhed, portabilitet, effektivitet og udvidelsesmuligheder) for at køre applikationer på virtuelle maskiner. Den Internationale Standardiseringsorganisation (ISO) har vedtaget OVF som ISO 17203-standard.

## Kort historie om OVF-filformat

OVF-filformatet blev introduceret af DMTF (Distributed Management Task Force), der skaber åbne håndteringsstandarder. Den er uafhængig af en bestemt hypervisor- eller instruktionssætarkitektur. OVF-pakken indeholder et eller flere virtuelle systemer, som hver især kan implementeres på en virtuel maskine.

## OVF-filformat - flere oplysninger

En OVF-pakke består af flere filer placeret i en enkelt mappe. Blandt disse indeholder den nøjagtig én OVF-deskriptor-fil (med endelsen .ovf), der er gemt i filformatet [XML](/web/xml/). Den beskriver den pakkede virtuelle maskine-information og metadatainformation om OVF-pakken, såsom:

 * navn
 * hardwarekrav
 * referencer til de andre filer i OVF-pakken, og
 * human-readable descriptions

Andre filer, der kan findes i en OVF-pakke, inkluderer et eller flere diskbilleder og eventuelt certifikatfiler og andre hjælpefiler.

## Referencer

* [Åbent virtualiseringsformat - DMTF](https://www.dmtf.org/standards/ovf)

* [OVF-filformatspecifikationer](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)


