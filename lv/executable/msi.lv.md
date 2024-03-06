{
  "date": "2021-06-30",
  "keywords": [
"msi failu",
"MSI faila formāts",
"kas ir msi fails",
"failu",
"msi piemērs",
"msi faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MSI failu formātu un API, kas var izveidot un atvērt MSI failus.",
  "title": "MSI — Windows Installer pakotnes fails",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-lvi"
}
},
  "lastmod": "2021-06-30"
}

## Kas ir MSI fails?
MSI fails, ko izmanto Windows programmu instalēšanai un palaišanai; pilnīga Microsoft Windows pakotne, kurā ir ietverta tipiskas programmatūras programmas instalēšanas informācija, tostarp svarīgi instalējamie faili un informācija par instalēšanas vietu. MSI failos var būt arī programmatūras atjauninājumu pakotne. MSI faili ir līdzīgi [EXE](/executable/exe/), taču EXE dažkārt var neiekļaut instalēšanas informāciju un programmatūra var darboties tieši, izpildot EXE failu.

## MSI faila formāts
Windows Installer faktiski ir API (lietojumprogrammu saskarne) un Microsoft Windows programmatūras komponents, ko izmanto programmatūras programmas instalēšanai, noņemšanai un apkopei. Instalācijas informācija un neobligātie faili tiek iesaiņoti kā instalācijas pakotnes un brīvi relāciju datu bāzes, kas strukturētas kā COM strukturētās krātuves; labi pazīstami kā **MSI faili**, kam ir .msi faila paplašinājums. Pakotnēs ar faila paplašinājumu **.mst** ir ietverti Windows Installer **Transformation Scripts**, faili ar paplašinājumu **.msm** satur **Merge Modules** un faila paplašinājumu **.pcp**. tiek izmantots **Patch Creation Properties**. Programma Windows Installer kļūst modernāka pēc būtiskām izmaiņām salīdzinājumā ar iepriekšējām versijām Setup API. GUI ietvars un automātiska atinstalēšanas secības ģenerēšana ir Windows Installer jaunie līdzekļi. Tagad tas tiek uzskatīts par alternatīvu atsevišķiem izpildāmo instalēšanas programmu ietvariem.

### MSI pakotņu loģiskā struktūra
Pakete apzīmē viena vai vairāku pilnu produktu uzstādīšanu, un to parasti identificē ar **GUID**. Produkts sastāv no viena vai vairākiem komponentiem un ir sagrupēts dažādās funkcijās. Windows Installer neapstrādā dažādu produktu atkarības vienlaikus. Pakešu loģiskā struktūra sastāv no šādiem elementiem:

- **Produkti**: viena, instalēta, darba programma vai vairāku programmu kopa, kas apvienota kopā, ir produkts. Produkts tiek identificēts ar unikālu GUID.
- **Funkcijas**: var saturēt neierobežotu skaitu komponentu un citu apakšfunkciju. Mazāki iepakojumi var sastāvēt no vienas funkcijas.
- **Komponenti**: Windows Installer komponentu apstrādā kā vienību; var saturēt programmu failus, mapes, reģistra atslēgas, COM komponentus un īsceļus.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## Atsauces 

* [Windows Installer — Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)



