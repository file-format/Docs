{
  "date": "2021-07-29",
  "keywords": [
"pes fil",
"pes filformat",
"hvad er en pes-fil",
"fil",
"pes eksempel",
"pes filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PES-filformat - Brother PE-broderiformat",
  "description": "Lær om PES-filformat og API'er, der kan oprette og åbne PES-filer.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pe-das"
}
},
  "lastmod": "2021-07-29"
}

## Hvad er en PES-broderifil?

PES-broderifilen er en designfil, der indeholder instruktioner til broderi-/symaskinerne. Det blev udviklet af Brother Industries til deres broderimaskiner, men blev senere formaliseret som et generelt filformat. PES-filer bruges af symaskiner til at læse instruktioner til at sy mønstre på stof. Disse filer tjener to formål; først at give designoplysninger til PE-Design-applikation udviklet af Brother Industries og for det andet at give designnavn, farver og broderimaskinekoder såsom stop, hop og trim.

## PES-filformat - flere oplysninger

En PES-fil gemmes på disk i binært filformat. Den indeholder flere sektioner, der har syinformation gemt ved hjælp af en foruddefineret metode. PES-filformatet er som følger.

 * Versionsdata - Giver versionsoplysninger og kan være en hvilken som helst værdi #PES0001, #PES0020, #PES0030, #PES0040, #PES0050, #PES0055, #PES0060.
 * PEC-søgeværdi - Et 4 byte lille-endian-heltal umiddelbart efter versionsdataene og repræsenterer søgeværdien for PEC-sektionen, der indeholder designdetaljer Information
 * PSE-sektion - Indeholder designoplysninger, der er relevante for Brother PE-designet og kan være andre syapplikationer
 * PCE-sektion - Kan være hvor som helst i PSE-filen, men refereret til af PEC-søgeværdien.

## Type symaskiner, der bruger PES-fil

PES-filer oprettes primært af PE-Design-softwaren, der bruges sammen med Brothers symaskiner. Nogle andre maskiner, der muligvis understøtter PES-filer, inkluderer Babylock og Bernina hjemmebroderimaskiner.

## Sådan konverteres PSE-filer?

PE-Design-softwareapplikationen kan [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) til andre formater såsom .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd eller .xxx . Det kan gøres ved at bruge PE-Design-applikationen ved at åbne filen og vælge Konverteringsformatet.

## Referencer

* [PE Design - Instruktionsmanual](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)


