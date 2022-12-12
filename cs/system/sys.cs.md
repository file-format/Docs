{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "rozšíření", "soubor", "formát", "systém", "Ovladač", "Systémový soubor", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Formát systémových souborů",
  "description":"Další informace o formátu souborů SYS a rozhraních API, která mohou vytvářet a otevírat soubory SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Co je soubor SYS? ##

Soubory SYS jsou "systémové soubory" používané v aplikacích OS Windows a MS-DOS. Tyto soubory nelze otevřít přímo a sestávají z ovladače a konfigurace zařízení. Soubory SYS jsou zodpovědné za to, že obsahují soubory základních funkcí operačního systému. Tyto soubory jsou považovány za kritické soubory ovladače zařízení a lze je také použít, když je třeba vyřešit jakýkoli problém se závodním ovladačem. Ty jsou zodpovědné za správné fungování počítačového systému a soubory .sys musí být správné a úplné.


## Technická specifikace ##

Soubory .sys jsou ve skutečnosti podmnožinou formátu [BMP](/cs/image/bmp), protože umožňují pouze specifické kombinace. Obvyklý formát těchto souborů je LOGOS.SYS, LOGOW.SYS a LOGO.SYS. Žádné jiné soubory tento formát nemají.

Tyto soubory se většinou používají v adresáři *C* systému Windows v době instalace. Většina problémů, které se točí kolem ovladačů zařízení, je vyřešena aktualizací operačního systému Windows. Podrobnosti a informace o těchto souborech lze zobrazit pomocí vestavěných programů operačního systému Windows. Patří sem také odkazy na různé moduly v operačním systému.
Některé z příkladů systémových souborů jsou:

* IO.SYS (Ukládají ovladače zařízení diskového operačního systému)
* MSDOS.SYS (obsahuje jádro nebo základní kód operačního systému)
* CONFIG.SYS (obsahuje různé možnosti konfigurace)
* KEYBOARD.SYS (obsahuje informace související s rozložením klávesnice)
* COUNTRY.SYS (Tyto obsahují informace o zemi a kódové stránce)

## Formát souboru SYS ##

Microsoft vyvinul soubory s příponami .sys. Proměnné a funkce jsou součástí souborů SYS. Ty jsou většinou používány operačním systémem Microsoft. Tyto soubory jsou umístěny hlavně v kořenovém adresáři disku:

* C:\Windows\system32\ovladače
* C:\Windows\WinSxS

Některá běžná upozornění na soubory SYS jsou následující:

* Názvy těchto souborů by se neměly měnit, protože tyto soubory jsou zodpovědné za základní funkce a proměnné operačního systému
* Tyto soubory by neměly být mazány, protože jejich absence může způsobit chyby
* Soubory .sys by neměly být stahovány z internetu, dokud si nejste jisti legitimitou zdroje
* Člověk by si s těmito soubory neměl zahrávat, protože jejich změna nebo manipulace s nimi způsobuje vážné systémové chyby
* Pokud se tyto soubory poškodí nějakým virem nebo malwarem, je třeba je znovu nainstalovat

## Příklad SYS ##

Následuje příklad jednoduchého konfiguračního souboru systému SYS:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
