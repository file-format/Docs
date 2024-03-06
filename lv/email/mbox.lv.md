{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX — e-pasta pastkastes fails",
  "description": "Uzziniet par MBOX failu formātu un API, kas var izveidot un atvērt MBOX failus.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir MBOX fails?

MBox faila formāts ir vispārīgs termins, kas apzīmē konteineru elektroniskā pasta ziņojumu apkopošanai. Ziņojumi tiek glabāti konteinerā kopā ar to pielikumiem. Ziņojumi no visas mapes tiek saglabāti vienā datu bāzes failā, un jauni ziņojumi tiek pievienoti faila beigām. Daudzas lietojumprogrammas un API nodrošina atbalstu MBox failu formātam, piemēram, Apple Mail un Mozilla Thunderbird.

## MBOX faila formāts ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Ziņojuma lasīšana no MBox faila ##

Lasītājs skenē mbox failu, meklējot rindiņas From_. Jebkura From_ rinda iezīmē ziņojuma sākumu. Lasītājam nevajadzētu mēģināt izmantot to, ka katra From_ rindiņa (pēc faila sākuma) ir tukša. Kad lasītājs atrod ziņojumu, tas no rindas No_ izņem (iespējams, bojātu) aploksnes sūtītāju un piegādes datumu. Pēc tam tas tiek nolasīts līdz nākamajai rindiņai From_ vai faila beigām, atkarībā no tā, kas tiek izpildīts pirmais. Tas noņem pēdējo tukšo rindiņu un dzēš citātu >No_rindām un >>No_rindiņām un tā tālāk. Rezultāts ir RFC 822 ziņojums.

## Kodēšanas apsvērumi ##

MBox faila saturs var neatgriezeniski sajaukties, ja saņemtajā e-pastā kā pielikums ir Mbox fails un tas tiek saglabāts citā Mbox failā. Lai no tā izvairītos, ziņojumapmaiņas sistēmām ir jākodē mbox datu bāze ar necaurspīdīgu pārsūtīšanas kodējumu (piemēram, BASE64 vai Quoted-Printable), kad šāds objekts tiek pārsūtīts, izmantojot ziņojumapmaiņas protokolus. Ieviestājiem jābūt gataviem arī lokāli kodēt mbox datus, ja tiek saņemti neatbilstoši dati.

## Atsauces Nr.

* [MBox — RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox — Wikipedia](https://en.wikipedia.org/wiki/Mbox)


