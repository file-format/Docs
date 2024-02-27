{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VPK-fil - PlayStation Vita Application Package Filformat",
  "description": "Lær om VPK filformat og API'er, der kan oprette og åbne VPK filer.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-dak"
}
},
  "lastmod": "2022-03-01"
}

## Hvad er VPK fil?

En fil med filtypenavnet .vpk er en komprimeret arkivpakkefil, der bruges til at installere tredjepartsapps på Sony PlayStation Vita-spillekonsollen. Disse filer kan kun installeres på Jailbreak Vita PlayStation af HENkaku, der gjorde det muligt for PS Vita og PSTV at bruge tilpasset brugerskabt indhold. En VPK-arkivfil indeholder alt det indhold, der udgør spillet, inklusive billeder såsom [PNG](/image/png/)-filer, indstillingsfiler såsom [.bin](/disc-and-media/bin/) og eventuelle konfigurationer i filformatet [XML](/web/xml/).

## VPK filformat

VPK-filer gemmes på disken som standard komprimerede [ZIP](/compression/zip/)-arkiver. Disse kan indeholde flere mapper og andre tilknyttede filer til tredjepartsapps, der skal installeres på Vita Gaming Console. For at se indholdet af VPK-pakkefilen skal du omdøbe dens udvidelse fra .vpu til .zip og udpakke indholdet ved hjælp af standard dekomprimeringsværktøjer såsom WinZip eller WinRAR.

Valvesoftware har detaljerede oplysninger om [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format), der kan henvises til fra udviklerens perspektiv.

## Sådan installeres VPK filer?

VPK-filerne kan installeres fra kommandolinjeværktøjet VPK.exe. På Windows OS kan filer slippes på vpk.exe-filen, som returnerer en \*.vpk, der indeholder alle de pakkede filer. Alternativt kan kommandolinjeværktøjet bruges som følger.

### Opret VPK og tilføj filer

```
vpk <dirname>
```

### Udpak VPK-filer

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referencer

* [VPK-filformat](https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [VPK-filer](https://developer.valvesoftware.com/wiki/VPK)


