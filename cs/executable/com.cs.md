{
  "date" : "2021-06-29",
  "keywords" :[ "soubor com", "co je soubor com", "soubor", "příklad com", "přípona souboru com", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru COM a rozhraních API, která mohou vytvářet a otevírat soubory COM.",
  "title" :"Formát souboru příkazů COM - DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor COM?
Soubory COM se jednoduše používají k provádění sady příkazů nebo instrukcí. Soubor COM se skládá ze spustitelného programu, který lze spustit ze systému Windows nebo MS-DOS. Stejně jako soubor EXE je soubor COM také uložen v binárním formátu, ale liší se od souboru EXE, protože nemá záhlaví ani metadata a také má maximální velikost přibližně 64 KB. Při prvním spuštění souboru COM na 32bitovém systému se zobrazí výzva k instalaci součásti NT Virtual DOS Machine (NTVDM). Soubor COM lze spustit v 64bitové verzi systému Microsoft Windows s virtuálním počítačem, který podporuje prostředí MS-DOS.

## Formát souboru COM
Formát souboru COM je binární spustitelný formát používaný v Microsoft Windows nebo MS-DOS. Jeho struktura se skládá pouze ze sady instrukcí; nemá žádné záhlaví a neobsahuje žádná standardní metadata. Ukládá všechna svá data a kód pouze do jednoho segmentu a jeho binární soubor má velikost maximálně 64 kB. Tento formát souboru se při pokusu o opětovné spuštění nepřemístí. Operační systém jej tedy načte na předem nastavenou adresu. Kromě toho je možné vytvořit soubor COM pro spuštění pod oběma operačními systémy ve formě **fat binary**. Na úrovni instrukcí neexistuje žádná skutečná kompatibilita. Instrukce ve vstupním bodě jsou vybrány tak, aby byly stejné ve funkčnosti, ale v obou operačních systémech se lišily, a aby program běžel, skočil do části používaného operačního systému. Jde v podstatě o dva různé programy se stejným postupem v jednom souboru, kterému předchází kód, který vybere ten, který se má použít.
### Příklad souboru COM
Při provádění souboru COM jsou instrukce čteny od prvního bajtu a jsou sledovány postupně, dokud nejsou nalezeny poslední instrukce. Zde je příklad kódu ASM:

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

## Reference

* [soubor COM – od Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

