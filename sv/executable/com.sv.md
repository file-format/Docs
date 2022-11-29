{
  "date" : "2021-06-29",
  "keywords" :[ "com-fil", "vad är en com-fil", "fil", "com-exempel", "com-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om COM-filformat och API:er som kan skapa och öppna COM-filer.",
  "title" :"COM - DOS Command File Format",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är en COM-fil?
COM-filerna används helt enkelt för att utföra en uppsättning kommandon eller instruktioner. En COM-fil består av ett körbart program som kan köras från Windows eller MS-DOS. Likaså en EXE-fil, COM-filen sparas också i binärt format men den är annorlunda än EXE-fil eftersom den inte har någon rubrik eller metadata och den har också en maximal storlek på ungefär 64KB. När COM-filen körs första gången på ett 32-bitarssystem uppmanas den att installera komponenten NT Virtual DOS Machine (NTVDM). COM-filen kan köras på 64-bitarsversionen av Microsoft Windows med en virtuell maskin som stöder MS-DOS-miljön.

## COM filformat
COM-filformatet är ett binärt körbart format som används i Microsoft Windows eller MS-DOS. Dess struktur består av bara en uppsättning instruktioner; den har ingen rubrik och innehåller inga standardmetadata. Den lagrar alla dess data och kod i endast ett segment och dess binära har maximalt 64KB i storlek. Det här filformatet flyttar inte sig självt när det försöker köras igen. Så operativsystemet laddar det på en förinställd adress. Dessutom är det möjligt att göra en COM-fil att köra under båda operativsystemen i form av en **fettbinär**. Det finns ingen faktisk kompatibilitet på instruktionsnivå. Instruktionerna vid ingångspunkten är valda att vara lika i funktionalitet men olika i båda operativsystemen, och gör att programmet körs, hoppa till avsnittet av operativsystemet som används. Det är i princip två olika program med samma procedur i en enda fil, föregås av kod som väljer den som ska användas.
### Exempel på COM-fil
När en COM-fil körs läses instruktionerna från den första byten och följs i följd tills de sista instruktionerna hittas. Här är ett exempel på ASM-kod:

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

## Referenser

* [COM-fil - av Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

