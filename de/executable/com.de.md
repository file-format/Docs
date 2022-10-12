{
  "date" : "2021-06-29",
  "keywords" :[ "com-Datei", "was ist eine com-Datei", "Datei", "com-Beispiel", "com-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das COM-Dateiformat und APIs, die COM-Dateien erstellen und öffnen können.",
  "title" :"COM - DOS-Befehlsdateiformat",
  "linktitle" :"KOM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine COM-Datei?
Die COM-Dateien werden einfach zum Ausführen einer Reihe von Befehlen oder Anweisungen verwendet. Eine COM-Datei besteht aus einem ausführbaren Programm, das unter Windows oder MS-DOS ausgeführt werden kann. Ebenso wie eine EXE-Datei wird die COM-Datei auch im Binärformat gespeichert, unterscheidet sich jedoch von der EXE-Datei, da sie keine Header- oder Metadaten enthält und außerdem die maximale Größe von ungefähr 64 KB hat. Wenn die COM-Datei zum ersten Mal auf einem 32-Bit-System ausgeführt wird, werden Sie aufgefordert, die Komponente NT Virtual DOS Machine (NTVDM) zu installieren. Die COM-Datei kann auf der 64-Bit-Version von Microsoft Windows mit einer virtuellen Maschine ausgeführt werden, die die MS-DOS-Umgebung unterstützt.

## COM-Dateiformat
Das COM-Dateiformat ist ein binäres ausführbares Format, das in Microsoft Windows oder MS-DOS verwendet wird. Seine Struktur besteht nur aus einer Reihe von Anweisungen; es hat keinen Header und enthält keine Standard-Metadaten. Es speichert alle seine Daten und seinen Code in nur einem Segment und seine Binärdatei hat eine maximale Größe von 64 KB. Dieses Dateiformat verschiebt sich nicht selbst, wenn Sie versuchen, es erneut auszuführen. Das Betriebssystem lädt es also an einer voreingestellten Adresse. Außerdem ist es möglich, eine COM-Datei zur Ausführung unter beiden Betriebssystemen in Form einer **fetten Binärdatei** zu erstellen. Es gibt keine tatsächliche Kompatibilität auf der Unterrichtsebene. Die Anweisungen am Einstiegspunkt sind so ausgewählt, dass sie in der Funktionalität gleich, aber in beiden Betriebssystemen unterschiedlich sind, und das Programm zum Laufen bringen, zu dem Abschnitt des verwendeten Betriebssystems springen. Es handelt sich im Grunde genommen um zwei verschiedene Programme mit demselben Verfahren in einer einzigen Datei, denen ein Code vorangestellt ist, der das zu verwendende auswählt.
### COM-Dateibeispiel
Beim Ausführen einer COM-Datei werden die Anweisungen ab dem ersten Byte gelesen und fortlaufend ausgeführt, bis die letzten Anweisungen gefunden sind. Hier ist ein ASM-Codebeispiel:

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

## Verweise

* [COM-Datei - von Wikipedia](https://en.wikipedia.org/wiki/COM_file)

