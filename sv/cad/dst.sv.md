{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "fil", "format", "tillägg", "API", "AutoCAD Sheet Set" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - AutoCAD Sheet Set File",
  "description" :"Läs mer om .dst-filer och API:er som kan skapa och öppna DST-filer.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Vad är en DST fil?

En DST-fil är en AutoCAD-fil som innehåller associationer och information för att definiera arkuppsättningar. Dessa lagras i standardmappen för arkuppsättningar, AutoCAD-arkuppsättningar. DST-filer innehåller inte de faktiska ritlayouterna men hänvisar till dessa från valda [DWG](/sv/cad/dwg/)- och [DWT](/sv/cad/dwt/)-filer som är associerade med dessa arkuppsättningar. I nätverksmiljö bör alla gruppmedlemmar ha nätverksåtkomst till dessa associerade filer. DST-filer sparas på skivan i filformatet [XML](/sv/web/xml/).

## DST-filformat - Mer information

DST-filer skapas med verktyget AutoDesk Sheet Set Manager (SSM). När en fil nås av någon i teamet, öppnas DST-filen kort och lagras sedan tillbaka med den uppdaterade informationen. Samtidig åtkomst till samma DST-fil hanteras av SSM-verktyget som visar en låsikon när filen är i åtkomst.

Vid en viss tidpunkt kan arkstatusen vara i något av följande tillstånd.

* Bladet är tillgängligt för redigering.
* Arket är låst.
* Arket saknas eller finns på en oväntad mappplats.

## Referenser

* [Om att använda DST Sheet Sets](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Läs mer om arkuppsättningar](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Mastering AutoCAD Sheet Sets](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

