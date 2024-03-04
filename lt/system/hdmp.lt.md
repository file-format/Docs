{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDMP failas – „Windows Heap Dump“ failo formatas",
  "description": "Sužinokite apie HDMP failo formatą ir API, kurios gali kurti ir atidaryti HDMP failus.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-ltp"
}
},
  "lastmod": "2022-08-19"
}

## Kas yra HDMP failas?

HDMP failas yra nesuspaustas atminties iškrovimas, kai programa ar programa sugenda dėl klaidos. Ją sukūrė tik Windows XP / Vista ir jame yra programos būsenos iškraunama, kai ji sudužo. Nesuspausti HDMP failai užima daugiau vietos diske, palyginti su Minidump [MDMP](/system/mdmp/) failais, kurie suglaudinami ataskaitų teikimo tikslais.

Programos, kurias galima naudoti HDMP failams **atidaryti** arba analizuoti, apima Microsoft Visual Studio su derinimo įrankiais, skirtais Windows.

## HDMP failo formatas

HDMP failai saugomi diske kaip dvejetainiai failai ir neduoda jokios naudos, jei atidaromi be atitinkamų programų. Juose yra atitinkami sistemos duomenys, įrašyti įvykus klaidai.

### Skirtumas tarp HDMP ir MDMP failų formatų

HDMP yra nesuspausti atminties iškelties failai. Priešingai, MDMP yra mini iškelties failai, kurie suglaudinami siekiant sumažinti failo dydį ir siunčiami Microsoft, kad būtų pranešta apie problemą.

## Nuoroda ##

* [DMP – „Microsoft“](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


