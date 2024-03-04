{
  "date": "2021-04-22",
  "keywords": [
"appx failą",
"pratęsimas",
"formatu",
"kaip atidaryti appx failą",
"appx failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPX – kas yra APPX failas?",
  "description": "Sužinokite apie APPX failo formatą ir API, kurios gali kurti ir atidaryti APPX failus.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-ltx"
}
},
  "lastmod": "2021-12-16"
}

## Kas yra APPX failas?

APPX failas yra platinamas paketo failo formatas, naudojamas programai platinti ir įdiegti. Jis buvo pristatytas kartu su Windows 8, kad būtų paskelbtas Microsoft Windows Store. Jame yra visi failai, reikalingi norint įdiegti Windows programą. Tai apima metaduomenis, failus ir kredencialų informaciją. Modernesnis pakuotės failo formatas yra MSIX, kuris šiuo metu yra dažniau naudojamas, palyginti su APPX.

## APPX failo formatas – daugiau informacijos

APPX failai išsaugomi kaip suspausti failai [ZIP](/compression/zip/) failo formatu. Dėl to visas paketas tampa mažesnio dydžio archyvo failu, kurį lengva įkelti į Microsoft Store.

## Kaip peržiūrėti failus APPX faile?

Norint peržiūrėti APPX failo turinį arba failus, reikia atlikti šiuos veiksmus.

 1. Kadangi APPX failai saugomi kaip suspausti ZIP failai, pervardykite failą į .zip plėtinį
 1. Norėdami išskleisti failus, esančius APPX faile, naudokite bet kokį išskleidimo įrankį, pvz., 7-Zip, WinZip arba WinRAR.

## Kaip sukurti APPX failą?

Yra du būdai, kuriuos galima naudoti kuriant APPX failus.

 1. Naudojant MakeApp.exe – [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) naudojamas programų paketams (.msix arba .appx) ir programų paketų rinkinio failams .msixbundle arba .appxbundle kurti. Be to, jis gali išgauti failus iš programos paketo. MakeApp.exe galima su Windows 10 SDK ir gali būti naudojama komandų eilutėje.
 1. Microsoft Visual Studio naudojimas – kūrėjai paprastai [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) naudoja Microsoft Visual Studio. Kai programos kūrimas bus baigtas ir programa bus paruošta publikuoti, APPX paketo failą galima sukurti paskelbus jį Visual Studio.

## Nuorodos

 * [Sukurkite MSIX paketą arba rinkinį naudodami MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Sukurkite APPX failus naudodami Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

