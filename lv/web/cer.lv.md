{
  "date": "2021-07-13",
  "keywords": [
"CER",
"pagarinājumu",
"failu",
"formātā",
"tīmeklī",
"sertifikāts",
"valodu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER — sertifikāta faila formāts",
  "description": "Uzziniet par CER failu formātu un API, kas var izveidot un atvērt CER failus.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-lvr"
}
},
  "lastmod": "2021-07-13"
}

## Kas ir CER fails? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. Īpaši aizsargātās sertifikātu iestādes ir tās, kas pieder HTTPS — uzticamam un aizsargātam pārlūkošanas protokolam  
CER ir jūsu servera sertifikāts. Parasti to saņem domēna sertifikācijas iestāde. CER lielākoties tiek uzskatīts par tādu pašu kā [CRT](/web/crt/), lai gan abi ir viens un tas pats SSL sertifikāta formāts, taču ir atšķirīgi faila nosaukuma paplašinājumi.
Tos var izmantot operētājsistēmās, vienkārši atverot pārlūkprogrammu un pārbaudot izmantotās pārlūkprogrammas vai vietnes drošību.

## Īsa vēsture ##

1995. gadā Thawte kļuva par pirmo sertifikācijas iestādi, lai atrisinātu publisku SSL (secured socket link) sertifikātu problēmu ārpus ASV. Pēc tam ir virkne šādu iestāžu, kas tika dibinātas no 1995. līdz 2020. gadam.

## CER faila formāts ##

Šie faili var būt vienkārši
* PKC S#7 ietver Base64 ASCII kodējumu
* Tā failu paplašinājumi ir p7b vai p7cZ
* Bināram saturam sertifikāts būtu DER vai pkcs12/pfx.
Ir daudz veidu sertifikātu faili ar dažām unikālām specifikācijām:
* .pem, kad organizācija usThawteificate ķēdē šo formātu ir labi zināms, lai izveidotu sertifikātus
* Nepieciešams .arm, ja sertifikācijas iegūšanas metode palīdz pašparakstītam, šim nolūkam norādītais formāts ir .arm. Tas ir attēlots bāzes-64 ASCII kodējumā.
* .der, tas sastāv no bināriem datiem. Tas nozīmē, ka to var izmantot tikai vienam sertifikātam
* .pfx (PKC512), tā sastāv no privātās atslēgas, kas atbilst CA izdotam sertifikātam vai pašparakstītam sertifikātam. Šis formāts ir labi pazīstams ar vienas SSL ieviešanas konvertēšanu uz otru.


