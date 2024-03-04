{
  "date": "2021-02-10",
  "keywords": [
"jpx failą",
"jpx failo formatas",
"kas yra jpx failas",
"failą",
"jpx pavyzdys",
"jpx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPX – vaizdo failo formatas",
  "description": "Sužinokite apie JPX failo formatą ir API, kurios gali kurti ir atidaryti JPX failus.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-ltx"
}
},
  "lastmod": "2021-02-10"
}

## Kas yra JPX failas? ##

Failas su plėtiniu .jpx yra JPEG 2000 failo formato plėtinys. Jame visų pirma naudojamas JPEG 2000 glaudinimas, taip pat yra pažangių funkcijų, tokių kaip keli vaizdo sluoksniai, įvairios spalvų erdvės, neskaidrumas ir suskaidyti kodo srautai. Be JPEG 2000 glaudinimo JPX taip pat leidžia kitus suspaudimus, tokius kaip JBIG, CCITT Group3, CCITT Group4 ir kt. JPX failo formatas buvo patvirtintas kaip [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standartas, bet negalėjo sulaukti šilto priėmimo dėl plačiai naudojamo [JPEG](/image/jpeg/) failo formato. Programos, kurios gali atidaryti JPX failus, yra Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 ir CorelDraw Graphics Suite 2020.

## Trumpa istorija

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. 2004 m. ISO/IEC 15444-2 formatas buvo viešai priimtas kaip JP2 failo formato plėtinys.

## JPX failo formatas

JPX failo formatas buvo suformuluotas taip, kad atitiktų taikomųjų programų, kurioms reikia duomenų struktūrų, viršijančių funkcijas, apibrėžtas failo formatu [JP2](/image/jp2/), reikalavimus. JP2 failas su nesuderinamais plėtiniais gali sukelti painiavą rinkoje, nes kai kurie skaitytojai gali interpretuoti kai kuriuos JP2 failus, bet ne kitus. JPX yra atsakymas, kaip išvengti tokių problemų programose.

### Failo identifikavimas

JPX failai saugomi kaip [JPF](/image/jpf/), kai saugomi tradicinėje kompiuterio failų sistemoje. Štai kodėl JPX terminas yra rečiausiai naudojamas, palyginti su JPF. JPX failas prasideda šiais baitais:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Failų organizavimas

Panašiai kaip JP2, JPX failas yra dėžučių rinkinys, turintis dvejetainę struktūrą su dėžėmis, išdėstytomis gretima tvarka. Pirmasis langelis nurodo failo pradžią su pirmuoju baitu, o paskutinis paskutinio langelio baitas reiškia paskutinį failo baitą.
Dvejetainė laukelio struktūra JPX faile yra identiška apibrėžtai [JP2](/image/jp2/) failo formate.

### CodeStream saugojimas JPX formatu

JPX failo formatas leidžia padalyti vaizdo kodo srautą į fragmentus. Tai leidžia modifikuoti vieną vaizdo plytelę ir įrašyti pakeistą plytelę į failo pabaigą neperrašant viso failo. Originalus [JP2](/image/jp2/) failo formatas riboja, kad visas kodo srautas būtų saugomas gretimoje failo dalyje, o tai gali sukelti problemų vaizdų redagavimo programoms, kurios gali norėti modifikuoti vieną vaizdo plytelę ir pasiekti aukščiau nurodytą JPX palaikymą. Dokumento formatas. Dėl vaizdo kodų srauto suskaidymo JPX failo formatas yra pranašesnis už JP2 failo formatą. Be to, JPX failo formatas leidžia sujungti kelis kodų srautus ir gauti pateiktą rezultatą. Kodų srautus galima derinti kaip komponavimą ir animaciją.

## Nuorodos Nr.

* [JPEG 2000 apžvalga](https://jpeg.org/jpeg2000/)


