{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7S fails — digitāli parakstīts e-pasta ziņojums",
  "description": "Uzziniet par P7S failu formātu un API, kas var izveidot un atvērt P7S failus.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-lvs"
}
},
  "lastmod": "2022.01.31"
}

## Kas ir P7S fails?

P7S fails ir ciparparaksts, kas tiek saņemts ar digitāli parakstītu e-pastu. Šī faila klātbūtne kā e-pasta pielikums apliecina, ka e-pasts ir nosūtīts no autentiska avota. Tas nodrošina, ka sūtītāja datorā ir instalēts e-pasta parakstīšanas sertifikāts. Kad šāds parakstīts e-pasts tiek nosūtīts no lietotāja datora, tam tiek pievienots P7S fails, kas satur sūtītāja vārdu. E-pasta klienti, kas atbalsta parakstītus e-pastus, var redzēt sūtītāja informāciju.

## P7S faila formāts — vairāk informācijas

S/MIME (drošs/daudzfunkcionāls interneta pasta paplašinājums) P7S faili satur informāciju vienkārša teksta formātā, kas ir cilvēkiem lasāma. E-pasta klienti, piemēram, Microsoft Outlook, Apple Mail un Mozilla Thunderbird, atbalsta digitāli parakstītas informācijas nolasīšanu no S/MIME e-pasta. E-pasta parakstīšana pārbauda sūtītāja identitāti un informē saņēmēju, ka ziņojums ir autentisks. Kad e-pasta ziņojumi tiek lejupielādēti no e-pasta klientiem (kā [EML](/email/eml/) vai [MSG](/email/msg/)), šie P7S faili tiek pievienoti šiem e-pasta ziņojumiem.

P7S failā ir šāda informācija:

 * E-pasta izcelsmes avots
 * Nosūtīšanas datums un laiks,
 * Vai tas ir pārveidots pārraides laikā

Šī informācija ir iegulta, izmantojot publiskās atslēgas kriptogrāfijas standarta Nr. 7 (PKCS7) tehnoloģiju, lai e-pasta ziņojumam pievienotu šifrētos parakstus.

## Atsauces Nr.

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


