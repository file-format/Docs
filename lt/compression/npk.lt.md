{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NPK failo formatas",
  "description":"Sužinokite apie NPK failo formatą ir API, kurios gali kurti ir atidaryti NPK failus.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Kas yra NPK failas?

NPK failas yra programinės įrangos atnaujinimo paketo failas, naudojamas **MikroTik** maršruto parinktuvuose maršrutizatoriaus operacinei sistemai atnaujinti. Jis pateikiamas kaip suspaustas dvejetainis archyvas, kuris įkeliamas į maršrutizatorių, kad būtų galima įdiegti programinės įrangos naujinimus. NPK failuose esanti informacija apima tinklo informaciją, pvz., IP adresą ir IP paslaugą, jungčių informaciją (eterneto sąsajas ir nuoseklųjį prievadą), el. pašto sąranką, tilto konfigūraciją ir vietinį naudotojų valdymą.

## NPK failo formatas

NPK failai saugomi kaip suspaustas dvejetainis archyvas. Tai uždaras failo formatas, kurį naudoja tik patys MikroTik. Neketinama kurti RouterOS priedų per trečiąsias šalis. NPK failus tvarko pati MikroTik, o atnaujintas jų versijas galima atsisiųsti iš [MikroTik](https://mikrotik.com/download) svetainės atsisiuntimo skilčių.

Kai NPK failas įkeliamas į maršruto parinktuvą, maršruto parinktuvo OS neįsigalioja, nebent jis paleidžiamas iš naujo. Todėl norint atnaujinti maršrutizatoriaus OS, reikia iš naujo paleisti.

## Nuorodos

* [MikroTik – Router OS atnaujinimas](https://mikrotik.com/download)

* [Kaip sukurti NPK failus](https://forum.mikrotik.com/viewtopic.php?t=87126)


