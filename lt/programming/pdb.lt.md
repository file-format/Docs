{
  "date": "2019-10-11",
  "keywords": [
"pdb failą",
"pdb",
"pratęsimas",
"formatu",
"Kas yra pdb failas",
"pdb failo formatas",
"PBP metaduomenys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDB failo formatas – programos duomenų bazės failas",
  "description": "Sužinokite apie PDB failo formatą ir API, kurios gali kurti ir atidaryti PDB failus.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-ltb"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra PDB failas?

Failas su plėtiniu .pdb yra programos duomenų bazės failas, kuriame yra sukompiliuoto vykdomojo failo (EXE/DLL) derinimo informacija. PDB failus generuoja Microsoft kompiliatoriai, kai taikomoji programa kompiliuojama derinimo režimu. PDB failo buvimas gali padėti apgręžti vykdomąjį failą, nes jame yra svarbios informacijos apie visus modulių simbolius. Būtent dėl šios priežasties šie failai laikomi atskirai nuo galutinio vykdomojo failo. Microsoft [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) gali atidaryti PDB failą, kad gautų informaciją, pvz., viešuosius ir eksportuotus duomenis, visuotinius simbolius, vietinius simbolius, tipo duomenis, šaltinio failus ir eilučių numerius.

## PDB failo formatas

PDB yra Microsoft patentuotas failo formatas ir dar niekur nebuvo oficialiai dokumentuotas. Tačiau pradinė dokumentacija yra prieinama [here](https://github.com/Microsoft/microsoft-pdb) ir gali būti nurodyta.

### PBP srautai

PDB failus sudaro keli srautai, kur kiekvienas srautas veikia kaip virtualus atskiras failas ir jame yra informacijos. PDB failų kūrėjai gali rašyti į šiuos failus ir failas baigiamas tik tada, kai išduodamas aiškus įsipareigojimas. Kompiliatorius gali ir toliau rašyti į PDB failą, bet įsipareigoti tik tada, kai sėkmingai kompiliuojamas visas vartotojo kodas. PBP failą sudaro šie srautai:

|Srauto Nr. |Turinys |Trumpas aprašymas|
---|---|---|
|1| Pdb (antraštė) |Versijos informacija ir informacija, skirta prijungti šį PBP prie EXE|
|2| Tpi (tipo tvarkyklė) |Visi vykdomajame faile naudojami tipai.|
|3| Dbi (Debug information) |Turi skilties indėlius ir 'Modifikacijų' sąrašą|
|4| NameMap| Laiko maišos stygų lentelę|
|4-(n+4)| n Mod's (Modulio informacija)| Kiekviename Mod sraute yra simboliai ir eilučių numeriai vienam kompilandui|
|n+4| Pasaulinio simbolio maiša| Rodyklė, leidžianti ieškoti visuotiniuose simboliuose pagal pavadinimą|
|n+5| Viešojo simbolio maiša| Rodyklė, leidžianti ieškoti viešuose simboliuose pagal adresus|
|n+6| Simbolių įrašai| Tikrieji pasaulinių ir viešųjų simbolių simbolių įrašai|
|n+7| Įveskite maišą| TPI sraute naudojama maiša.|

Kiekvienas PBP failo srautas susideda iš kelių puslapių, kurie nebūtinai yra sunumeruoti iš eilės.

### PBP antraštė

PDB failas turi antraštę, kurią sudaro parašas, skirtas konkretaus formato identifikavimui ir patvirtinimui. Parašo ilgis priklauso nuo PBP formato. Antraštė gali būti ilgesnė nei vienas puslapis.

### PBP metaduomenys
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Taip pat yra nesutvarkytas šakninis srautas, kuriame yra kai kurie metaduomenys.

## Nuorodos
 * [PBP – Vikipedija](https://en.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

