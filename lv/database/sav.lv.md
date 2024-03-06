{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par SAV failu formātu un API, kas var izveidot un atvērt SAV failus.",
  "title" : "SAV — SPSS datu fails",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-lv",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Kas ir SAV fails?
SAV fails ir datu fails, ko izveido sociālo zinātņu statistikas pakotne (SPSS), kas ir lietojumprogramma, ko plaši izmanto tirgus pētnieki, veselības pētnieki, aptauju uzņēmumi, valdība, izglītības pētnieki, mārketinga organizācijas, datu ieguvēji statistikas analīzei. SAV, kas saglabāts patentētā binārā formātā, sastāv no datu kopas, kā arī vārdnīcas, kas attēlo datu kopu, saglabā datus rindās un kolonnās.

## SAV faila formāts
SAV faila formāts ir kļuvis salīdzinoši stabils, taču mēs nevaram teikt, ka tas ir statisks. Atpakaļ un uz priekšu saderība ir pēc izvēles pieejama, ja nepieciešams, bet netiek pareizi uzturēta. Dati SAV failā ir iedalīti šādās sadaļās:

### Faila galvene
Tas sastāv no 176 baitiem. Pirmie 4 baiti norāda virkni **$FL2** vai **$FL3** failam izmantotajā rakstzīmju kodējumā. Pēdējie trīs baiti norāda, ka dati failā ir saspiesti, izmantojot **ZLIB**. Nākamā 60 baitu virkne sākas ar **@(#) SPSS DATA FILE**, kā arī nosaka operētājsistēmu un SPSS versiju, kas izveidoja failu. Pēc tam galvene turpinās ar sešu ciparu laukiem, kas satur mainīgo skaitu katrā novērojumā un ciparu kodu saspiešanai, un beidzas ar rakstzīmju datiem, kas norāda izveides datumu un laiku, un faila etiķeti.
### Mainīgo deskriptora ieraksti
Ieraksts satur fiksētu lauku secību, kas klasificē mainīgā veidu un nosaukumu kopā ar SPSS izmantoto formatēšanas informāciju. Katrs mainīgā ieraksts pēc izvēles var ietvert mainīgā apzīmējumu līdz 120 rakstzīmēm un līdz trim trūkstošām vērtībām.
### Vērtību etiķetes
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Pirmajam ierakstam, kas ir 3. tags, ir virkne lauku pāru, un katrs pāris satur vērtību un saistīto vērtības apzīmējumu. Otrais ieraksts, kas ir 4. tags, norāda, uz kuriem mainīgajiem attiecas vērtību/iezīmju kopa.
### Dokumenti
Single or multiple records with integer tag 6. Pēc izvēles dokumentācija. satur 80 rakstzīmju rindiņas.
### Paplašinājuma ieraksti
Single or multiple records with integer tag 7. Paplašinājuma ieraksti sniedz informāciju, ko var droši ignorēt, taču daudzās situācijās saglabājot, ļauj jaunākā programmatūras rakstītajiem failiem saglabāt atpakaļejošu saderību. Paplašinājuma ierakstos ir veselu skaitļu apakštipu tagi.
### Vārdnīcas terminators
Only record with integer tag 999. Tas atdala vārdnīcu no datu novērojumiem.
### Datu novērojumi
Tiek uzskatīts, ka dati ir novērojumu secībā, piemēram, visas mainīgās vērtības pirmajam novērojumam, pēc tam visas vērtības otrajam novērojumam utt. Datu ieraksta formāts mainās atkarībā no saspiešanas koda faila galvenes ierakstā. Sav faila datu daļu var nesaspiest:
- **kods 0**: saspiests ar baitkodu
- **kods 1**: saspiests, izmantojot ZLIB saspiešanu
 






## Atsauces Nr.

* [SPSS sistēmas datu failu formātu saime (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


