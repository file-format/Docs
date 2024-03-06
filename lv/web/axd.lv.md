{
  "date": "2023-05-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AXD fails — ASP.NET tīmekļa apdarinātāja faila formāts",
  "description": "Uzziniet, kas ir AXD fails un API, kas var izveidot un atvērt AXD failus.",
  "linktitle": "AXD",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ax-lvd"
}
},
  "lastmod": "2023-05-23"
}

## Kas ir AXD fails?

AXD fails ir tīmekļa iestatījumu fails, ko izmanto, lai apstrādātu un izgūtu iegulto resursu pieprasījumus ASP.NET. Tajā ir ietverti norādījumi par iegulto resursu, piemēram, attēlu, JavaScript ([.JS](/web/js/)) failu un [.CSS](/web/css/) failu, izgūšanu. AXD faili tiek izmantoti resursu ievadīšanai klienta puses lapās. Tas ļauj klientu lapām standarta veidā piekļūt šiem servera resursiem.

## AXD faila formāts

AXD faili tiek glabāti kā binārie faili servera pusē. Tas attiecas uz Web Handler failu ASP.NET, kas ir komponenti, kas ģenerē atbildes uz konkrētiem pieprasījumiem tīmekļa serverim. AXD faili veic pielāgotu apstrādi pirms atbildes ģenerēšanas, pamatojoties uz klienta puses lapu pieprasījumiem. Tie parasti tiek saglabāti kā **WebResource.axd** faili.

### Kas ir WebResource.axd fails?

Lielākā daļa ASP.NET projektu saglabā AXD failus kā WebResource.axd failus, kas ļauj klienta puses lapām lejupielādēt resursus, kas ir iegulti komplektā. Jūsu lietojumprogramma var saskarties ar lēnu veiktspēju, ja palaižat to atkļūdošanas režīmā, jo WebResources.axd apstrādātājs nav kešatmiņā.

## Atsauces

 * [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

