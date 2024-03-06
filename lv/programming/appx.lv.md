{
  "date": "2021-04-22",
  "keywords": [
"appx fails",
"pagarinājumu",
"formātā",
"kā atvērt appx failu",
"appx faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPX — kas ir APPX fails?",
  "description": "Uzziniet par APPX failu formātu un API, kas var izveidot un atvērt APPX failus.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-lvx"
}
},
  "lastmod": "2021-12-16"
}

## Kas ir APPX fails?

APPX fails ir izplatāms pakotnes faila formāts, ko izmanto lietojumprogrammas izplatīšanai un instalēšanai. Tas tika ieviests ar Windows 8, lai to publicētu Microsoft Windows veikalā. Tajā ir visi faili, kas nepieciešami Windows lietojumprogrammas instalēšanai. Tie ietver metadatus, failus un informāciju par akreditācijas datiem. Mūsdienīgāks iepakojuma faila formāts ir MSIX, kas pašlaik tiek izmantots biežāk nekā APPX.

## APPX faila formāts — vairāk informācijas

APPX faili tiek saglabāti kā saspiesti faili [ZIP](/compression/zip/) faila formātā. Tādējādi visa pakotne kļūst par arhīva failu ar samazinātu faila lielumu, ko ir viegli augšupielādēt Microsoft veikalā.

## Kā skatīt failus APPX failā?

Lai skatītu saturu vai failus APPX failā, ir jāveic šādas darbības.

 1. Tā kā APPX faili tiek glabāti kā saspiesti ZIP faili, pārdēvējiet failu uz .zip paplašinājumu
 1. Izmantojiet jebkuru dekompresijas rīku, piemēram, 7-Zip, WinZip vai WinRAR, lai izvilktu APPX failā esošos failus.

## Kā izveidot APPX failu?

Ir divas metodes, ko var izmantot, lai izveidotu APPX failus.

 1. MakeApp.exe izmantošana — [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) tiek izmantota, lai izveidotu gan lietotņu pakotnes (.msix vai .appx), gan lietotņu pakotņu komplekta failus .msixbundle vai .appxbundle. Turklāt tas var izvilkt failus no lietotņu pakotnes. MakeApp.exe ir pieejams ar Windows 10 SDK, un to var izmantot, izmantojot komandu uzvedni.
 1. Microsoft Visual Studio izmantošana — izstrādātāji parasti [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) izmanto Microsoft Visual Studio. Kad lietojumprogrammas izstrāde ir pabeigta un lietotne ir gatava publicēšanai, APPX pakotnes failu var izveidot, publicējot to no Visual Studio.

## Atsauces

 * [Izveidojiet MSIX pakotni vai komplektu, izmantojot MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Izveidojiet APPX failus, izmantojot Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

