{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om VHDX-filformat och API:er som kan skapa och öppna VHDX-filer.",
  "title" :"VHDX-filformat - Vad är en VHDX-fil?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Vad är en VHDX fil?

En VHDX-fil är en diskbildsfil i filformatet Virtual Hard Disk v2. Den innehåller ett helt operativsystem som kan laddas och användas som vilken vanlig maskin som helst för att testa programvara eller köra programvara som kräver ett specifikt operativsystem. En VHDX, trots att den är en fullständig skivavbild, lagras i en enda fil. Virtuell maskinprogramvara som Parallels Desktop, Windows Virtual Machine och Virtual Box kan ladda och öppna diskavbildningen.

VHDX-fil kan konverteras till [VHD](/sv/disc-and-media/vhd/) med Hyper-V Manager, eller till [VDI](/sv/disc-and-media/vdi/) med VirtualBox.

## VHDX-filformat - Mer information

Detaljerna för VHDX-filformatet är fullständigt dokumenterade och tillgängliga online som [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) på Microsoft Documentation. Det är en förlängning av VHD-formatet och inkluderar förbättrade möjligheter. VHDX-filformatet tillhandahåller ytterligare funktioner som är tillgängliga på den virtuella hårddisken och fillagren på den virtuella hårddisken. Den är mer optimerad och ger bättre resultat för konfiguration och funktioner för lagringshårdvara. VHDX-filer kan öppnas

### Stöd för virtuella hårddiskar i VHDX

Den stöder tre typer av virtuella hårddiskar.

1. **Fast virtuell hårddisk** - Virtuell hårddisk med fast datastorlek allokerad. Storleken på den virtuella hårddisken ändras inte med tillägg eller borttagning av data.

1. **Dynamisk virtuell hårddisk** - Virtuell hårddisk med dynamisk skivstorlek. Dens storlek är när som helst lika stor som den faktiska data som skrivits till den och metadata. Dess filstorlek ökar dynamiskt när data läggs till eller tas bort från den.

1. **Skillnad mellan virtuell hårddisk** - Representerar strömmen för den virtuella hårddisken som en uppsättning modifierade block i jämförelse med en överordnad virtuell hårddiskfil.

## Referenser

* [VHDX filformatspecifikationer](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - av Wikipedia](https://en.wikipedia.org/wiki/VHD_(filformat))

