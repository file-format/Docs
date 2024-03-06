{
  "date": "2021-08-10",
  "keywords": [
".ovf fails",
"faila formātā",
"kas ir .ovf fails",
"failu",
"faila paplašinājums"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet, kas ir .ovf faila formāts un API, kas var izveidot un atvērt OVF failus.",
  "title": "OVF faila formāts - atveriet virtualizācijas failu",
  "linktitle": "OVF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-lvf"
}
},
  "lastmod": "2022-01-03"
}

## Kas ir OVF fails?

OVF fails ir teksta fails, kas satur informāciju par programmatūras iepakošanu un izplatīšanu, kas darbojas virtuālajā mašīnā. Tas ir formatēts atbilstoši [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf), kas apraksta visas prasības (piemēram, drošību, pārnesamību, efektivitāti un paplašināmību), lai palaistu lietojumprogrammas virtuālajās mašīnās. Starptautiskā standartizācijas organizācija (ISO) ir pieņēmusi OVF kā ISO 17203 standartu.

## Īsa OVF faila formāta vēsture

OVF faila formātu ieviesa DMTF (Distributed Management Task Force), kas izveido atvērtus pārvaldības standartus. Tas ir neatkarīgs no jebkura hipervizora vai instrukciju kopas arhitektūras. OVF pakotnē ir viena vai vairākas virtuālās sistēmas, no kurām katru var izvietot virtuālajā mašīnā.

## OVF faila formāts — vairāk informācijas

OVF pakotne sastāv no vairākiem failiem, kas ievietoti vienā direktorijā. Starp tiem tajā ir tieši viens OVF deskriptora (ar paplašinājumu .ovf) fails, kas tiek saglabāts [XML](/web/xml/) faila formātā. Tajā ir aprakstīta iepakotā virtuālās mašīnas informācija un metadatu informācija par OVF pakotni, piemēram:

 * nosaukums
 * aparatūras prasības
 * atsauces uz citiem failiem OVF pakotnē un
 * human-readable descriptions

Citi faili, ko var atrast OVF pakotnē, ietver vienu vai vairākus diska attēlus un pēc izvēles sertifikātu failus un citus palīgfailus.

## Atsauces

* [Atvērtais virtualizācijas formāts — DMTF](https://www.dmtf.org/standards/ovf)

* [OVF faila formāta specifikācijas](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)


