
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML failas – „Microsoft Assistance“ žymėjimo kalbos failas",
  "description":"Sužinokite, kas yra AML failas ir API, kurios gali kurti ir atidaryti AML failus.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML – Microsoft pagalbos žymėjimo kalbos failas

## Kas yra AML failas?

AML (pagalbos žymėjimo kalbos) failas yra XML failas, sugeneruotas naudojant Microsoft Assistance Markup Language (MAML). Ją sukūrė Microsoft, siekdama teikti internetinę Microsoft Windows OS pagalbą. Prieš tai Windows žinynas buvo pasiekiamas sukompiliuotu HTML [CHM](/web/chm/) failo formatu. AML failai yra struktūrinis dokumentas, leidžiantis programai kurti šaltinio kodą ir pagalbinius pagalbos puslapius. Tai leidžia apibrėžti dokumentus ir jų sudedamąsias dalis pagal jų kontekstą. AML žinyno failai skelbiami internete ir gali būti sukonfigūruoti taip, kad būtų atnaujinami naudojant internete pasiekiamus paketo naujinimus.

## MAML failo struktūra

AML failai, sukurti naudojant MAML, išsaugomi kaip [XML](/web/xml/) failai, kuriuos galima naudoti įvairioms aktyvioms sąvokoms išreikšti. Ji taip pat gali teikti vadovaujamą žinyną (aktyvų turinio vedlį), dėl kurio žinyno failas tampa interaktyvus vartotojui naudojant nuoseklų vedlį.

An AML file generated using the MAML follows its authoring structure that can be divided into segments like:

 * Konceptualus
 * DUK
 * Žodynėlis
 * Procedūra
 * Nuoroda
 * Daugkartinis turinys
 * Užduotis
 * Trikčių šalinimas ir
 * Pamoka

## Kaip sukurti MAML failus?

MAML failus galima sukurti vienu iš šių būdų:

 * Sandcastle naudojimas – pagalbos failui generuoti naudojamas schemų ir programos vykdomųjų failų rinkinys. Tačiau šis įrankis buvo nutrauktas.
 * DocProject naudojimas – Microsoft Visual Studio papildinys, kurį galima paleisti iš Microsoft Visual Studio žinyno turiniui generuoti.

MAML failus galima sukurti naudojant Sandcastle, .XSL schemų ir programų vykdomųjų failų rinkinį. Jie taip pat gali būti sukurti naudojant DocProject, Microsoft Visual Studio pagalbos kūrimo įrankio priedą.

## Nuorodos

 * [Sukurkite XML pagrįstą pagalbą naudodami PlatyPS](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
 * [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML – Arc Macro Language File

## Kas yra ARC Macro AML failas?

AML (ARC makro kalbos) failas yra scenarijų failas, sugeneruotas naudojant ArcInfo Workstation GIS programą. Ji parašyta ARC Macro Language, kuri yra patentuota aukšto lygio algoritminė kalba, skirta GIS programoms kurti ArcInfo. AML sukūrė ESRI 1986 m. ir buvo skirtas kurti programas iš komandinės eilutės ARCINFO GIS sistemos. Kaip scenarijų failas, AML failuose gali būti scenarijaus komandų, skirtų atlikti daugybę užduočių, pavyzdžiui, sukurti vartotojo sąsajos komponentus ir valdyti žemėlapio duomenis.

## AML failo formatas – daugiau informacijos

AML, kaip scenarijų failai, išsaugo informaciją į diską kaip paprasto teksto failus. Ji atitinka AML sintaksę, kuri buvo pagrįsta PRIMOS operacinės sistemos CPL apvalkalo kalba. AML kalba buvo pakeista ESRI geoprocesų sistema, kuri yra ArcGIS rinkinio dalis ir naudoja ArcObjects, kad teiktų programavimo palaikymą per VBA arba Python.

## Nuorodos

 * [ARC makro kalba](https://en.wikipedia.org/wiki/ARC_Macro_Language)
 * [AML naudojimas su scenarijaus įrankiais](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

