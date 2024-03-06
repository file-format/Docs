{
  "date": "2019-10-11",
  "keywords": [
"dcm failu",
"dcm faila formātā",
"kas ir dcm fails",
"failu",
"dcm piemērs",
"dcm faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DCM faila formāts — digitālās medicīniskās informācijas fails",
  "description": "Uzziniet par DCM failu formātu un API, kas var izveidot un atvērt DCM failus.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-lvm"
}
},
  "lastmod": "2021-07-03"
}

## Kas ir DCM fails?

Faili ar paplašinājumu .dcm ir digitālais attēls, kurā tiek saglabāta pacientu medicīniskā informācija, piemēram, MRI, CT skenēšana un ultraskaņas attēli. DCM failos tiek izmantots attēla faila formāts [DICOM](/image/dicom/) (digitālā attēlveidošana un sakari medicīnā), un tajos uzziņai var būt iekļauta pacienta informācija. To izstrādāja [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA), un tas bija paredzēts, lai standartizētu attēlveidošanas faila formātu medicīnisko attēlu izplatīšanai un skatīšanai.

## DCM faila formāts

DCM faili saglabā informāciju DICOM attēla formātā. Šajos failos tiek glabāta datu kopa, kas ir reālās pasaules informācija, kas atspoguļo SOP gadījumu, kas saistīts ar DICOM IOD. DICOM faila metainformācija tiek saglabāta failā, kam seko faktiskās datu kopas baitu plūsma.

### DICOM faila metainformācija ##

Katrā DICOM failā ir ietverta iekapsulētās datu kopas identifikācijas informācijas galvene, kas sastāv no:
   * 128 baitu faila preambula
   * 4 baitu DICOM prefikss
   * Failu meta elementi

Šī galvene ir obligāta katram DICOM failam.

### Faila metaelementi ###
|Atribūta nosaukums|Taga|Veids| Atribūta apraksts
---|---|---|---|
|Faila preambula|Nav tagu vai garuma lauku|1|Pieejams fiksēts 128 baitu lauks lietojumprogrammas profila vai ieviešanas noteiktam lietojumam. Ja to neizmanto lietojumprogrammas profilā vai konkrētā implementācijā, visi baiti ir jāiestata uz 00H. Failu kopas lasītāji vai atjauninātāji nedrīkst paļauties uz šīs preambulas saturu, lai noteiktu, vai šis fails ir vai nav DICOM fails.
|DICOM prefikss|Nav tagu vai garuma lauku|1|Četri baiti, kas satur rakstzīmju virkni DICM. Šis prefikss ir paredzēts, lai atpazītu, vai šis fails ir vai nav DICOM fails.
|Faila metainformācijas grupas garums|(0002,0000)|1|Baitu skaits pēc šī faila meta elementa (vērtības lauka beigas) līdz pēdējam 2. grupas faila meta elementam ieskaitot, faila metainformācija
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Visi pārējie biti netiek pārbaudīti.
|Multivides krātuves SOP klases UID|(0002,0002)|1|Unikāli identificē ar datu kopu saistīto SOP klasi. Multivides glabāšanai atļautie SOP klases UID ir norādīti PS3.4 — multivides krātuves lietojumprogrammu profili.
|Multivides krātuves SOP instances UID|(0002,0003)|1|Unikāli identificē SOP gadījumu, kas saistīts ar failā ievietoto datu kopu un seko faila metainformācijai.
|Pārsūtīšanas sintakse UID|(0002,0010)|1|Unikāli identificē pārsūtīšanas sintakse, kas tiek izmantota šīs datu kopas kodēšanai. Šī pārsūtīšanas sintakse neattiecas uz faila metainformāciju.
|Ieviešanas klase UID|(0002,0012)|1|Unikāli identificē implementāciju, kas uzrakstīja šo failu, un tā saturu. Tas nodrošina nepārprotamu ieviešanas veida identifikāciju, kas pēdējo reizi ierakstīja failu apmaiņas problēmu gadījumā.
|Ieviešanas versijas nosaukums|(0002,0013)|3|Identificē versiju ieviešanas klases UID (0002,0012), izmantojot līdz 16 repertuāra rakstzīmēm.
|Avota lietojumprogrammas entītijas nosaukums|(0002,0016)|3|DICOM lietojumprogrammas entītijas (AE) nosaukums AE, kas uzrakstīja šī faila saturu (vai pēdējo reizi to atjaunināja). Ja tas tiek izmantots, tas ļauj izsekot kļūdu avotu datu nesēju apmaiņas problēmu gadījumā.
|Privātās informācijas veidotāja UID|(0002,0100)|3|Privātās informācijas veidotāja UID (0002,0102).
|Privāta informācija|(0002,0102)|1C|Satur privātu informāciju, kas ievietota faila metainformācijā. Radītāju identificē ar (0002,0100). Nepieciešams, ja ir privātās informācijas veidotāja UID (0002,0100).

### Datu kopas iekapsulēšana ###

DICOM fails satur vienu datu kopu, kas apzīmē vienu SOP gadījumu, kas saistīts ar vienu SOP klasi. DICOM faila metainformācijas pārsūtīšanas sintakses UID nosaka datu kopas kodēšanai izmantoto pārsūtīšanas sintaksi.

### Atbalsts failu pārvaldības informācijai ###

Multivides formāta slānis nodrošina šādu failu pārvaldības informāciju, ja tas ir nepieciešams konkrētajam DICOM lietojumprogrammas profilam.

  * Faila satura īpašnieka identifikācija

  * Failu piekļuves statistika (piemēram, izveides datums un laiks)

  * Lietojumprogrammu failu piekļuves kontrole

  * Fiziskā datu nesēja piekļuves kontrole (piemēram, rakstīšanas aizsardzība)

## Atsauces Nr.
  * [DICOM standarts](https://www.dicomstandard.org/current/)
  * [DICOM faila formāts](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

