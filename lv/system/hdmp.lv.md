{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDMP fails — Windows Heap Dump faila formāts",
  "description": "Uzziniet par HDMP failu formātu un API, kas var izveidot un atvērt HDMP failus.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-lvp"
}
},
  "lastmod": "2022-08-19"
}

## Kas ir HDMP fails?

HDMP fails ir nesaspiesta atmiņas izgāztuve, kad lietojumprogramma vai programma avarē kļūdas dēļ. Tas ir izveidots tikai operētājsistēmā Windows XP/Vista, un tajā ir lietojumprogrammas statusa izdruka, kad tā avarēja. Tā kā HDMP faili nav saspiesti, tie aizņem vairāk vietas diskā, salīdzinot ar Minidump [MDMP](/system/mdmp/) failiem, kas ir saspiesti ziņošanas nolūkos.

Lietojumprogrammas, kuras var izmantot, lai **atvērtu** vai analizētu HDMP failus, ietver Microsoft Visual Studio ar atkļūdošanas rīkiem operētājsistēmai Windows.

## HDMP faila formāts

HDMP faili tiek saglabāti diskā kā bināri faili, un tie nesniedz nekādu labumu, ja tie tiek atvērti bez atbilstošām lietojumprogrammām. Tajos ir ietverti attiecīgie sistēmas dati, kas reģistrēti, kad radās kļūda.

### Atšķirība starp HDMP un MDMP failu formātiem

HDMP ir nesaspiesti atmiņas izdrukas faili. Turpretim MDMP ir mini izgāztuves faili, kas tiek saspiesti, lai samazinātu faila lielumu un nosūtītu Microsoft ziņošanai par problēmu.

## Atsauce Nr.

* [DMP — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


