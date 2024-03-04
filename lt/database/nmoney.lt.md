{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie NMONEY failo formatą ir API, kurios gali kurti ir atidaryti NMONEY failus.",
  "title": "NMONEY failas – Denaro paskyros failo formatas",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-lty"
}
},
  "lastmod": "2023-05-17"
}

## Kas yra NMONEY failas?

NMONEY failas yra finansinių duomenų saugojimo duomenų bazės failas, kuriame yra finansinių operacijų įrašai. Jį sukūrė Nickvision ir naudojo Nickvision Denaro programinėje įrangoje, kuri yra asmeninė finansinė programinė įranga. NOMONEY faile saugomi duomenys apima sąskaitos kredito ir debeto operacijų informaciją.

NOMONEY failus galima atidaryti naudojant [Github](https://github.com/NickvisionApps/Denaro) programą.

## Apie Denaro programinę įrangą

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Denaro siūlomos funkcijos

 * Tvarkykite kelias paskyras vienu metu naudodami populiariausią ir žinomiausią skirtukų sąsają
 * Filtruokite operacijas pagal tipą, grupę arba datą
 * Kartokite operacijas, pvz., sąskaitas, kurios atsiranda kiekvieną mėnesį
 * Perveskite pinigus iš vienos sąskaitos į kitą
 * Eksportuokite duomenis iš paskyros kaip CSV failą ir importuokite CSV, OFX arba QIF failą, kad įtrauktumėte operacijas į paskyrą

## Denaro failo formatas – daugiau informacijos

Denaro failai išsaugomi diske dvejetainiu failo formatu. Finansiniai duomenys saugomi kaip duomenų bazės failas **.SQLITE3** failo formatu. SQLITE yra lengvas SQL duomenų bazės failas, sukurtas naudojant SQLite programinę įrangą. Tai suteikia savarankišką duomenų bazės variklį, galintį teikti visapusiškas ir labai patikimas duomenų bazes. SQLite duomenų bazės failus galima naudoti norint dalytis turtingu turiniu tarp sistemų tiesiog keičiantis šiais failais tinkle. SQLite susiejimas egzistuoja tokioms programavimo kalboms kaip C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) ir daugeliui kitų.

## Nuorodos

 * [Nickvision](https://nickvision.org/)
 * [NIckVision – Github](https://github.com/NickvisionApps/Denaro)

