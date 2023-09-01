{
  "date" : "2021-08-10",
  "keywords" :[ ".ova-fil", "filformat", "vad är en .ova-fil", "fil", "filtillägg"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om vad som är ett .ova-filformat och API:er som kan skapa och öppna ova-filer.",
  "title" :"OVA-filformat - Öppna Virtual Appliance-fil",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Vad är OVA fil?

En OVA-fil (Open Virtual Appliance) är en OVF-katalog som sparas som ett arkiv med .tar-arkiveringsformatet. Det är en virtuell enhetspaketfil som innehåller filer för distribution av programvara som körs på en virtuell maskin. Ett OVA-paket innehåller en [.ovf](/sv/disc-and-media/ovf/) deskriptorfil, certifikatfiler, en valfri [.mf](/sv/programming/mf/) fil tillsammans med andra relaterade filer. OVA-filer har mediatyp som application/ovf.

## OVA filformat

Som nämnts är en OVA-fil en arkivfil som skapas med hjälp av OVF-katalogen i TAR-filformat. Själva filen sparas som en binär fil. De flesta virtualiseringsplattformar, som VMware, Microsoft, Oracle och Citrix, kan installera virtuella apparater från en OVF-fil som är en deskriptorfil med detaljerna om bilden som ska laddas i virtuell maskin.

## Fördelar med en OVA-fil

* OVA-filer är komprimerade, vilket möjliggör snabbare nedladdningar.
* vSphere Client validerar en OVA-fil innan den importeras och säkerställer att den är kompatibel med den avsedda destinationsservern. Om apparaten är inkompatibel med den valda värden kan den inte importeras och ett felmeddelande visas.
* OVA kan kapsla in flerskiktade applikationer och mer än en virtuell maskin.

## Referenser

* [OVA-filformat och mallar](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
* [OVF-filformatsspecifikationer](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

