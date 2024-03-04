{
  "date": "2021-06-30",
  "keywords": [
"exe failą",
"exe failo formatas",
"kas yra exe failas",
"failą",
"exe pavyzdys",
"exe failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": ".exe failas yra „Microsoft Executable“ failas, paleistas „Windows“ OS. Sužinokite daugiau apie EXE failo formatą.",
  "title": "Kas yra vykdomasis EXE failas?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-lte"
}
},
  "lastmod": "2021-06-30"
}

## Kas yra EXE failas?

Žodis EXE yra **vykdomasis** trumpinys. .exe failas yra programa, kurią galima vykdyti Microsoft Windows operacinėje sistemoje. Programų kūrėjai savo programas, skirtas Windows OS, dažniausiai skelbia vykdomuoju formatu kaip exe failus. Tai standartinis failo formatas, skirtas programoms paleisti sistemoje Windows. **Setup.exe**, **Install.exe** ir **cmd.exe** yra keli įprasti ir gerai žinomi EXE failų pavadinimai.

## EXE failo formatas

MS-DOS kompiliatoriai buvo pristatyti su atminties modeliais, turinčiais 64K atminties apribojimą. Bendra koncepcija yra nustatyti skirtingus segmentų registrus x86 procesoriuje (CS, DS, ES, SS), kad jie būtų nukreipti į skirtingus arba tuos pačius segmentus, taip suteikiant įvairaus laipsnio prieigą prie atminties. Kai kurie specifiniai atminties modeliai buvo:

- **Tiny**: visos atminties prieigos yra 16 bitų (segmentų registrai nepakitę). Vietoj .EXE failo sukuriamas .COM failas.
- **Mažas**: visos atminties prieigos yra 16 bitų (segmentų registrai nepakitę).
- **Kompaktiškas**: duomenų adresai apima ir segmentą, ir poslinkį, perkraunant DS arba ES registrus prieigai ir leidžiant iki 1M duomenų. Prieigos prie kodo nekeičia CS registro, leidžia 64K kodo.
- **Vidutinis**: kodo adresai apima segmento adresą, CS įkėlimą iš naujo ir leidžiant iki 1 mln. kodo. Duomenų prieigos nekeičia DS ir ES registrų, todėl galima gauti 64 000 duomenų.
- **Didelis**: tiek kodo, tiek duomenų adresai yra (segmento, poslinkio) poros, visada įkeliami segmentų adresai. Visa 1M baito atminties vieta yra tiek kodui, tiek duomenims.
- **Didžiulis**: toks pat kaip ir didelis modelis, o kompiliatorius sugeneruoja papildomą aritmetiką, kad būtų galima pasiekti didesnius nei 64K masyvus.

Kurdami exe failą kūrėjai turi nuspręsti, kurį modelį pasirinkti.

### Nešiojamasis EXE failo formatas

Nešiojamame vykdomojo failo formate (PE) yra keletas informacinių antraščių, toliau pateikiamas antraščių sąrašas:

- **DOS antraštė**: MS-DOS antraštė užtikrina arba atgalinį suderinamumą, arba grakštų naujų failų tipų mažinimą.
- **PE antraštė**: 60 (0x3C) poslinkis nuo DOS antraštės pradžios yra rodyklė į PE failo antraštę
- **COFF antraštė**: COFF antraštėje yra informacijos, kuri yra naudinga vykdomajam failui, ir informacijos, naudingesnės objekto failui.
- **Neprivaloma PE antraštė**: PE pasirenkama antraštė atsiranda iškart po COFF antraštės, o kai kurie šaltiniai netgi rodo, kad dvi antraštės yra tos pačios struktūros dalis.
- **Skyrių lentelė**: iš karto po PE pasirenkamos antraštės randame skyrių lentelę. Skyrių lentelę sudaro IMAGE_SECTION_HEADER struktūrų masyvas.
- **Susiejami skyriai**: galima sutaupyti vietos atmintyje, susiejant bibliotekos kodą į daugiau nei vieną procesą.

## Ar galite paleisti EXE failą „Mac“?

Exe failai nenaudojami kaip vykdomieji failai Mac OS. Tačiau, jei norite paleisti exe failą Mac OS, galite naudoti šiuos metodus.

 1. **Wine** – Wine yra puikus sprendimas žmonėms, norintiems naudoti savo kompiuterio programas Mac sistemose. Tai akronimas, reiškiantis vynas nėra emuliatorius, reiškiantis. Wine sukuria tą pačią katalogų aplinką, kurią naudoja Microsoft, kad galėtumėte paleisti Windows programą naudodami ją.
 2. **Virtualios mašinos** – sukurkite Windows virtualią mašiną naudodami Parallel Desktop arba VM Virtual Box ir paleiskite programą virtualioje mašinoje.
 3. **Boot Camp** – Windows Boot Camp įdiegimas ir konfigūravimas Mac OS leidžia paleisti Windows OS Mac kompiuteryje.

## Nuorodos

* [.exe- pateikė Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly / Windows vykdomieji failai](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


