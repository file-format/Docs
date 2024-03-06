{
  "date": "2021-07-28",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QBL — QuickBooks licences fails",
  "description": "Uzziniet par QBL failu formātu un API, kas var izveidot un atvērt QBL failus.",
  "linktitle": "QBL",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-qb-lvl"
}
},
  "lastmod": "2021-07-28"
}

## Kas ir QBL fails?

Fails ar paplašinājumu .qbl ir QuickBooks licences fails, kas satur lietotāja iegādātās kopijas licencēšanas informāciju. Tas parasti tiek saglabāts vietējā sistēmā ar nosaukumu license.qbl pēc QuickBooks instalēšanas un lietotājs ievada licencēšanas informāciju programmatūrā, kad programmatūra tiek palaista pirmo reizi. QBL bija agrākais faila formāts, ko izmantoja QuickBooks licencēšanas informācijas glabāšanai. Tagad tas ir aizstāts ar QuickBooks `qbregisteration.dat' failu, un tas ir aizpildīts ar informāciju no lietotāja apstiprinājuma e-pasta, iegādātā DVD vai citiem pirkšanas līdzekļiem. QBL failus var atvērt jebkurā teksta redaktorā, piemēram, Windows Notepad, Apple TextEdit, Notepad++, Github Atom redaktorā un daudzos citos.

## QBL faila formāts — vairāk informācijas

QBL faili tiek izveidoti un saglabāti kā vienkārša teksta faili. Informācija šajos failos ir cilvēkiem lasāma, un to var rediģēt/atjaunināt, kad šie faili tiek atvērti teksta redaktoros. Licencēšanas un lietotāja reģistrācijas informāciju pēc tam var iekopēt šajā failā, lai sāktu darbu ar QuickBooks programmatūru. QBL faili parasti tiek glabāti Windows operētājsistēmas direktorijā Program Files\Intuit\QuickBooks\INET.

QBL fails satur divu veidu informāciju.

* `QuickBooks versijas informācija:` attiecas uz instalēto QuickBooks versiju un ir tādā formātā kā xx.x

* Licences atslēga: teksts 000-000 0000-0000-0000-000 000073adbf3f formātā, kur 000-000 0000-0000-0000-000 tiek aizstāts ar lietotāja qbregisteration atslēgu.


## Atsauces

 * [QuickBooks by Intuit](https://quickbooks.intuit.com/)
 * [QuickBooks — faila qbregistration.dat ģenerēšana](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)

