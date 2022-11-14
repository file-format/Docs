{
  "date" : "2021-06-29",
  "keywords" :[ "com-bestand", "wat is een com-bestand", "bestand", "com-voorbeeld", "com-bestandsextensie", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over COM-bestandsindelingen en API's die COM-bestanden kunnen maken en openen.",
  "title" :"COM - DOS-opdrachtbestandsindeling",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een COM-bestand?
De COM-bestanden worden eenvoudigweg gebruikt voor het uitvoeren van een reeks opdrachten of instructies. Een COM-bestand bestaat uit een uitvoerbaar programma dat kan worden uitgevoerd vanuit Windows of MS-DOS. Evenzo een EXE-bestand, het COM-bestand wordt ook opgeslagen in binair formaat, maar het is anders dan het EXE-bestand omdat het geen header of metadata heeft en het heeft ook de maximale grootte van ongeveer 64 KB. Wanneer het COM-bestand voor de eerste keer op een 32-bits systeem wordt uitgevoerd, wordt gevraagd om het onderdeel NT Virtual DOS Machine (NTVDM) te installeren. Het COM-bestand kan worden uitgevoerd op de 64-bits versie van Microsoft Windows met een virtuele machine die de MS-DOS-omgeving ondersteunt.

## COM-bestandsindeling
Het COM-bestandsformaat is een binair uitvoerbaar formaat dat wordt gebruikt in Microsoft Windows of MS-DOS. De structuur bestaat uit slechts een reeks instructies; het heeft geen header en bevat geen standaard metadata. Het slaat al zijn gegevens en code op in slechts één segment en het binaire bestand heeft een maximale grootte van 64 KB. Dit bestandsformaat verplaatst zichzelf niet wanneer het opnieuw wordt uitgevoerd. Dus het besturingssysteem laadt het op een vooraf ingesteld adres. Bovendien is het mogelijk om een COM-bestand onder beide besturingssystemen uit te voeren in de vorm van een **dikke binary**. Er is geen echte compatibiliteit op instructieniveau. De instructies bij het beginpunt zijn geselecteerd om gelijk te zijn in functionaliteit, maar verschillend in beide besturingssystemen, en om het programma te laten draaien, spring naar het gedeelte van het besturingssysteem dat in gebruik is. Het zijn in feite twee verschillende programma's met dezelfde procedure in een enkel bestand, voorafgegaan door code die het te gebruiken programma selecteert.
### COM-bestand voorbeeld
Bij het uitvoeren van een COM-bestand worden de instructies gelezen vanaf de eerste byte en worden ze achtereenvolgens gevolgd totdat de laatste instructies zijn gevonden. Hier is een voorbeeld van een ASM-code:

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

## Referenties

* [COM-bestand - door Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

