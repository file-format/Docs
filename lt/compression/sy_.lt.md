{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SY_ failo formatas – suspaustas SYS failas",
  "description": "Sužinokite apie SY_ failo formatą ir API, kurios gali kurti ir atidaryti SY_ failus.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-lt_"
}
},
  "lastmod": "2022-06-24"
}

## Kas yra SY_ failas?

SY_ failas yra suspaustas .sys failas, kurį programinės įrangos diegimo programos naudoja norėdami sumažinti diegimo failų, supakuotų į diegimo programą, dydį. Tai sumažina bendrą montuotojo dydį. SY_ failus galima išplėsti naudojant Microsoft Expand komandų eilutės įrankį, kuris išplečia vieną ar daugiau suspaustų failų.

## SY_ Failo formatas – daugiau informacijos

SY_ failai išsaugomi diske kaip suspausti dvejetainiai failai. Tačiau jų vidinis failo formatas nėra viešai prieinamas. Microsoft Expand komandų eilutės programa gali išplėsti SY_ failus naudodama vieną iš šių komandų eilučių.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Išplėtus SY_ failai konvertuojami į [SYS](/system/sys/) failą.

SY_ failai yra panašūs į EX_ ir DL_ failus.

## Nuorodos

 * [StuffIt – Vikipedija](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

