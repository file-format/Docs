{
  "date": "2021-08-17",
  "keywords": [
"udf failą",
"udf failo formatas",
"kas yra udf failas",
"failą",
"udf pavyzdys",
"udf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie UDF failo formatą ir API, kurios gali kurti ir atidaryti UDF failus.",
  "title": "UDF – universalaus disko formato failas",
  "linktitle": "UDF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ud-ltf"
}
},
  "lastmod": "2021-08-17"
}

## Kas yra UDF failas?
Failas su plėtiniu .udf yra disko vaizdo formatas, paprastai naudojamas failams įrašyti optinėje laikmenoje; gali būti naudojamas DVD, kompaktinių diskų ir kitų optinių laikmenų įrašymui; saugo failų rinkinį, naudodamas UDF standarte nurodytą katalogų struktūrą; leidžia ištrinti ir modifikuoti tiksliniame diske esančius failus net ir juos parašius. Optinio saugojimo technologijų asociacija nustatė UDF failų sistemą kaip standartą, kad būtų sudaryta bendra failų sistema visoms optinėms laikmenoms, pvz., perrašomai optinei laikmenai ir tik skaitomai laikmenai.

## UDF failo formatas 
UDF failo formatas yra atvira, pardavėjo atžvilgiu neutrali failų sistema, skirta kompiuteriniams duomenims saugoti įvairioms laikmenoms. Jis dažniausiai naudojamas DVD ir naujesniuose optinių diskų formatuose. Paprastai programinė įranga valdo UDF failų sistemą paketiniu procesu ir vienu praėjimu įrašo ją į optinę laikmeną. Tačiau, kai jis įrašo paketus į perrašomą laikmeną, UDF leidžia kurti, ištrinti ir keisti failus diske, panašiai kaip bendrosios paskirties failų sistema keičiamosiose laikmenose, pvz., flash drives arba diskeliuose.
### UDF specifikacijos
UDF standartas apibrėžia šiuos tris failų sistemos variantus:

- **Paprastas pastatymas**: tai originalus formatas, palaikomas visose UDF versijose. Jis buvo pristatytas pirmoje standarto versijoje, šis formatas gali būti naudojamas bet kokio tipo diskuose, kuriuose galima atsitiktine skaitymo arba rašymo prieiga, pvz., DVD+RW, standžiuosiuose diskuose ir DVD-RAM laikmenose.
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) versija**: naudojama specialiai rašant į perrašomą laikmeną. Ji prideda papildomą taupymo lentelę, kad būtų galima valdyti gedimus, kurie galiausiai atsiras tose disko dalyse, kurios buvo perrašytos kelis kartus. Ši lentelė išsaugo susidėvėjusius sektorius ir perskirsto juos į veikiančius. UDF defektų valdymas netaikomas sistemoms, kuriose jau įdiegta kita defektų valdymo forma, pvz., Mount Rainier (MRW) optiniams diskams arba disko valdiklis standžiajam diskui.
 



## Nuorodos 

* [Windows vaizdų formatas – pateikė Vikipedija](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



