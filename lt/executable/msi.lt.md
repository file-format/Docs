{
  "date": "2021-06-30",
  "keywords": [
"msi failą",
"MSI failo formatas",
"kas yra msi failas",
"failą",
"msi pavyzdys",
"msi failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MSI failo formatą ir API, kurios gali kurti ir atidaryti MSI failus.",
  "title": "MSI – „Windows Installer“ paketo failas",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-lti"
}
},
  "lastmod": "2021-06-30"
}

## Kas yra MSI failas?
MSI failas, naudojamas Windows programoms įdiegti ir paleisti; visas paketas, skirtas Microsoft Windows, kuriame yra tipinės programinės įrangos diegimo informacija, įskaitant esminius failus, kuriuos reikia įdiegti, ir informaciją apie diegimo vietą. MSI failuose taip pat gali būti programinės įrangos naujinimų paketas. MSI failai yra panašūs į [EXE](/executable/exe/), tačiau EXE kartais gali neįtraukti diegimo programos informacijos ir programinė įranga gali paleisti tiesiogiai, kai vykdomas EXE failas.

## MSI failo formatas
Windows Installer iš tikrųjų yra API (Application Programming Interface) ir Microsoft Windows programinės įrangos komponentas, naudojamas programinės įrangos programai įdiegti, pašalinti ir prižiūrėti. Diegimo informacija ir pasirenkami failai yra supakuoti kaip diegimo paketai ir laisvai reliacinės duomenų bazės, struktūrizuotos kaip COM struktūrinės saugyklos; gerai žinomi kaip **MSI failai**, turintys .msi failo plėtinį. Paketuose su failo plėtiniu **.mst** yra Windows Installer **Transformacijos scenarijai**, failuose su plėtiniu **.msm** yra **Sujungimo moduliai** ir failo plėtinys **.pcp** naudojamas **Pataiso kūrimo ypatybėms**. Windows Installer tampa pažangesnė po reikšmingų ankstesnių versijų – sąrankos API pakeitimų. GUI sistema ir automatinis diegimo pašalinimo sekos generavimas yra naujos Windows Installer funkcijos. Dabar tai buvo laikoma alternatyva atskiroms vykdomosioms diegimo programos sistemoms.

### Loginė MSI paketų struktūra
Paketas nurodo vieno ar kelių pilnų gaminių įdiegimą ir paprastai žymimas **GUID**. Produktas sudarytas iš vieno ar kelių komponentų ir sugrupuotas į įvairias funkcijas. Windows Installer vienu metu neapdoroja įvairių produktų priklausomybių. Loginė paketų struktūra susideda iš šių elementų:

- **Produktai**: viena, įdiegta, veikianti programa arba kelių programų rinkinys kartu yra produktas. Produktas identifikuojamas pagal unikalų GUID.
– **Funkcijos**: gali turėti bet kokį komponentų ir kitų papildomų funkcijų skaičių. Mažesnius paketus gali sudaryti viena funkcija.
- **Komponentai**: Windows Installer komponentą traktuoja kaip vienetą; gali būti programų failų, aplankų, registro raktų, COM komponentų ir nuorodų.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## Nuorodos 

* [Windows Installer – pateikė Vikipedija](https://en.wikipedia.org/wiki/Windows_Installer)



