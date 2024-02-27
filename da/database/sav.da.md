{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om SAV-filformat og API'er, der kan oprette og åbne SAV-filer.",
  "title" : "SAV - SPSS datafil",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-da",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Hvad er en SAV fil?
SAV-fil er en datafil, der er oprettet af Statistical Package for the Social Sciences (SPSS), som er en applikation, der i vid udstrækning bruges af markedsforskere, sundhedsforskere, undersøgelsesvirksomheder, regering, uddannelsesforskere, marketingorganisationer, dataminere til statistisk analyse. SAV gemt i et proprietært binært format og består af et datasæt samt en ordbog, der repræsenterer datasættet, gemmer data i rækker og kolonner.

## SAV filformat
SAV-filformatet er blevet relativt stabilt, men vi kan ikke sige det statisk. Bagud- og fremadkompatibilitet er valgfrit tilgængelig, hvor det er nødvendigt, men vedligeholdes ikke korrekt. Dataene i en SAV-fil er kategoriseret i følgende sektioner:

### Filoverskrift
Den består af 176 bytes. De første 4 bytes angiver strengen **$FL2** eller **$FL3** i den tegnkodning, der bruges til filen. De sidste tre bytes repræsenterer, at dataene i filen er komprimeret ved hjælp af **ZLIB**. Den næste 60-byte streng begynder **@(#) SPSS DATA FILE** og bestemmer også operativsystemet og SPSS-versionen, der oprettede filen. Overskriften fortsætter derefter med sekscifrede felter, der indeholder antallet af variable pr. observation og en cifferkode til komprimering, og slutter med tegndata, der angiver oprettelsesdato og -tidspunkt og en filetiket.
### Variable deskriptorposter
Posten indeholder en fast række af felter, der klassificerer typen og navnet på variablen sammen med formateringsoplysninger, der bruges af SPSS. Hver variabelpost kan valgfrit indeholde en variabel etiket på op til 120 tegn og op til tre manglende værdispecifikationer.
### Værdietiketter
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Den første post, som er tag 3, har en sekvens af par af felter, hvor hvert par indeholder en værdi og den tilhørende værdilabel. Den anden post, som er tag 4, repræsenterer hvilke variable værdisættet/etiketter gælder for.
### Dokumenter
Single or multiple records with integer tag 6. Valgfri dokumentation. indeholder 80-tegns linjer.
### Udvidelsesregistreringer
Single or multiple records with integer tag 7. Udvidelsesregistreringer giver information, som sikkert kan ignoreres, men som i mange situationer bevares, gør det muligt for filer skrevet af nyere software at bevare bagudkompatibilitet. Udvidelsesposter har heltals undertype-tags.
### Ordbogsterminator
Only record with integer tag 999. Den adskiller ordbog fra dataobservationer.
### Dataobservationer
Det betragtes som data er i observationsrækkefølge, f.eks. alle variable værdier for den første observation, efterfulgt af alle værdier for den anden observation osv. Formatet på dataposten varierer afhængigt af komprimeringskoden i filheaderposten. Datadelen af en .sav-fil kan være ukomprimeret:
- **kode 0**: komprimeret af bytekode
- **kode 1**: komprimeret ved hjælp af ZLIB-komprimering
 






## Referencer ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


