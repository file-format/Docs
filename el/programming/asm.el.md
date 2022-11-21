{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου ASM - Μορφή αρχείου πηγαίου κώδικα γλώσσας Assembly",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ASM και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ASM.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Τι είναι ένα αρχείο ASM; ##

Ένα αρχείο ASM είναι ένα πρόγραμμα γραμμένο στη γλώσσα προγραμματισμού χαμηλού επιπέδου που είναι γνωστή ως γλώσσα assembly. Χρησιμοποιείται κυρίως για τη σύνταξη κώδικα σχετικού με το υλικό, όπως για τον προγραμματισμό μικροελεγκτών. Το πρόγραμμα είναι γραμμένο χρησιμοποιώντας απλή σύνταξη γλώσσας συναρμολόγησης που περιλαμβάνει τελεστές και τελεστές για την εκτέλεση διαφορετικών λειτουργιών. Τα αρχεία ASM γράφονται και επεξεργάζονται σε προγράμματα επεξεργασίας κειμένου και εκτελούνται χρησιμοποιώντας ένα πρόγραμμα συναρμολόγησης όπως τα HLA, MASM, FASM, NASM ή GAS.

## Μορφή αρχείου ASM

Τα αρχεία ASM αποτελούνται από μια ακολουθία λειτουργιών που εκτελούνται από έναν assembler για τη δημιουργία **κώδικα αντικειμένου**. Ο κώδικας αντικειμένου που προκύπτει είναι μια μετάφραση συνδυασμών μνημονικών και τρόπων διεύθυνσης στα αριθμητικά τους ισοδύναμα.

### Παράδειγμα μορφής αρχείου ASM

Ακολουθεί ένα παράδειγμα εφαρμογής **Hello World** για αρχιτεκτονική x86.
```
global  go
extern  _ExitProcess@4
extern  _GetStdHandle@4
extern  _WriteConsoleA@20

section .data
msg:    db      'Hello, World', 10
handle: db      0
written:
db      0

section .text
go:
; handle = GetStdHandle(-11)
push    dword -11
call    _GetStdHandle@4
mov     [handle], eax

; WriteConsole(handle, &msg[0], 13, &written, 0)
push    dword 0
push    written
push    dword 13
push    msg
push    dword [handle]
call    _WriteConsoleA@20

; ExitProcess(0)
push    dword 0
call    _ExitProcess@4
```

## Αναφορά ##

* [Assembly Language - by Wikipedia](https://en.wikipedia.org/wiki/Assembly_language)
* [Assembly Language - Basic Syntax](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)

