{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS — Lidar LASer faila formāts",
  "description": "Uzziniet par LAS faila formātu un API, kas var izveidot un atvērt LAS failus.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-lvs"
}
},
  "lastmod": "2023-07-18"
}

## Kas ir LAS fails?

LAS (Lidar LASer) faila formāts ir binārais faila formāts, kas īpaši paredzēts lidara punktu mākoņa datu glabāšanai. To izstrādāja un uztur American Society for Photogrammetry and Remote Sensing (ASPRS) kā standartizētu formātu lidara datu apmaiņai un savietojamībai.

LAS faili glabā detalizētu informāciju par atsevišķiem lidara punktiem, tostarp to 3D koordinātas (x, y un z), intensitātes vērtības, klasifikācijas kodus un papildu atribūtus. Formāts atbalsta gan diskrētu atgriešanos, gan pilnas viļņu formas lidara datus, ļaujot saglabāt vairākas atdeves katram lāzera impulsam.

## LAS faila formāts

LAS faila struktūra sastāv no trim galvenajām sadaļām: faila galvenes, mainīga garuma ierakstiem (VLR) un punktu datu ierakstiem.

1. Faila galvene: faila galvenē ir ietverta būtiska informācija par LAS failu, piemēram, datu formāta versija, punkta datu formāts, punktu skaits, robežlodziņa koordinātas, koordinātu atsauces sistēma (CRS) un citi metadati. Tas nodrošina failā ietverto lidara datu kopsavilkumu.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Punktu datu ieraksti: punktu datu ieraksti saglabā faktiskos lidara mērījumus. Katrs punkta datu ieraksts attēlo vienu lidara punktu un satur tādus atribūtus kā x, y un z koordinātas, intensitātes vērtības, klasifikācijas kodus (piemēram, zeme, veģetācija, ēkas) un citus lietotāja definētus atribūtus. Punktu ierakstos var saglabāt arī laika zīmogus, atgriešanās skaitļus un skenēšanas leņķus.

LAS faili atbalsta dažādus datu formātus (no 0 līdz 10), lai pielāgotos dažāda veida lidar datiem un nepieciešamās informācijas līmenim. Piemēram, 0 formāts apzīmē vienkāršu punktu formātu ar pamatinformāciju, savukārt 1.–3. formāts nodrošina visaptverošākus datus, tostarp viļņu formas informāciju par katru atgriešanos.

LAS failus plaši atbalsta lidar programmatūra un apstrādes rīki, padarot tos par standarta formātu lidar datu apmaiņai un analīzei. Turklāt LAS failus var saspiest, izmantojot bezzudumu saspiešanas paņēmienus, lai samazinātu faila lielumu, vienlaikus saglabājot sākotnējo datu precizitāti. LAS failu saspiestā versija bieži tiek saukta par LAZ, kas piedāvā efektīvas uzglabāšanas un datu pārsūtīšanas iespējas.

## Atsauces

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
