{
  "date": "2022-09-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRL fails — sertifikātu atsaukšanas saraksts",
  "description": "Uzziniet par CRL faila formātu un API, kas var izveidot un atvērt CRL failus.",
  "linktitle": "CRL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-lvl"
}
},
  "lastmod": "2022-09-01"
}

## Kas ir CRL fails?

CRL (Certificate Revocation List) fails ir X.509 ciparsertifikātu melnais saraksts, ko sertifikātu iestāde (CA) atsauc pirms tiem piešķirtā atsaukšanas datuma. Tajā ir informācija par problēmu un atsaukšanas datumu, kas ļauj drošības administratoriem bloķēt ietekmētos ciparsertifikātus. CRL neietver sertifikātus, kuriem beidzies derīguma termiņš, jo tā galvenais mērķis ir paziņot par neuzticamiem un nederīgiem sertifikātiem.

Lietojumprogrammas, kas var **atvērt CRL failus**, ietver OpenSSL, Microsoft IIS Server un Citrix NetScaler.

## CRL faila formāts — vairāk informācijas

CRL faili satur informāciju X.509 standartā, kas arī nosaka tā semantiku publiskās atslēgas informācijas koplietošanai. Cita CRL failā ietvertā informācija var ietvert termiņu, uz kuru sertifikāti ir atsaukti, atsaukšanas iemeslu, atsauktā sertifikāta sērijas numuru un laika zīmogu.


### Galvenie iemesli, kāpēc sertifikāti tiek pievienoti CRL

Var būt vairāki iemesli, kāpēc jūsu vietnes sertifikāts tiek atsaukts un pievienots CRL. Daži no tiem varētu būt;

1. Jūsu sertifikāta privātā atslēga ir apdraudēta
1. Jūsu sertifikāts nav derīgs vai to ir nepareizi izdevusi CA
1. Tiek mainīta ar sertifikātu saistītā organizatoriskā informācija, un CA izsniedz jaunu sertifikātu
1. Jebkurš cits neizbēgams iemesls, kura dēļ sertifikāts ir atsaukts

## Atsauces

* [Nacionālais standartu un tehnoloģiju institūts (NIST)](https://csrc.nist.gov/glossary/term/CRL)

* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)

* [Sertifikācijas atsaukšanas saraksts](https://en.wikipedia.org/wiki/Certificate_revocation_list)


