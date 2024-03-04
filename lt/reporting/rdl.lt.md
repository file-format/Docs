{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL – ataskaitos apibrėžimo kalbos failas",
  "keywords": [
"rdl",
"ataskaitos apibrėžimo kalba",
"XmlTextWriter",
"XSD",
"RDL elementas"
],
  "description": "Sužinokite apie RDL failo formatą, kuris yra SQL serverio ataskaitų tarnybų ataskaitos apibrėžimo XML atvaizdas.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-ltl"
}
},
  "lastmod": "2021-03-01"
}

## Kas yra RDL failas? ##

RDL (ataskaitų apibrėžimo kalba) yra Microsoft nustatytas etalonas ataskaitoms apibrėžti. RDL failas susideda iš vieno ar kelių RDL elementų. Tuo tarpu RDL elementą sudaro jo duomenų tipas ir kardinalumas. Elementas gali būti paprastas arba sudėtingas. Paprastas elementas neturi antrinio elemento ar atributų, o sudėtingas elementas turi antrinius elementus ir pasirenkamus atributus.

## RDL XML schemos apibrėžimas
XML schemos apibrėžimo (XSD) failas patvirtina RDL failą. Schema apibrėžia taisykles, kur RDL elementai gali atsirasti .rdl faile. RDL elementas gali būti paprastas arba sudėtingas. Paprastas elementas neturi antrinių elementų ar atributų, o sudėtingas elementas turi antrinius elementus ir pasirinktinai atributus.

## RDL kūrimas
Kadangi RDL yra atviras ir išplečiamas, galima sukurti daugybę programų ir įrankių, kurie generuoja RDL failus pagal XML schemą. Vienas iš paprasčiausių būdų sukurti RDL iš programos yra naudoti Microsoft .NET Framework klases **System.Xml** vardų srityje ir System.Linq vardų srityje. Visų pirma, **XmlTextWriter** klasė gali būti naudojama RDL rašymui. Galite sugeneruoti visą ataskaitos apibrėžimą nuo pradžios iki pabaigos bet kurioje .NET Framework programoje naudodami **XmlTextWriter**. Kūrėjai taip pat gali pridėti pasirinktinių ataskaitos elementų su pasirinktinėmis savybėmis, kad išplėstų RDL.

## RDL tipai
Šioje lentelėje pateikiami RDL elementuose naudojami tipai ir atributai.

|Tipas|Aprašymas|
---|---|
|Dvejetainė |Ypatybė su 64 bazine koduota dvejetaine verte.|
|Bulio| Savybė, kurios objekto vertė yra teisinga arba klaidinga. Jei nenurodyta kitaip, praleisto pasirinktinio Būlio objekto reikšmė yra False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Ypatybė su eilutės teksto verte, kuri turi būti viena iš nurodytų reikšmių sąrašo.|
|Plaukiojantis |Nuosavybė su kintamąja verte. Taškas (.) naudojamas kaip pasirenkamas dešimtainis skyriklis.|
|Sveikasis skaičius |Ypatybė su sveikojo skaičiaus (int32) reikšme.|
|Language |Ypatybė su teksto verte, kurioje yra kalbos ir kultūros kodas, pvz., en-us JAV anglų kalba. Reikšmė turi būti konkreti kalba arba neutrali kalba, kurios numatytoji kalba yra apibrėžta Microsoft .NET Framework.|
|Pavadinimas |Ypatybė su eilutės teksto reikšme. Vardai turi būti unikalūs elemento vardų srityje. Jei nenurodyta, elemento vardų erdvė yra vidinėje dalyje esantis objektas, turintis pavadinimą.|
|NormalizedString |Ypatybė su eilutės teksto reikšme, kuri buvo normalizuota.|
|Dydis |Dydžio elemente turi būti skaičius (su taško ženklu, kuris naudojamas kaip pasirenkamas dešimtainis skyriklis). Po numerio turi būti nurodytas CSS ilgio vieneto žymuo, pvz., cm, mm, in, pt arba pc. Tarpas tarp skaičiaus ir žymens yra neprivalomas. Norėdami gauti daugiau informacijos apie dydžio žymeklius, žr. CSS reikšmių ir vienetų nuorodą. RDL didžiausia dydis yra 160 colių. Mažiausias dydis yra 0 colių.|
|Eilutė |Ypatybė su eilutės teksto reikšme.|
|UnsignedInt |Ypatybė su nepasižymėjusio sveikojo skaičiaus (uint32) reikšme.|
|Variantas |Savybė su bet kokiu paprastu XML tipu.|

## RDL duomenų tipai
RDL DataType Enumeration apibrėžia atributo, išraiškos arba parametro duomenų tipą. Šioje lentelėje parodyta, kaip CLR duomenų tipai atitinka RDL duomenų tipus.

|CLR tipas (-ai) |Atitinkamas duomenų tipas|
---|---|
|Bulio| Būlio|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Sveikasis skaičius|
|Vienvietis, Dvivietis |Plūdė|
|Eilutė, Char, GUID, Laiko intervalas |Eilutė|


## Nuorodos Nr.

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

