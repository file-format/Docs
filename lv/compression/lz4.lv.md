{
  "date": "2021-04-08",
  "keywords": [
"lz4 fails",
"lz4 faila formāts",
"kas ir lz4 fails",
"failu",
"lz4 piemērs",
"lz4 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 — LZ4 saspiestā faila formāts",
  "description": "Uzziniet par LBR failu formātu un API, kas var izveidot un atvērt LZ4 failus.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-lv4"
}
},
  "lastmod": "2021-04-19"
}

## Kas ir LZ4 fails?

Fails ar paplašinājumu .lz4 ir saspiests arhīva fails, kas izveidots ar lietojumprogrammām/utilītprogrammām, kas atbalsta [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) saspiešanu. LZ4 algoritms koncentrējas uz kompromisu starp ātrumu un kompresijas pakāpi. Saspiestus LZ4 arhīvus var izveidot, izmantojot LZ4 komandrindas utilītu, un tos var atspiest, izmantojot to pašu.

## LZ4 faila formāts

LZ4 faila formāts, kas balstīts uz LZ4 saspiešanas algoritmu, nav atkarīgs no CPU veida, operētājsistēmas, failu sistēmas un rakstzīmju kopas. Tas ir piemērots failu saspiešanai un straumēšanas saspiešanai, izmantojot LZ4 algoritmu. Sākotnējo LZ4 formāta ieviešanu [C](/programming/c/) valodā veica Yann Collet 2011. gadā, un tas ir pieejams izstrādātāju uzziņai vietnē [Github](https://github.com/lz4/lz4).

### LZ4 rāmja formāts

LZ4 faila formāta vispārējā struktūra ir tāda, kā parādīts zemāk.

|MagicNb|F. Deskriptors| Bloks|(...)|Beigu atzīme |C. Kontrolsumma|
---|---|---|---|---|---|
|4 baiti| 3–15 baiti ||| 4 baiti| 0-4 baiti|

#### Maģiskais numurs

4 baiti, Little Endian formāts. Vērtība: 0x184D2204

#### Rāmja deskriptors

Kadra deskriptors sastāv no 3 t0 15 baitiem, un tas ir vissvarīgākā specifikāciju daļa. Lauki Magic_Number un Frame_Descriptor kopā tiek saukti par LZ4 Frame Header, un tā lielums svārstās no 7 līdz 19 baitiem. Tas ir kā parādīts zemāk.

|FLG| BD| (Satura lielums)| (Vārdnīcas ID)| HC|
---|---|---|---|---|
|1 baits| 1 baits| 0 - 8 baiti| 0 - 4 baiti| 1 baits|

#### Datu bloki

Katrs datu bloks atbilst šādai secībai.

|Bloka izmērs| dati| (Bloka kontrolsumma)|
---|---|---|
|4 baiti| |0 - 4 baiti|

#### EndMark

Bloku plūsma beidzas, kad pēdējam datu blokam seko 32 bitu vērtība 0x00000000.

#### Satura kontrolsumma

Content_Checksum pārbauda pareizi atšifrētā satura derīgumu un tiek veikta, izmantojot xxHash-32 algoritma rezultātu. Tas apstiprina visu bloku veiksmīgas pārsūtīšanas rezultātus pareizā secībā un bez kļūdām.

## Atsauces

* [LZ4 rāmja formāts](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)

* [LZ4 saspiešanas algoritms — Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))


