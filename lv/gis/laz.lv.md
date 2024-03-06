{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAZ - saspiests LIDAR datu apmaiņas fails",
  "description": "Uzziniet par LAZ faila formātu un API, kas var izveidot un atvērt LAZ failus.",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-lvz"
}
},
  "lastmod": "2023-07-18"
}

## Kas ir LAZ fails?

LAZ faila formāts ir LAS (Lidar LASer) faila formāta saspiesta versija, kas īpaši paredzēta lidara punktu mākoņa datu glabāšanai. LAZ faili saglabā tādus pašus datus un struktūru kā LAS faili, bet izmanto bezzudumu saspiešanas paņēmienus, lai samazinātu faila lielumu, vienlaikus saglabājot sākotnējo datu precizitāti.

## LAZ faila formāts — īsa vēsture

LAZ faila formāts tika izstrādāts, lai apmierinātu pieaugošo pieprasījumu pēc efektīvas lielu lidar datu kopu uzglabāšanas un pārsūtīšanas. Saspiežot LAS failus, LAZ faili ievērojami samazina to lielumu, padarot tos vieglāk pārvaldāmus un pārsūtot. Saspiešana tiek panākta, izmantojot dažādu algoritmu kombināciju, piemēram, entropijas kodēšanu un mainīga garuma kodēšanu, lai attēlotu lidara punkta atribūtus kompaktākā formā.

## LAZ faila formāts

Neskatoties uz saspiešanu, LAZ faili saglabā iespēju pilnībā atjaunot sākotnējos LAS datus, nezaudējot informāciju. Tas nozīmē, ka pēc LAZ faila atspiešanas to var apstrādāt un analizēt tāpat kā nesaspiestu LAS failu. Saspiešanas un dekompresijas process parasti tiek veikts, izmantojot specializētu programmatūru vai bibliotēkas, kas atbalsta LAZ formātu.

LAZ faila formāts saglabā savietojamību ar LAS failiem, nodrošinot lidar programmatūras un apstrādes rīku savietojamību. Tas nozīmē, ka lietojumprogrammas, kas var lasīt un apstrādāt LAS failus, parasti var apstrādāt LAZ failus bez jebkādām izmaiņām. Turklāt LAZ faili joprojām ietver faila galvenes, mainīga garuma ierakstus (VLR) un punktu datu ierakstus, saglabājot tādu pašu struktūru kā LAS failiem.

## LAZ faila formāta priekšrocības

**Samazināts faila lielums:** LAZ saspiešana ievērojami samazina Lidar datu kopu faila lielumu, padarot tās vieglāk pārvaldāmas un vieglāk uzglabājamas un pārsūtāmas.

**Datu integritāte:** LAZ saspiešana notiek bez zudumiem, kas nozīmē, ka atspiestie dati ir precīza oriģinālo LAS datu kopija, kas nodrošina informācijas vai precizitātes zudumu.

**Sadarbspēja:** LAZ faili ir saderīgi ar LAS failiem, kas nodrošina nemanāmu integrāciju ar esošo lidar programmatūru un darbplūsmām.

**Efektīva apstrāde:** samazinātā izmēra dēļ LAZ failus var ielādēt un apstrādāt ātrāk, tādējādi uzlabojot kopējo apstrādes un analīzes laiku.

LAZ faila formāts ir kļuvis plaši izmantots lidar kopienā kā standarts saspiestu lidara datu glabāšanai un apmaiņai. Tas nodrošina līdzsvaru starp efektīvu datu saspiešanu un datu integritāti, ļaujot vieglāk apstrādāt lielas Lidar datu kopas, vienlaikus saglabājot sākotnējo datu precizitāti un kvalitāti.

## Atsauces

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
