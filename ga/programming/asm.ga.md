{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Formáid Chomhaid ASM - Formáid Chomhaid Chód Foinse Teanga Tionóil",
  "description":"Foghlaim faoi fhormáid comhaid ASM agus APIanna ar féidir leo comhaid ASM a chruthú agus a oscailt.",
  "linktitle" : "ASM",
  "menu" : {
    "docs" : {
      "identifier" : "programming-asm-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Cad is comhad ASM ann? ##

Is clár é comhad ASM atá scríofa sa teanga ríomhchláraithe ísealleibhéil ar a dtugtar teanga tionóil. Úsáidtear go príomha é chun cód a bhaineann le crua-earraí a scríobh, mar shampla le haghaidh ríomhchláraitheoirí. Scríobhtar an clár agus úsáid á baint as comhréir shimplí sa teanga tionóil a chuimsíonn oibreoirí agus oibritheoirí chun oibríochtaí éagsúla a dhéanamh. Déantar comhaid ASM a scríobh agus a chur in eagar in eagarthóirí téacs agus déantar iad a fhorghníomhú ag baint úsáide as clár cóimeálaí mar HLA, MASM, FASM, NASM, nó GAS.

## Formáid Chomhaid ASM

Is éard atá i gcomhaid ASM seicheamh oibríochtaí a dhéanann cóimeálaí chun **cód réad** a ghiniúint. Is éard atá sa chód oibiachta dá bharr ná aistriú ar theaglaim de chuimhneacháin agus de mhodhanna seoltaí ina gcoibhéisí uimhriúla.

### Sampla Formáid Comhaid ASM

Seo a leanas sampla d’iarratas **Hello World** ar ailtireacht x86.
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

## Tagairt ##

* [Teanga an Tionóil - le Vicipéid](https://en.wikipedia.org/wiki/Assembly_language )

* [Teanga Tionóil - Comhréir Bunúsach](https://www.tutorialspoint.com/assembly_programming/assembly_basic_syntax.htm)


