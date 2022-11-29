{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK-fil - PlayStation Vita Application Package File Format",
  "description":"Läs mer om VPK-filformat och API:er som kan skapa och öppna VPK-filer.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Vad är VPK fil?

En fil med filtillägget .vpk är en komprimerad arkivpaketfil som används för att installera appar från tredje part på Sony PlayStation Vita-spelkonsolen. Dessa filer kan endast installeras på Jailbreak Vita PlayStation av HENkaku som gjorde det möjligt för PS Vita och PSTV att använda anpassat användarskapat innehåll. En VPK-arkivfil innehåller allt innehåll som utgör spelet inklusive bilder som [PNG](/sv/image/png/)-filer, inställningsfiler som [.bin](/sv/disc-and-media/bin/) och alla konfigurationer i filformatet [XML](/sv/web/xml/).

## VPK filformat

VPK-filer sparas på skiva som standardkomprimerade [ZIP](/sv/compression/zip/)-arkiv. Dessa kan innehålla flera mappar och andra associerade filer för tredjepartsappar som ska installeras på Vita Gaming Console. För att se innehållet i VPK-paketfilen byter du namn på filtillägget från .vpu till .zip och extraherar innehållet med hjälp av vanliga dekomprimeringsverktyg som WinZip eller WinRAR.

Valvesoftware har detaljerad information om [VPK-filformatet](https://developer.valvesoftware.com/wiki/VPK_File_Format) som kan refereras från utvecklarens perspektiv.

## Hur installerar man VPK-filer?

VPK-filerna kan installeras från kommandoradsverktyget VPK.exe. På Windows OS kan filer släppas på filen vpk.exe som returnerar en \*.vpk som innehåller alla paketerade filer. Alternativt kan kommandoradsverktyget användas enligt följande.

### Skapa VPK och lägg till filer

```
vpk <dirname>
```

### Extrahera VPK-filer

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referenser

* [VPK-filformat](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK-filer](https://developer.valvesoftware.com/wiki/VPK)

