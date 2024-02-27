{
  "date": "2021-08-10",
  "keywords": [
".ova-fil",
"filformat",
"hvad er en .ova-fil",
"fil",
"filtypenavn"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om, hvad et .ova-filformat og API'er er, der kan oprette og åbne ova-filer.",
  "title": "OVA-filformat - Åbn Virtual Appliance-fil",
  "linktitle": "OVA",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-daa"
}
},
  "lastmod": "2022-01-03"
}

## Hvad er en OVA fil?

En OVA-fil (Open Virtual Appliance) er en OVF-mappe, der er gemt som et arkiv ved hjælp af .tar-arkiveringsformatet. Det er en virtuel enhedspakkefil, der indeholder filer til distribution af software, der kører på en virtuel maskine. En OVA-pakke indeholder en [.ovf](/disc-and-media/ovf/)-deskriptorfil, certifikatfiler, en valgfri [.mf](/programming/mf/)-fil sammen med andre relaterede filer. OVA-filer har medietype som applikation/ovf.

## OVA filformat

Som nævnt er en OVA-fil en arkivfil, der er oprettet ved hjælp af OVF-mappen i TAR-filformat. Selve filen gemmes som en binær fil. De fleste virtualiseringsplatforme, såsom VMware, Microsoft, Oracle og Citrix, kan installere virtuelle apparater fra en OVF-fil, der er en deskriptorfil med detaljerne i billedet, der skal indlæses i den virtuelle maskine.

## Fordele ved en OVA-fil

* OVA-filer er komprimeret, hvilket giver mulighed for hurtigere downloads.

* vSphere Client validerer en OVA-fil, før den importeres, og sikrer, at den er kompatibel med den tilsigtede destinationsserver. Hvis apparatet er inkompatibelt med den valgte vært, kan det ikke importeres, og der vises en fejlmeddelelse.

* OVA kan indkapsle multi-tiered applikationer og mere end én virtuel maskine.


## Referencer

* [OVA File Formats and Templates](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
* [OVF File Format Specifications](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

