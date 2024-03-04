{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS – Lidar LASer failo formatas",
  "description": "Sužinokite apie LAS failo formatą ir API, kurios gali kurti ir atidaryti LAS failus.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-lts"
}
},
  "lastmod": "2023-07-18"
}

## Kas yra LAS failas?

LAS (Lidar LASer) failo formatas yra dvejetainis failo formatas, specialiai sukurtas Lidar taško debesies duomenims saugoti. Jį sukūrė ir prižiūri Amerikos fotogrammetrijos ir nuotolinio stebėjimo draugija (ASPRS), kaip standartizuotą lidar duomenų mainų ir sąveikumo formatą.

LAS failuose saugoma išsami informacija apie atskirus lidaro taškus, įskaitant jų 3D koordinates (x, y ir z), intensyvumo reikšmes, klasifikavimo kodus ir papildomus atributus. Formatas palaiko ir diskrečią grąžą, ir visos bangos formos lidar duomenis, leidžiančius saugoti kelis vieno lazerio impulso grąžinimus.

## LAS failo formatas

LAS failo struktūra susideda iš trijų pagrindinių skyrių: failo antraštės, kintamo ilgio įrašų (VLR) ir taškinių duomenų įrašų.

1. Failo antraštė: Failo antraštėje yra pagrindinė informacija apie LAS failą, pvz., duomenų formato versija, taško duomenų formatas, taškų skaičius, ribojamojo langelio koordinatės, koordinačių atskaitos sistema (CRS) ir kiti metaduomenys. Jame pateikiama faile esančių lidar duomenų santrauka.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Taškinių duomenų įrašai: taško duomenų įrašuose saugomi faktiniai lidaro matavimai. Kiekvienas taško duomenų įrašas reiškia vieną lidaro tašką ir jame yra atributų, tokių kaip x, y ir z koordinatės, intensyvumo reikšmės, klasifikavimo kodai (pvz., žemė, augmenija, pastatai) ir kiti vartotojo nustatyti atributai. Taškų įrašuose taip pat gali būti saugomos laiko žymos, grąžinimo skaičiai ir nuskaitymo kampai.

LAS failai palaiko skirtingus duomenų formatus (nuo 0 iki 10), kad būtų galima pritaikyti įvairių tipų lidar duomenis ir reikalingą informacijos lygį. Pavyzdžiui, 0 formatas reiškia paprastą taško formatą su pagrindine informacija, o formatai nuo 1 iki 3 pateikia išsamesnius duomenis, įskaitant bangos formos informaciją apie kiekvieną grąžinimą.

LAS failus plačiai palaiko lidar programinė įranga ir apdorojimo įrankiai, todėl jie yra standartinis lidar duomenų mainų ir analizės formatas. Be to, LAS failus galima suglaudinti naudojant be nuostolių glaudinimo metodus, kad būtų sumažintas failo dydis, išsaugant originalų duomenų tikslumą. Suspausta LAS failų versija dažnai vadinama LAZ, kuri siūlo efektyvias saugojimo ir duomenų perdavimo galimybes.

## Nuorodos

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
