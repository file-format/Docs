{
  "date": "2021-06-29",
  "keywords": [
"com failą",
"kas yra com failas",
"failą",
"com pavyzdys",
"com failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie COM failo formatą ir API, kurios gali kurti ir atidaryti COM failus.",
  "title": "COM – DOS komandos failo formatas",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-ltm"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra COM failas?
COM failai tiesiog naudojami komandų ar instrukcijų rinkiniui vykdyti. COM failą sudaro vykdomoji programa, kurią galima paleisti iš Windows arba MS-DOS. Panašiai kaip EXE failas, COM failas taip pat išsaugomas dvejetainiu formatu, tačiau jis skiriasi nuo EXE failo, nes neturi antraštės ar metaduomenų, be to, jo maksimalus dydis yra maždaug 64 KB. Kai COM failas pirmą kartą paleidžiamas 32 bitų sistemoje, jis ragina įdiegti NT virtualiosios DOS mašinos (NTVDM) komponentą. COM failą galima paleisti 64 bitų Microsoft Windows versijoje su virtualia mašina, kuri palaiko MS-DOS aplinką.

## COM failo formatas
COM failo formatas yra dvejetainis vykdomasis formatas, naudojamas Microsoft Windows arba MS-DOS. Jo struktūrą sudaro tik instrukcijų rinkinys; jame nėra antraštės ir standartinių metaduomenų. Jis saugo visus savo duomenis ir kodą tik viename segmente, o jo dvejetainis dydis yra ne didesnis kaip 64 KB. Šis failo formatas nekeičia savo vietos, kai bandoma paleisti iš naujo. Taigi operacinė sistema ją įkelia iš anksto nustatytu adresu. Be to, galima sukurti COM failą, kuris būtų vykdomas abiejose operacinėse sistemose **riebaus dvejetainio formato** forma. Instrukcijų lygiu nėra jokio tikro suderinamumo. Instrukcijos įėjimo taške parenkamos taip, kad būtų vienodos funkcionalumo, bet skirtingos abiejose operacinėse sistemose, todėl programa veikia, pereina į naudojamos operacinės sistemos skyrių. Iš esmės tai yra dvi skirtingos programos su ta pačia procedūra viename faile, prieš tai pasirenkamas naudojamas kodas.
### COM failo pavyzdys
Vykdant COM failą, instrukcijos nuskaitomos nuo pirmojo baito ir vykdomos iš eilės, kol randamos paskutinės instrukcijos. Štai ASM kodo pavyzdys:

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

## Nuorodos 

* [COM failas – pateikė Wikipewdia](https://en.wikipedia.org/wiki/COM_file)


