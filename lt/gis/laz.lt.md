{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAZ – suspaustas LIDAR duomenų mainų failas",
  "description": "Sužinokite apie LAZ failo formatą ir API, kurios gali kurti ir atidaryti LAZ failus.",
  "linktitle": "LAZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-ltz"
}
},
  "lastmod": "2023-07-18"
}

## Kas yra LAZ failas?

LAZ failo formatas yra suglaudinta LAS (Lidar LASer) failo formato versija, kuri yra specialiai sukurta Lidar taško debesies duomenims saugoti. LAZ failai išsaugo tuos pačius duomenis ir struktūrą kaip ir LAS failai, tačiau naudoja be nuostolių glaudinimo metodus, kad sumažintų failo dydį ir išsaugotų pradinių duomenų tikslumą.

## LAZ failo formatas – trumpa istorija

LAZ failo formatas buvo sukurtas siekiant patenkinti didėjantį didelių lidar duomenų rinkinių efektyvaus saugojimo ir perdavimo poreikį. Suglaudinus LAS failus, LAZ failai žymiai sumažina jų dydį, todėl juos lengviau valdyti ir perkelti. Suspaudimas pasiekiamas naudojant skirtingų algoritmų, tokių kaip entropijos kodavimas ir kintamo ilgio kodavimas, derinį, kad būtų galima pateikti kompaktiškesnę Lidar taško atributiką.

## LAZ failo formatas

Nepaisant suspaudimo, LAZ failai išlaiko galimybę visiškai atkurti pradinius LAS duomenis neprarandant informacijos. Tai reiškia, kad išskleidus LAZ failą, jį galima apdoroti ir analizuoti taip pat, kaip ir nesuspaustą LAS failą. Suspaudimo ir išskleidimo procesas paprastai atliekamas naudojant specializuotą programinę įrangą arba bibliotekas, kurios palaiko LAZ formatą.

LAZ failo formatas palaiko suderinamumą su LAS failais, užtikrindamas lidar programinės įrangos ir apdorojimo įrankių sąveiką. Tai reiškia, kad programos, galinčios skaityti ir apdoroti LAS failus, paprastai gali apdoroti LAZ failus be jokių pakeitimų. Be to, LAZ failuose vis dar yra failo antraštė, kintamo ilgio įrašai (VLR) ir taškų duomenų įrašai, išsaugant tą pačią struktūrą kaip ir LAS failai.

## LAZ failo formato privalumai

**Sumažintas failo dydis:** LAZ glaudinimas žymiai sumažina Lidar duomenų rinkinių failo dydį, todėl juos lengviau valdyti ir lengviau saugoti bei perkelti.

**Duomenų vientisumas:** LAZ glaudinimas yra be nuostolių, o tai reiškia, kad išspausti duomenys yra tiksli originalių LAS duomenų kopija, todėl neprarandama informacija ar tikslumas.

**Sąveika:** LAZ failai yra suderinami su LAS failais, todėl juos galima sklandžiai integruoti su esama Lidar programine įranga ir darbo eigomis.

**Efektyvus apdorojimas:** dėl mažesnio dydžio LAZ failus galima įkelti ir apdoroti greičiau, todėl pailgėja bendras apdorojimo ir analizės laikas.

LAZ failo formatas tapo plačiai naudojamas lidar bendruomenėje kaip suspaustų lidar duomenų saugojimo ir mainų standartas. Tai suteikia veiksmingo duomenų glaudinimo ir duomenų vientisumo pusiausvyrą, leidžiančią lengviau tvarkyti didelius Lidar duomenų rinkinius, išlaikant pradinių duomenų tikslumą ir kokybę.

## Nuorodos

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
