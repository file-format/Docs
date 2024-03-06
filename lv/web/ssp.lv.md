---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP — Scala servera lapu faila veidlapaat
linktitle: SSP
description: Lnopelniet par SSP faila formātu un API, kas var izveidot un atvērt SSP failus.
menu:
  docs:
    identifier: "web-ss-lvp"
    parent: "web"
lastmod: 2021-09-30
---

## Kas ir SSP fails?

Fails ar paplašinājumu .ssp ir tīmekļa lapa, kas izveidota ar Scala kodu izteiksmēm, nevis tikai vienkāršu HTML. Tas darbojas kā servera puses skripts, izmantojot HTML un Scala kombināciju. Šie faili atrodas serverī un tiek izmantoti, lai izveidotu statiskas tīmekļa lapas, kas tiks rādītas lietotājiem. Pati Scala ir vispārējas nozīmes programmēšanas valoda, kuras sintakse ir pazīstama lietotājiem, kuri ir strādājuši ar Velocity, JSP vai Erb. SSP failus var analizēt un novērtēt, izmantojot [Scalate](https://scalate.github.io/scalate/), kas ir uz Scala balstīta veidņu programma teksta un marķējuma ģenerēšanai.

## SSP faila formāts — vairāk informācijas

SSP faili tiek saglabāti vienkārša teksta failā, un tos var novērtēt, izmantojot Scalate. Ssp veidne sastāv no vienkārša teksta, kas biežāk ir HTML dokuments. Tajā ir iegulti Ssp tagi, kas liek renderēšanas programmām dinamiski renderēt dažādas dokumenta daļas. Tagi sākas un beidzas ar <% ... %> un ${ ... } secību, un viss ārpus šīm tiek uzskatīts par burtisku tekstu.

### SSP piemērs

Nākamajā piemērā ir parādīts SSP kods un tā izvade, kad to renderē renderēšanas programma.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Izvade ir šāda.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Atsauces

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

