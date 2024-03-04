{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DTSX failo formatą ir API, kurios gali kurti ir atidaryti DTSX failus.",
  "title": "DTSX failo formatas – SQL serverio DTS nustatymų failas",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-ltx"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra DTSX failas?

Failas su plėtiniu .dtsx (duomenų transformavimo paslaugų paketo XML) yra duomenų transformavimo paslaugų (DTS) failas, kurį naudoja Microsoft SQL, nurodydama duomenų perkėlimo veiksmus / taisykles, perkeliant duomenis iš vienos duomenų bazės į kitą. Tai apima transformacijas ir visus pasirenkamus apdorojimo veiksmus, kurių gali prireikti perduodant duomenis tarp pradinio ir paskirties taško. SQL Server Integration Services (SSIS), Microsoft SQL Server komponentas, naudoja DTSX failus, kad nustatytų duomenų apdorojimo tarp duomenų bazių serverių veiksmus. DTSX failus galima atidaryti naudojant Microsoft SQL Server 2019.

## DTSX failo formatas

Duomenų judėjimui tarp duomenų bazių serverių reikalingos taisyklės ir apdorojimo veiksmai, užtikrinantys duomenų vientisumą šios operacijos metu. SSIS užtikrina, kad visos šios veiklos, skirtos duomenims iš įvairių šaltinių perkelti ir suderinti įmonėje, vyktų patogiai. Štai čia atsiranda DTSX, kuris apibrėžia struktūras, kurias turi naudoti SSIS, kad nustatytų veiksmus, kurių metu duomenys gali būti tvarkomi, kaip tai daroma atliekant šiuos veiksmus.

DTSX aprašytas duomenų srautas yra toks, kaip parodyta kitame paveikslėlyje.

{{< figure src="../DataFlowDTSX.png" alt="Duomenų srautas DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## Nuorodos

 * [DTSX formatas – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2 formatas – pateikė Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

