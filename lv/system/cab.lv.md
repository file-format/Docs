{
  "date": "2021-06-29",
  "keywords": [
"TAKSIS",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Windows kabineta fails",
"Microsoft",
"Uzstādītājs",
"Uzstādīt",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB — Windows kabineta fails",
  "description": "Uzziniet par CAB failu formātu un API, kas var izveidot un atvērt CAB failus.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-lvb"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir CAB fails? ##

Fails ar paplašinājumu .cab pieder Windows kabineta failam, kas pieder sistēmas failu kategorijai. Tas ir fails, kas tiek saglabāts arhīva faila formātā Microsoft Windows versijās, kas atbalsta saspiestu datu algoritmus, piemēram, [LZX](/compression/lzx/), Quantum un [ZIP](/compression/zip/). Fails ir ļoti svarīgs, ja lietotājs vai izstrādātājs vēlas saturēt un koplietot programmatūras instalēšanas datus un failus. Šajos failos iekļautās datu bezzudumu saspiešanas funkcijas un digitālā sertifikācija padara šo failu ideāli piemērotu šādu failu glabāšanai un kopīgošanai. Tā atbalsta dažādus Microsoft instalētājus, piemēram, Device Installer, SetUp API un AdvPak.

## Īsa vēsture ##

CAB fails ir datu saspiešanas faila veids, ko izstrādājis Microsoft. Sākotnēji to sauca par Dimantu, bet pēc tam tas kļuva pazīstams kā CAB fails, saīsinājums no vārda Cabinet

## Tehniskā specifikācija Nr.

CAB failā parasti var būt ne vairāk kā 65 535 mapes, kas savukārt var saturēt ne vairāk kā 65 536 failus katrā. CAB failu glabāšanas mehānisms ir efektīvs laika un vietas ziņā, jo tas katru mapi saglabā kā saspiestu bloku, nevis saspiež un glabā katru failu atsevišķi. Tukšas mapes nevar saglabāt CAB arhīva mapēs. CAB failu vispirms izstrādāja Microsoft, un to izmanto dažādos instalēšanas programmās, piemēram, InstallShield ar nedaudz atšķirīgu formātu. CAB faili parasti tiek savienoti ar pašizpletes programmām. Microsoft CAB faili ir viegli atpazīstami, pateicoties to unikālajam marķierim, kas palīdz noteikt formātu. Unikālais marķieris visiem Microsoft CAB failiem ir četru vārdu prefikss MSCF. Redzot šo kodu, lietotājs var viegli atšķirt Microsoft CAB failu no citiem failiem un attiecīgi izmantot to kompresoros vai versijās. Failus var saspiest, izmantojot vairāk programmatūras instalēšanas datu, vai pašreizējos datus var atspiest, izmantojot pareizo programmatūru.


## CAB piemērs ##

Šis piemērs ilustrē attiecības starp failiem un mapēm CAB failu struktūrā:

{{< figure src="../cab.png" alt="CAB faila formāts" >}}

## Atsauce Nr.

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
