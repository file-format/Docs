{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"failą",
"pratęsimas",
"Dokumento formatas",
"Excel atidarykite XML makrokomandą",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra XLTM failas ir API, kurios gali juos sukurti ir atidaryti.",
  "title": "Kas yra XLTM failas?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-ltm"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra XLTM failas?

XLTM failo plėtinys reiškia failus, kuriuos Microsoft Excel sugeneruoja kaip makrokomandos įgalintus šablonų failus. XLTM failai yra panašūs į [XLTX](/spreadsheet/xltx/) savo struktūra, išskyrus tą, kuri vėliau nepalaiko šabloninių failų su makrokomandomis kūrimo. Tokie šablonų failai naudojami generuoti ir nustatyti išdėstymą, formatavimą ir kitus parametrus kartu su makrokomandomis, kad būtų lengviau sukurti panašius XLSX failus.

## Trumpa istorija ##

Tai buvo 2000 m. pradžioje, kai Microsoft nusprendė imtis pakeitimų, kad atitiktų **Office Open XML** standartą. Įvairių tipų dokumentai pagal šį naują standartą buvo identifikuoti prie jų plėtinių pridedant X, kur X reiškia XML. Iki 2007 m. šis naujas failo formatas tapo Office 2007 dalimi ir taikomas ir naujose Microsoft Office versijose. Naujasis failo tipas prideda mažų failų dydžių, mažesnių sugadinimo pakeitimų ir gerai suformatuotų vaizdų privalumų.

## XLTM failo formato specifikacijos ##

XLTM failai yra pagrįsti Office OpenXML failo formatu ir naudoja XML ir [ZIP](/compression/zip/), kad sumažintų failo dydį. Juos galima atidaryti naudojant Microsoft Excel, dukart spustelėjus failą. Failų organizavimą XLTM failo formatu galima stebėti pervadinus failą į ZIP ir ištraukus jo turinį į diską.

### [Content_Types].xml ###

Tai vienintelis failas, kuris randamas pagrindiniame lygyje, kai ištraukiamas ZIP failas. Jame pateikiami paketo dalių turinio tipai. Visos nuorodos į pakete esančius XML failus yra pateiktos šiame XML faile.

### \_rels (aplankas) ###

Tai aplankas Ryšiai, kuriame yra vienas XML failas, kuriame saugomi paketo lygio ryšiai. Nuorodos į pagrindines Xltx failų dalis yra šiame faile kaip URI. Šie URI nustato kiekvienos pagrindinės dalies ryšio su paketu tipą. Tai apima ryšį su pagrindiniu biuro dokumentu, esančiu kaip xl/workbook.xml, ir kitas docProps dalis kaip pagrindines ir išplėstines ypatybes.

### docProps ###

Šiame aplanke yra visos dokumento ypatybės. Tai apima pagrindinių ypatybių rinkinį, išplėstinių arba konkrečiai programai būdingų ypatybių rinkinį ir dokumento miniatiūros peržiūrą. Tuščioje darbaknygėje šiame aplanke yra du failai, ty app.xml ir core.xml. core.xml yra tokia informacija kaip autorius, sukūrimo, išsaugojimo ir modifikavimo data. App.xml yra informacijos apie failo turinį.

### xl (aplankas) ###

Tai pagrindinis aplankas, kuriame yra visa informacija apie darbaknygės turinį. Pagal numatytuosius nustatymus jame yra šie aplankai:

* \_rels

*tema

* darbalapiai


ir šiuos xml failus:

* styles.xml

* darbaknygė.xml


## Nuorodos Nr.

* [MS-XLSX failo formatas](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


