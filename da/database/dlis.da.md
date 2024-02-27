{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om DLIS-filformat og API'er, der kan oprette og åbne DLIS-filer.",
  "title" : "DLIS-filformat - Brøndlogdatafil",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-da",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Hvad er en DLIS fil?

.dlis-filformatet er et standardfilformat til lagring og udveksling af brøndlogdata i olie- og gasindustrien. Formatet er udviklet af Loging Industry Data Standard (LIDS) udvalget, og det står for Digital Log Information Standard. Formatet er designet til at gemme brøndlogdata på en måde, der er nem at læse, skrive og udveksle mellem forskellige systemer.

DLIS-filer indeholder et sæt logiske poster, der beskriver brøndlogdataene og dets karakteristika, såsom typen af logdata (f.eks. resistivitet, gammastråle), måleenhederne og placeringen af dataene i brønden. De faktiske logdata gemmes i separate binære filer og refereres til af de logiske poster i DLIS-filen.

## Kort information om brøndlogdata

Brøndlogdata er en registrering af målinger taget i forskellige dybder i en brønd, typisk under boringsprocessen eller efter brønden er blevet boret. Disse målinger kan omfatte forskellige fysiske, kemiske og/eller geofysiske egenskaber af bjergarten og væskerne i brønden. Nogle eksempler på brøndlogdata inkluderer:

- Elektrisk resistivitet: et mål for stenens evne til at modstå strømmen af en elektrisk strøm
- Gammastråle: et mål for bjergartens naturlige radioaktivitet
- Porøsitet: et mål for mængden af åbne rum eller porer i klippen
- Sonic: et mål for den tid, det tager for en lydbølge at rejse gennem klippen
- Massefylde: et mål for massen af en sten pr. volumenenhed
- Litologi: et mål for bjergarten eller formationen

Brøndlogdata bruges til forskellige formål i olie- og gasindustrien, såsom:

- Identifikation af placering og kvalitet af kulbrinteførende formationer
- Evaluering af produktionspotentialet for en brønd
- Planlægning og overvågning af færdiggørelse og stimulering af en brønd
- Overvågning af brøndens adfærd over tid

## Relation til PPDM

PPDM (Professional Petroleum Data Management) er en datastyringsstandard for olie- og gasindustrien, der giver en fælles datamodel til styring af brønd- og produktionsdata. PPDM-datamodellen definerer et sæt standarddataobjekter og -relationer, der kan bruges til at organisere og administrere brøndlogdata, inklusive DLIS-data.

PPDM-datamodellen inkluderer dataobjekter for brønd- og produktionsdata, såsom brønde, brøndhoveder, brøndlogfiler og produktionsdata. Det inkluderer også relationer mellem disse dataobjekter, såsom forholdet mellem en brønd og de brøndlogfiler, der er knyttet til den.

PPDM-datamodellen giver en konsistent, industristandard måde at organisere og administrere brøndlogdata, herunder DLIS-data. Det giver forskellige organisationer mulighed for at dele og udveksle data ved hjælp af en fælles datamodel, hvilket forbedrer datainteroperabiliteten og reducerer omkostningerne til dataintegration.

Brug af PPDM-datamodel og DLIS-data sammen gør det muligt at gemme og administrere brøndlogdata på en måde, der er i overensstemmelse med industristandarder og let tilgængelig for andre systemer og applikationer.


