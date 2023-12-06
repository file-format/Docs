{
"data":"2023-07-20",
   "keywords":[
"COS",
"Fișier BIN",
"fişier",
"Extensie fișier BIN",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier BIN - fișier executabil Unix",
   "description":"Aflați despre formatul BIN și despre API-urile care pot crea și deschide fișiere BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Ce este un fișier BIN?

Un fișier BIN este un fișier executabil pe sisteme de operare bazate pe Unix, cum ar fi Linux sau FreeBSD. Deține un program compilat compus din cod binar derivat din codul sursă, făcându-l compatibil cu arhitectura sistemului de bază. Fișierele BIN executabile Unix pot fi comparate cu fișierele Windows .EXE și fișierele macOS .APP în ceea ce privește rolul lor ca formate executabile.

În domeniul dezvoltării software pentru sistemele Unix, fișierele BIN sunt utilizate în mod obișnuit de dezvoltatori pentru a împacheta și distribui programe. Ele oferă un mijloc convenabil de a furniza software utilizatorilor, permițând instalarea și execuția ușoară. Pe lângă fișierele BIN, există și alte tipuri de executabile Unix, inclusiv [.ELF](/ro/executable/elf/), .X86, [.RUN](/ro/executable/run/) și .X86_64, fiecare adaptat pentru un anumit hardware sau Cerințe de sistem.

Când vine vorba de structura internă a unui fișier BIN, acesta constă din date codificate pe care sistemul de operare Unix le utilizează pentru a identifica, citi și executa programul inclus. Sistemul se bazează pe semnături sau anteturi de fișiere specifice pentru a recunoaște fișierul BIN ca executabil, urmat de interpretarea și executarea instrucțiunilor binare conținute în acesta.

Fișierele BIN vin adesea împreună cu un fișier însoțitor **INSTALL.TXT**, care oferă instrucțiuni detaliate despre cum să instalați și să configurați corect programul. Această documentație asigură că utilizatorii pot naviga cu succes în procesul de instalare și pot începe să utilizeze software-ul fără complicații.

## Cum se deschide fișierul BIN?

Fișierele BIN nu sunt concepute pentru a fi deschise și vizualizate direct. Cu toate acestea, puteți executa programele sau puteți extrage datele pe care le conțin. Pentru a accesa conținutul unui fișier BIN, urmați acești pași pe linia de comandă, presupunând că numele fișierului BIN este "sample.bin":

1. **Asigurați permisiunile executabile:**

Înainte de a executa fișierul BIN, asigurați-vă că are permisiunile necesare pentru a fi rulat ca executabil. Utilizați comanda:

```
$ chmod +x sample.bin
```

Această comandă acordă fișierului privilegii executabile.

2. **Execută fișierul BIN:**

După setarea permisiunilor executabile, puteți rula fișierul BIN introducând următoarea comandă:

```
$ ./sample.bin
```

**Avertizare**

_Aveți grijă atunci când aveți de-a face cu fișiere BIN descărcate sau trimise prin e-mail, deoarece acestea pot fi folosite de infractorii cibernetici pentru a distribui programe malware. Rulați fișiere BIN numai din surse de încredere pentru a reduce riscul atacurilor executabile rău intenționate._

## Alte fișiere BIN

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.bin**.

- [BIN - Fișier codificat MacBinary](/ro/compression/bin/)
- [BIN - Fișier imagine disc binar](/ro/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/ro/settings/bin/)
- [BIN - Sega Genesis Game ROM](/ro/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/ro/game/bin-pcsx/)

## Referințe

* [Cum se execută fișiere binare în Linux](https://linuxhint.com/execute-binary-files-in-linux/)


