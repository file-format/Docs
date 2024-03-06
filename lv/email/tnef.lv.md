{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "Uzziniet par TNEF faila formātu un API, kas var izveidot un atvērt TNEF failus.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir TNEF fails?

Transport Neutral Encapsulation Format (TNEF) ir Microsoft patentēts e-pasta pielikumu iekapsulēšanai, pamatojoties uz Messaging Application Programming Interface (**MAPI**). Microsoft Outlook un Microsoft Exchange Server pilnībā atbalsta TNEF, savukārt vēlāk TNEF atšifrē MAPI un parāda formatētos e-pastus. E-pasta pielikumam ar TNEF kodējumu ir MIME veids MS-TNEF, un tas tiek saglabāts kā winmail/win.dat. Pielikumā winmail .dat ir ietverta šāda informācija:


|Ziņojums|OLE objekti|Outlook līdzekļi
---|---|---|
|<ul><li> Oriģinālo ziņojumu pielikumi</li><li> Oriģinālā formatētā versija</li><li> fontus, teksta izmērus un teksta krāsas</li></ul> |<ul><li> iegultie attēli</li><li> iegultie Office dokumenti</li></ul> |<ul><li> pielāgotas veidlapas</li><li> balsošanas pogas</li><li> tikšanās pieprasījumi</li></ul>


Citi e-pasta pakalpojumi, kas neatbalsta TNEF, piedāvā vienkāršu tekstu TNEF formāta ziņojumiem. Programma Outlook iegulst bagātīgu ziņojuma formātu TNEF failos (OLE) vai konkrētos Outlook līdzekļos (veidlapas, aptaujas pogas un konferences pieprasījumi). Sankcionēt skaidru TNEF kodējumu Outlook e-pasta klientā nav iespējams, tomēr RTF formāta izvēle e-pasta nosūtīšanai netieši atvieglo TNEF kodēšanu.

## TNEF faila formāts

TNEF datu algoritms izveido saplacinātu struktūru no bagātīgām hierarhiskām ziņojumu īpašībām. Šīs saplacinātās struktūras pēc tam tiek izmantotas, lai attēlotu sērijveida datu straumi, kas sastāv no konkrētām īpašībām.

Dažās situācijās, kad rekvizīti ir sastopami grupās vai tiem ir vairākas vērtības, straumē var būt iekļauti skaitļi un pildījumi, lai ieviestu noteiktu datu izlīdzināšanu. Īpaša situācija, kad šī algoritma izmantošana ir izdevīga, ir neatbalstošā ziņojumapmaiņas vidē. Šādās vidēs bagātīgu ziņojumu rekvizītu TNEF Writer kodē sērijas datu straumē. Turklāt rekvizīti, kas nepieder pamatā esošajam TNEF, pārraides laikā var tikt iekapsulēti. Šie iekapsulētie rekvizīti pēc tam kļuva pieejami, dekodējot, izmantojot TNEF, lai nodrošinātu visu sākotnējā ziņojuma rekvizītu pieejamību klienta lietojumprogrammai.

TNEF visi skaitļu datu tipi ir mazi un to lielums ir lielāks par vienu baitu. Lai apstrādātu šīs skaitliskās vērtības platformās, kas nav mazas, ir jāveic atbilstošas transformācijas, lai iegūtu pareizas vērtības. Virknes vērtības tiek attēlotas paplašinātā Backus-Naur Form (ABNF) formātā saskaņā ar [RFC5234] specifikācijām. Kad virkne beidzas ar nulles rakstzīmi, tā tiek iekļauta arī; piemēram, `darbinieks@paraugs.com %x00`.

{{< figure src="../TNEF.png" alt="TNEF faila formāts" >}}

## TNEF atribūti un apstrādes noteikumi ##

Datu straume TNEF sākas ar mantotās versijas numuru, parakstu, primitīvu atslēgas vērtību un atribūtu, kas apzīmē koda lapu. Šī koda lapa tiek ģenerēta, kad kodētājs ieraksta ANSI atribūtus un rekvizītus. Pēc tam straume kļuva par atribūtu sēriju, kurā vispirms tika izvietoti ziņojuma atribūti un pēc tam sekoja pielikuma atribūti. Dažādi ziņojumu un pielikumu raksturlielumi ir ietverti īpašos atribūtos, piemēram, attMsgProps, attAttachment un attRecipTable. Atribūtos, kas parādās TNEF straumē, ir ietverta struktūra, ziņojuma rekvizīti un reklāmguvumi, kas nepieciešami, lai tos piesaistītu ziņojuma rekvizītiem. Katrs atribūts sastāv no ID, atribūta lieluma un datiem, kontrolsummas un līmeņa atbilstoši tā lietojumam.

## Saistība ar protokoliem un citiem algoritmiem ##

Sistēmām, kurām ir slikts mehānisms, lai sākotnēji parādītu bagātīgu ziņojumu formātu, transportēšanai ir nepieciešams TNEF datu algoritms. Izmantojot multivides tipu ms-TNEF, algoritma izvade sastāv no pielikuma faila (winmail.dat) un MIME pamatdaļas, kas norādīta [RFC2045]. Vienkāršā teksta ziņojuma pamatteksts tiek pārsūtīts, izmantojot UUENCODE saskaņā ar [MSDN-UAF] specifikāciju, un šis ziņojuma pamatteksts vai līdzvērtīga metode tiek dekodēta adresāta galā. Turklāt TNEF var pārsūtīt ziņojumu datus, izmantojot dažādus interneta protokolus, piemēram, SMTP, POP3, IMAP4 un tos, kas integrē MIME saskaņā ar RFC2045 standartu.

## Piemērojamības paziņojums Nr.

Papildus vienkāršai ziņojumu pārraidei TNEF sākotnējā lietojumprogramma bija jāizveido, lai izmantotu ziņojumu klases un atbalstītu papildu funkcijas, kurām nav oriģināla atbalsta transporta protokolā. Šī lietojumprogramma tika tālāk uzlabota, lai pārraidītu bagātīgus ziņojumu rekvizītus un nosauktos rekvizītus, kurus mūsdienās izmanto mūsdienu ziņojumapmaiņas klienti. Lai nodrošinātu atbilstību sākotnējai ieviešanai, tiek saglabāta sākotnējā atribūta sintakse, un īpašs atribūts satur jauno ziņojuma rekvizītus atsevišķi.

## Atsauces

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [E-pasta adreses un adrešu grāmatas programmā Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)

* [[MS-OXTNEF]: Transporta neitrāla iekapsulēšanas formāta (TNEF) datu algoritms](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


