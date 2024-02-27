{
  "date": "2021-06-29",
  "keywords": [
"com fil",
"hvad er en com-fil",
"fil",
"com eksempel",
"com filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om COM-filformat og API'er, der kan oprette og åbne COM-filer.",
  "title": "COM - DOS Command File Format",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-dam"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er en COM fil?
COM-filerne bruges simpelthen til at udføre et sæt kommandoer eller instruktioner. En COM-fil består af et eksekverbart program, som kan køres fra Windows eller MS-DOS. Ligeledes er en EXE-fil, COM-filen gemmes også i binært format, men den er anderledes end EXE-fil, fordi den ikke har nogen header eller metadata, og den har også den maksimale størrelse på ca. 64KB. Når COM-filen kører første gang på et 32-bit system, bliver du bedt om at installere NT Virtual DOS Machine (NTVDM) komponenten. COM-filen kan køres på 64-bit versionen af Microsoft Windows med en virtuel maskine, der understøtter MS-DOS-miljøet.

## COM filformat
COM-filformatet er et binært eksekverbart format, der bruges i Microsoft Windows eller MS-DOS. Dens struktur består kun af et sæt instruktioner; den har ingen header og indeholder ingen standard metadata. Den gemmer kun alle sine data og kode i ét segment, og dens binære har maksimalt 64 KB i størrelse. Dette filformat flytter ikke sig selv, når det forsøges at køre igen. Så operativsystemet indlæser det på en forudindstillet adresse. Desuden er det muligt at lave en COM-fil til at køre under begge operativsystemer i form af en **fedt binær**. Der er ikke nogen egentlig kompatibilitet på instruktionsniveau. Instruktionerne ved indgangspunktet er valgt til at være ens i funktionalitet, men forskellige i begge operativsystemer, og gør programmet kørende, hop til den sektion af operativsystemet, der er i brug. Det er dybest set to forskellige programmer med den samme procedure i en enkelt fil, efterfulgt af kode, der vælger den, der skal bruges.
### Eksempel på COM-fil
Når du udfører en COM-fil, læses instruktionerne fra den første byte og følges fortløbende, indtil de sidste instruktioner er fundet. Her er et eksempel på ASM-kode:

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

## Referencer 

* [COM-fil - af Wikipewdia](https://en.wikipedia.org/wiki/COM_file)


