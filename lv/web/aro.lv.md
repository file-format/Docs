{
  "date": "2021-12-09",
  "keywords": [
"aro",
".aro failu",
"aro faila formātā",
"faila tips",
"failu",
"veids",
"kas ir .aro fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARO faila formāts — SteelArrow tīmekļa lietojumprogrammas fails",
  "description": "Uzziniet, kas ir ARO fails un API, kas var izveidot un atvērt ARO failus.",
  "linktitle": "ARO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ar-lvo"
}
},
  "lastmod": "2021-12-09"
}

## Kas ir ARO fails?

ARO fails ir servera puses tīmekļa lapas fails, kas tiek ģenerēts ar SteelArrow Web Application. Tas satur [HTML](/web/html/) un SteelArrow tagus un skriptus. Tie tiek izpildīti serverī, lai ģenerētu pilnīgu atbildes lapu pirms to nosūtīšanas uz lietotāja pārlūkprogrammu. ARO faili satur gandrīz 95% HTML satura, bet pārējais sastāv no SteelArrow koda. Lai ARO faili darbotos jūsu labā, SteelArrow Web Applications serverim ir jābūt instalētam un jādarbojas tīmekļa servera mašīnā.

## ARO faila formāts

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web pages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### ARO taga piemērs

The<SAOUTPUT> ARO tags ļauj izstrādātājiem izvadīt datu vērtības jebkurā skripta vietā. Piemēram, to var izmantot, lai iegūtu PARAM tabulas izvadi ar<SAOUTPUT VALUE=PARAM[]> ko var parādīt HTML<BODY> tagu.

## Atsauces

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)

