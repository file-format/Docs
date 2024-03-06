{
  "date": "2020-11-11",
  "keywords": [
"NDF",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MDF failu formātu un API, kas var izveidot un atvērt NDF failus.",
  "title": "NDF faila formāts — SQL servera galvenā datu bāzes fails",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-lvf"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir NDF fails?

Fails ar paplašinājumu .ndf ir sekundārs datu bāzes fails, ko izmanto [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server), lai saglabātu lietotāja datus. NDF ir sekundārais krātuves fails, jo SQL serveris saglabā lietotāja norādītos datus primārajā krātuves failā, kas pazīstams kā [MDF](/database/mdf/). NDF datu fails nav obligāts un ir lietotāja definēts, lai pārvaldītu datu glabāšanu gadījumā, ja primārais MDF fails izmanto visu atvēlēto vietu. Tas parasti tiek glabāts atsevišķā diskā un var izplatīties uz vairākām atmiņas ierīcēm. MDF failu klātbūtne ir nepieciešama, lai atvērtu NDF failus.

## NDF faila formāts

NDF faila formāts neatšķiras no [MDF](/database/mdf/) un izmanto lapas kā datu glabāšanas pamatvienību. katra lapa sākas ar 96 baitu galveni, kas ietver:

 * Lapas ID
 * Struktūras veids
 * Ierakstu skaits lapās
 * Norādes uz iepriekšējo un nākamo lapu

### NDF failu struktūra

MDF failam ir šāda datu struktūra.

 * 0. lapa: galvene
 * 1. lapa: pirmais PFS
 * 2. lapa: Pirmā GAM
 * 3. lapa: pirmais SGAM
 * 4. lapa: Nelietots
 * 5. lapa: Nelietots
 * 6. lapa: pirmais DCM
 * 7. lapa: pirmais BCM

#### NDF faila galvene

Visu failu lappuses numurs 0 satur galvenes, kas glabā metadatus par failu.

#### Lapas brīva vieta (PFS)
PFS identificē piešķiršanas statusu un nosaka brīvās vietas daudzumu.

 * 1. bits: norāda, vai lapa ir piešķirta vai nav.
 * 2. bits: norāda, vai lapa ir no jaukta apjoma.
 * 3. bits: norāda, ka šī lapa ir IAM lapa.
 * 4. bits: norāda, ka šajā lapā ir spoku ieraksti
 * Biti no 5 līdz 7: apvienota trīs bitu vērtība, kas norāda lapas pilnību šādi:
   * 0: lapa ir tukša
   * 1: lapa ir pilna par 1–50%.
   * 2: lapa ir pilna par 51–80%.
   * 3: lapa ir pilna par 81–95%.
   * 4: lapa ir pilna par 96–100%.

## Datu faila lapa

Lapas SQL Server datu failā sākas no nulles (0) un palielinās secīgi. Katrs fails tiek atpazīts pēc unikāla faila ID numura. Faila ID un lapas numura pāris unikāli identificē lapu datubāzē. Piemērs, kas parāda lappušu numurus datu bāzē, ir tāds pats kā nākamajā attēlā.

{{< figure src="../ndf.png" alt="NDF datu bāzes faila formāts" >}}

Šajā piemērā ir parādīti lappušu numuri datu bāzē, kurā ir 4 MB primāro datu fails un 1 MB sekundāro datu fails.

## Atsauces

 * [Datu bāzes faili un failu grupas](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
 * [Datu bāzes atdalīšana un pievienošana — SQL serveris](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- versija 15)
 * [SQL servera datu faila anatomijas analīze](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

