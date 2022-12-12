{
  "date" : "2021-06-29",
  "keywords" :[ "com fájl", "mi az a com fájl", "fájl", "com példa", "com fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a COM-fájlformátumról és az API-król, amelyek COM-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"COM - DOS parancsfájl formátum",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a COM fájl?
A COM fájlokat egyszerűen parancsok vagy utasítások végrehajtására használják. A COM-fájl egy végrehajtható programból áll, amely Windows vagy MS-DOS rendszerből futtatható. Hasonlóan az EXE fájlokhoz, a COM fájl is bináris formátumban kerül mentésre, de eltér az EXE fájltól, mivel nincs fejléce vagy metaadata, és a maximális mérete körülbelül 64 KB. Amikor a COM-fájl először fut 32 bites rendszeren, az NT Virtual DOS Machine (NTVDM) összetevő telepítését kéri. A COM-fájl a Microsoft Windows 64 bites verzióján futtatható olyan virtuális géppel, amely támogatja az MS-DOS környezetet.

## COM fájlformátum
A COM fájlformátum egy bináris futtatható formátum, amelyet a Microsoft Windows vagy az MS-DOS rendszerben használnak. Szerkezete csupán egy utasításkészletből áll; nincs fejléce és nem tartalmaz szabványos metaadatokat. Minden adatát és kódját csak egy szegmensben tárolja, a bináris fájl mérete pedig maximum 64 KB. Ez a fájlformátum nem helyezi át magát, amikor megpróbálja újra futtatni. Tehát az operációs rendszer egy előre beállított címre tölti be. Ezenkívül lehetőség van egy COM-fájl végrehajtására mindkét operációs rendszer alatt **fat bináris** formájában. Nincs tényleges kompatibilitás az utasítások szintjén. A belépési pont utasításai úgy vannak kiválasztva, hogy funkcionalitásukban azonosak, de mindkét operációs rendszerben eltérőek legyenek, és a program futását a használt operációs rendszer szakaszára ugorják. Ez alapvetően két különböző program, ugyanazzal az eljárással egyetlen fájlban, amelyet egy kód előz meg, amely kiválasztja a használni kívántat.
### COM fájl példa
COM-fájl végrehajtásakor az utasításokat a rendszer az első bájttól olvassa be, és folyamatosan követi az utolsó utasítás megtalálásáig. Itt van egy példa az ASM kódra:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Hivatkozások

* [COM-fájl – a Wikipewdia által](https://en.wikipedia.org/wiki/COM_file)

