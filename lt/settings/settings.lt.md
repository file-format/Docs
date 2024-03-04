{
  "date": "2023-03-29",
  "keywords": [
"nustatymų failą",
"kas yra nustatymų failas",
"failą",
"nustatymų failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "NUSTATYMAI Failo formatas – „Visual Studio“ nustatymų failas",
  "description": "Sužinokite apie SETTINGS formatą ir API, kurios gali kurti ir atidaryti SETTINGS failus.",
  "linktitle": "SETTINGS",
  "menu": {
    "docs": {
      "identifier": "settings-settings-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-03-29"
}

## Kas yra SETTINGS failas?

Visual Studio .settings failas yra failas, kuriame yra programos parametrų ir kuris gali būti naudojamas konkretaus projekto ar sprendimo vartotojo nuostatoms ir konfigūracijos duomenims saugoti. Šie nustatymai gali apimti tokius dalykus kaip šrifto dydžiai, langų išdėstymas, numatytieji projekto nustatymai ir kitos konfigūracijos parinktys. Failą .settings paprastai sukuria automatiškai Visual Studio, kai sukuriamas projektas ir išsaugomas kataloge, pavadintame projekto aplanko ypatybės. Pats failas yra XML failas, kuriame yra elementų ir atributų rinkinys, apibrėžiantis įvairius projekto parametrus ir reikšmes.

Kūrėjai taip pat gali kurti pasirinktinius .settings failus projektams ir su jais susijusiems sprendimams, kurie gali būti naudojami papildomiems konfigūracijos duomenims, būdingiems jų programai, saugoti. Šiuos tinkintus .settings failus galima pasiekti ir modifikuoti naudojant Visual Studio IDE arba naudojant kodą naudojant ConfigurationManager klasę .NET. Visual Studio .settings failas yra svarbi IDE konfigūracijos sistemos dalis ir suteikia galimybę kūrėjams saugoti ir tvarkyti programų parametrus ir nuostatas projektuose.

## NUSTATYMAI Failo formatas – daugiau informacijos

The .settings file consists of several sections each containing one or more settings. Each setting is defined by a name and a value, including other attributes e.g. description or default value.

Viena iš pagrindinių .settings failo ypatybių yra ta, kad ji leidžia kūrėjams sukurti griežtai įvestus nustatymus, o tai reiškia, kad kiekvienas nustatymas turi konkretų duomenų tipą ir gali būti pasiekiamas bei manipuliuojamas naudojant kodą. Tai leidžia kūrėjams lengvai saugoti ir nuskaityti taikomųjų programų nustatymus, nereikalaujant rašyti sudėtingo kodo ar valdyti konfigūracijos failų rankiniu būdu.

Visual Studio teikia Settings Designer įrankį, leidžiantį kūrėjams kurti ir valdyti savo projektų nustatymus naudojant grafinę sąsają. Įrankis sugeneruoja reikalingą kodą nustatymams pasiekti ir keisti, todėl kūrėjai gali lengvai juos naudoti savo kode.

Be numatytojo .settings failo, kūrėjai taip pat gali kurti savo projektų tinkintus nustatymų failus. Šiuos failus galima naudoti papildomiems konfigūracijos duomenims, būdingiems jų programai, pvz., ryšio eilutėms, API raktams ar kitiems slaptiems duomenims saugoti. Norėdami apsaugoti šiuos duomenis, kūrėjai gali užšifruoti tinkintų nustatymų failus naudodami duomenų apsaugos API (DPAPI), kuri užtikrina, kad duomenys būtų saugūs, net jei failas yra pažeistas.

## Nuorodos
* [Visual Studio](https://en.wikipedia.org/wiki/Visual_Studio)


