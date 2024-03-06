{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN fails",
"failu",
"BIN faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN faila formāts — Unix izpildāmais fails",
   "description":"Uzziniet par BIN formātu un API, kas var izveidot un atvērt BIN failus.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin-lv",
         "parent":"executable"
}
},
   "lastmod":"2023-07-20"
}

## Kas ir BIN fails?

BIN fails ir izpildāms fails operētājsistēmās, kuru pamatā ir Unix, piemēram, Linux vai FreeBSD. Tajā ir apkopota programma, kas sastāv no bināra koda, kas iegūts no pirmkoda, padarot to saderīgu ar pamatā esošo sistēmas arhitektūru. Unix izpildāmos BIN failus var salīdzināt ar Windows .EXE failiem un macOS .APP failiem, ņemot vērā to izpildāmo formātu lomu.

Unix sistēmu programmatūras izstrādes jomā izstrādātāji parasti izmanto BIN failus, lai iepakotu un izplatītu programmas. Tie piedāvā ērtu veidu programmatūras piegādei lietotājiem, kas ļauj viegli instalēt un izpildīt. Līdzās BIN failiem ir arī citi Unix izpildāmo failu veidi, tostarp [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) un .X86_64, un katrs ir pielāgots konkrētām aparatūras vai sistēmas prasībām.

Runājot par BIN faila iekšējo struktūru, tas sastāv no kodētiem datiem, kurus Unix operētājsistēma izmanto, lai identificētu, lasītu un izpildītu pievienoto programmu. Sistēma paļaujas uz konkrētiem failu parakstiem vai galvenēm, lai atpazītu BIN failu kā izpildāmu, kam seko tajā ietverto bināro instrukciju interpretācija un izpilde.

BIN failiem bieži vien ir pievienots fails **INSTALL.TXT**, kurā sniegti detalizēti norādījumi par to, kā pareizi instalēt un iestatīt programmu. Šī dokumentācija nodrošina, ka lietotāji var veiksmīgi orientēties instalēšanas procesā un bez sarežģījumiem sākt lietot programmatūru.

## Kā atvērt BIN failu?

BIN faili nav paredzēti tiešai atvēršanai un skatīšanai. Tomēr jūs varat izpildīt programmas vai izvilkt tajās esošos datus. Lai piekļūtu BIN faila saturam, izpildiet šīs darbības komandrindā, pieņemot, ka BIN faila nosaukums ir sample.bin:

1. **Nodrošiniet izpildāmās atļaujas:**

Pirms BIN faila izpildes pārliecinieties, ka tam ir nepieciešamās atļaujas, lai to palaistu kā izpildāmo failu. Izmantojiet komandu:

```
$ chmod +x sample.bin
```

Šī komanda failam piešķir izpildāmās privilēģijas.

2. **Izpildiet BIN failu:**

Pēc izpildāmo atļauju iestatīšanas varat palaist BIN failu, ievadot šādu komandu:

```
$ ./sample.bin
```

**Brīdinājums**

_Esiet piesardzīgs, strādājot ar lejupielādētiem vai pa e-pastu nosūtītiem BIN failiem, jo kibernoziedznieki tos var izmantot ļaunprātīgas programmatūras izplatīšanai. Palaidiet BIN failus tikai no uzticamiem avotiem, lai mazinātu ļaunprātīgu izpildāmu uzbrukumu risku._

## Citi BIN faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.bin**.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Atsauces

* [Kā izpildīt bināros failus operētājsistēmā Linux](https://linuxhint.com/execute-binary-files-in-linux/)



