{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FZPZ Fayl Format - Fritzing Part File",
  "description": "FZPZ faylının nə olduğunu və FZPZ fayllarını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-azz"
}
},
  "lastmod": "2022-06-20"
}

## FZPZ faylı nədir?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ Fayl Format - Ətraflı Məlumat

FZPZ faylları diskdə sıxılmış [ZIP](/compression/zip/) arxiv kimi saxlanılır. Siz genişləndirmənin adını .fzpz-dən .zip-ə dəyişdirə və faylları arxivdən çıxarmaq üçün WinZIP kimi istənilən standart dekompressiya yardım proqramından istifadə edə bilərsiniz.

### FZPZ Fayl Struktur Məlumatı

Qeyd edildiyi kimi, FZPZ faylı çap dövrə lövhəsində istifadə olunan hissənin təsviri üçün çoxsaylı faylları ehtiva edən arxiv faylıdır. FZPZ aşağıdakı faylları ehtiva edir:

 * `Dörd SVG faylı` - hissənin çörək lövhəsi, sxematik, PCB və ikon şəkillərini təmsil edir
 * `FZP faylı` - hissənin xassələri, birləşdiriciləri və avtobusları haqqında məlumatları ehtiva edən XML faylı

Fayllar adətən aşağıdakı kimi adlandırılır.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## İstinadlar ##

* [Fzpz uzantılı yeni hissələr](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


