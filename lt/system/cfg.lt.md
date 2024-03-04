{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"pratęsimas",
"failą",
"formatu",
"sistema",
"konfigūracija",
"nustatymus",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG – failo formatas",
  "description": "Sužinokite apie CFG failo formatą ir API, kurios gali kurti ir atidaryti CFG failus.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-ltg"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra CFG failas? ##

Failas su plėtiniu .cfg yra nustatymų failo tipas. Tai plačiai naudojamas failo tipas ir naudojamas informacijai apie kompiuterių programų konfigūraciją ir nustatymus saugoti. Dauguma CFG failų tipų yra saugomi teksto formatu ir neturėtų būti atidaromi rankiniu būdu, o juos reikia atidaryti naudojant teksto rengyklę. Tačiau yra įvairių tipų CFG failų, kurie skiriasi formatu, kuriuo saugoma informacija. Funkcijos, kurias siūlo CFG failai, įvairiose programose skiriasi. Kai kurios kompiuterių programos leidžia vartotojams keisti arba plėtoti savo konfigūracijos failų sintaksę naudojant grafinius trukdžius, o kitos leidžia modifikuoti tik naudojant teksto rengyklę. Pakeitę šiuos failus, vartotojai gali nurodyti programai dar kartą perskaityti šiuos failus ir pritaikyti pakeitimus sistemai.


## CFG failo formatas ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Formatas, kuriuo šie failai saugomi ir naudojami kiekvienoje iš šių operacinių sistemų, skiriasi. Dauguma sistemų naudoja ir saugo šiuos failus žmonėms skaitomu ir redaguojamu paprasto teksto formatu, o kitose saugomi sudėtingesnio formato failai, atsižvelgiant į failų naudojimą ir operacinės sistemos reikalavimus.

Unix ir Unix tipo operacinėse sistemose daugumoje CFG failų naudojami keli skirtingi CFG failų formatų stiliai, tačiau labiausiai paplitęs formatas yra lengvai skaitomas paprasto teksto formatas, o beveik visi formatai leidžia komentuoti ir redaguoti. Dažniausiai šiose operacinėse sistemose naudojami CFG failų plėtiniai yra CNF, CONF, CF ir INI.

MS-DOS operacinėje sistemoje iš pradžių buvo tik vienas konfigūracijos failo formatas, ty paprastas tekstas, tačiau MS-DOS 6 atnešė INI konfigūracijos failo formato įvedimą.

macOS naudoja standartinį ypatybių sąrašo formato stiliaus konfigūracijos failą.

Microsoft Windows sistemoje paprasto teksto INI stiliaus konfigūracijos failai buvo svarbus informacijos saugojimo ir redagavimo šaltinis, tačiau 1993 m. buvo pristatyta nauja duomenų bazių sistema, todėl po 1993 m. Microsoft Windows sumažėjo konfigūracijos failų naudojimas.


## CFG pavyzdys Nr.

CFG failo pavyzdį galite pamatyti žemiau:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Kiti CFG failai

Štai kiti failų tipai, kuriuose naudojamas **.cfg** failo plėtinys.

**Nustatymai**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Žaidimas**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistema ir kita**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

