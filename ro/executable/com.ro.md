{
  "date" : "2021-06-29",
  "keywords" :[ "fișier com", "ce este un fișier com", "fișier", "exemplu com", "extensie fișier com", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier COM și despre API-urile care pot crea și deschide fișiere COM.",
  "title" :"COM - Format fișier de comandă DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier COM?
Fișierele COM sunt folosite pur și simplu pentru executarea unui set de comenzi sau instrucțiuni. Un fișier COM constă dintr-un program executabil care poate fi rulat din Windows sau MS-DOS. La fel și un fișier EXE, fișierul COM este salvat și în format binar, dar este diferit de fișierul EXE deoarece nu are antet sau metadate și, de asemenea, are dimensiunea maximă de aproximativ 64KB. Când fișierul COM rulează pentru prima dată pe un sistem pe 32 de biți, acesta vă solicită să instalați componenta NT Virtual DOS Machine (NTVDM). Fișierul COM poate fi rulat pe versiunea pe 64 de biți a Microsoft Windows cu o mașină virtuală care acceptă mediul MS-DOS.

## Format de fișier COM
Formatul de fișier COM este un format binar executabil utilizat în Microsoft Windows sau MS-DOS. Structura sa constă doar dintr-un set de instrucțiuni; nu are antet și nu conține metadate standard. Acesta stochează toate datele și codul într-un singur segment, iar binarul său are o dimensiune de maxim 64KB. Acest format de fișier nu se relocește atunci când încercați să rulați din nou. Deci sistemul de operare îl încarcă la o adresă prestabilită. Mai mult, este posibil să faci un fișier COM care să fie executat sub ambele sisteme de operare sub forma unui **binar gras**. Nu există nicio compatibilitate reală la nivel de instruire. Instrucțiunile de la punctul de intrare sunt selectate pentru a fi egale ca funcționalitate, dar diferite în ambele sisteme de operare și fac ca programul să ruleze să sară la secțiunea sistemului de operare în uz. Practic este vorba de două programe diferite cu aceeași procedură într-un singur fișier, precedate de codul de selectare a celui de utilizat.
### Exemplu de fișier COM
La executarea unui fișier COM, instrucțiunile sunt citite din primul octet și sunt urmate consecutiv până când sunt găsite ultimele instrucțiuni. Iată un exemplu de cod ASM:

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

## Referințe

* [Fișier COM - de Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

