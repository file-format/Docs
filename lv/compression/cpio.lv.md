{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO fails — Unix CPIO arhīva faila formāts",
  "description":"Uzziniet, kas ir CPIO fails un API, kas var izveidot un atvērt CPIO failus.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Kas ir CPIO fails?

CPIO fails ir arhīva fails, kas izveidots Unix formātā Copy In Copy Out (CPIO). Tas ir līdzīgs TAR faila formātam, izņemot to, ka tas ir nesaspiests. CPIO failos var saglabāt ierīces failus, simboliskas saites un paplašinātus failu atribūtus.

## CPIO faila formāts

CPIO arhīvs tiek izveidots kā binārs fails, kas nav cilvēkiem lasāms. Tas saglabā failu un direktoriju kolekciju. CPIO arhīva saturs tiek identificēts ar metadatu informāciju, piemēram, failu nosaukumiem, atļaujām, īpašumtiesībām un laika zīmogiem. Šī metadatu informācija tiek saglabāta arī arhīva failā, lai sistēma varētu tai piekļūt.

## CPIO arhīva formāts

CPIO fails sastāv no viena vai vairākiem sasaistītiem dalībnieku failiem. Katrs arhīva fails sastāv no galvenes, kam pēc izvēles seko faila saturs, kā minēts galvenē. Arhīva beigās ir vēl viena galvene, ko apraksta tukšs fails ar nosaukumu TRAILER!!.

### CPIO arhīvu veidi

Ir divu veidu CPIO arhīvi. Tie atšķiras tikai pēc galvenes stila.

* ASCII arhīvi — šiem CPIO arhīviem ir drukājama galvene, kas kļūst par daļu no CPIO arhīva, ja pats arhīvs sastāv no ASCII failiem.

* Binārie arhīvi — šiem CPIO arhīviem ir bināras galvenes.


## Darbs ar CPIO arhīvu

### Kā izveidot CPIO arhīvus?

Varat izveidot CPIO Unix līdzīgās sistēmās, izmantojot komandu **cpio**. Šī komanda atradīs visus failus un direktorijus pašreizējā direktorijā un tā apakšdirektorijās. Pēc tam šī izvade tiek nosūtīta uz komandu cpio, kas ģenerēs jaunu CPIO arhīvu ar nosaukumu arhivs.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Kā izvilkt failus no CPIO arhīviem?

Šī komanda izvelk failus no esoša arhīva.

```
cpio -id < archive_cpio.cpio
```
Tas nolasīs archive.cpio failu no standarta ievades un izvilks failus pašreizējā direktorijā.


## Atsauces

* [CPIO — Wikipedia](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

