{
  "date": "2021-04-22",
  "keywords": [
"msix fails",
"pagarinājumu",
"formātā",
"Kā atvērt msix failu",
"msix faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX — kas ir MSIX fails?",
  "description": "Uzziniet par MSIX failu un API, kas var izveidot un atvērt MSIX failus.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-lvx"
}
},
  "lastmod": "2021-12-16"
}

## Kas ir MSIX fails?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Šis ir modernais pakotnes faila formāts salīdzinājumā ar [APPX](/programming/appx/) un MSI, kas beidzot tiks pakāpeniski izņemts uz šo jauno faila formātu. To var izmantot Win32, WPF un Windows Forms lietotņu izvietošanai. MSIX faili ir uzticami, un to mērķis ir tīkla un diska vietas optimizācija. Izstrādātāji tos izmanto, lai izplatītu programmas galalietotājiem, izmantojot Microsoft Store (iepriekš zināms kā Windows Store).

## MSIX faila formāts — vairāk informācijas

MSIX faili ir [ZIP](/compression/zip/) saspiesti, un visi faili ir iekļauti iepakotajā failā. Papildus ar lietotni saistītajiem failiem MSIX failā ir [.xml](/web/xml/) konfigurācijas faili, kas satur informāciju, kas saistīta ar lietotnes instalēšanu.

## Kas atrodas MSIX pakotnē?

MSIX pakotne sastāv no šādiem failiem.

 * AppxBlockMap.xml — pazīstams kā pakotņu bloka kartes fails, tas ir XML dokuments, kurā ir ietverts lietotnes failu saraksts ar indeksiem un kriptogrāfiskām jaukām katram pakotnē saglabātajam datu blokam.
 * AppxManifest.xml — XML dokuments, kas satur informāciju, kas nepieciešama MSIX lietotnes izvietošanai, parādīšanai un atjaunināšanai. Šī informācija ietver pakotnes identitāti, pakotnes atkarības, nepieciešamās iespējas, vizuālos elementus un paplašināšanas punktus.
 * AppxSignature.p7x — fails, kas tiek ģenerēts, kad pakotne ir parakstīta. Pirms instalēšanas visas MSIX pakotnes ir jāparaksta. Izmantojot AppxBlockmap.xml, platforma var instalēt pakotni un tikt apstiprināta.

## Atsauces

 * [MSIX pārskats](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Izveidojiet APPX failus, izmantojot Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

