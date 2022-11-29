{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf-fil", "filformat", "vad är en .ovf-fil", "fil", "filtillägg"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om vad som är ett .ovf-filformat och API:er som kan skapa och öppna OVF-filer.",
  "title" :"OVF-filformat - Öppna virtualiseringsfil",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Vad är OVF fil?

En OVF-fil är en textfil som innehåller information om paketering och distribution av en programvara som körs på en virtuell maskin. Den är formaterad enligt [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) som beskriver alla krav (som säkerhet, portabilitet, effektivitet och utökningsbarhet) för att köra applikationer på virtuella maskiner. International Organization for Standardization (ISO) har antagit OVF som ISO 17203-standard.

## Kort historia av OVF-filformat

OVF-filformat introducerades av DMTF (Distributed Management Task Force) som skapar öppna hanterbarhetsstandarder. Den är oberoende av någon speciell hypervisor- eller instruktionsuppsättningsarkitektur. OVF-paketet innehåller ett eller flera virtuella system, som vart och ett kan distribueras till en virtuell maskin.

## OVF-filformat - Mer information

Ett OVF-paket består av flera filer placerade i en enda katalog. Bland dessa innehåller den exakt en OVF-beskrivningsfil (med filändelsen .ovf) som lagras i filformatet [XML](/sv/web/xml/). Den beskriver den paketerade virtuella maskininformationen och metadatainformationen om OVF-paketet som:

* namn
* hårdvarukrav
* referenser till de andra filerna i OVF-paketet, och
* läsbara beskrivningar

Andra filer som kan hittas i ett OVF-paket inkluderar en eller flera diskbilder och eventuellt certifikatfiler och andra hjälpfiler.

## Referenser

* [Öppet virtualiseringsformat - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF-filformatspecifikationer](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

