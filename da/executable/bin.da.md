{
   "date":"2023-07-20",
   "keywords":[
"BEHOLDER",
"BIN fil",
"fil",
"BIN filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN filformat - Unix eksekverbar fil",
   "description":"Lær om BIN-format og API'er, der kan oprette og åbne BIN-filer.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin-da",
         "parent":"executable"
}
},
   "lastmod":"2023-07-20"
}

## Hvad er en BIN fil?

En BIN-fil er en eksekverbar fil på Unix-baserede operativsystemer såsom Linux eller FreeBSD. Den har et kompileret program sammensat af binær kode afledt af kildekoden, hvilket gør den kompatibel med den underliggende systemarkitektur. Unix-eksekverbare BIN-filer kan sammenlignes med Windows .EXE-filer og macOS .APP-filer med hensyn til deres rolle som eksekverbare formater.

Inden for softwareudvikling til Unix-systemer anvendes BIN-filer almindeligvis af udviklere til at pakke og distribuere programmer. De tilbyder et praktisk middel til at levere software til brugerne, hvilket giver mulighed for nem installation og udførelse. Ud over BIN-filer findes der andre typer Unix-eksekverbare filer, inklusive [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) og .X86_64, hver skræddersyet til specifikke hardware- eller systemkrav.

Når det kommer til den interne struktur af en BIN-fil, består den af kodede data, som Unix-operativsystemet bruger til at identificere, læse og udføre det vedlagte program. Systemet er afhængigt af specifikke filsignaturer eller overskrifter for at genkende BIN-filen som en eksekverbar, efterfulgt af fortolkningen og udførelsen af de binære instruktioner indeholdt i den.

BIN-filer kommer ofte sammen med en medfølgende **INSTALL.TXT**-fil, som giver detaljerede instruktioner om, hvordan man korrekt installerer og opsætter programmet. Denne dokumentation sikrer, at brugere kan navigere i installationsprocessen med succes og begynde at bruge softwaren uden komplikationer.

## Hvordan åbner jeg filen BIN?

BIN-filer er ikke designet til at blive åbnet og vist direkte. Du kan dog køre programmerne eller udtrække de data, de indeholder. For at få adgang til indholdet af en BIN-fil skal du følge disse trin på kommandolinjen, forudsat at navnet på BIN-filen er sample.bin:

1. **Sørg for eksekverbare tilladelser:**

Før du udfører BIN-filen, skal du sikre dig, at den har de nødvendige tilladelser til at blive kørt som en eksekverbar. Brug kommandoen:

```
$ chmod +x sample.bin
```

Denne kommando giver filen eksekverbare rettigheder.

2. **Kør BIN-filen:**

Efter at have indstillet de eksekverbare tilladelser, kan du køre BIN-filen ved at indtaste følgende kommando:

```
$ ./sample.bin
```

**Advarsel**

_Udvis forsigtighed, når du håndterer downloadede eller e-mailede BIN-filer, da de potentielt kan bruges af cyberkriminelle til at distribuere malware. Kør kun BIN-filer fra pålidelige kilder for at mindske risikoen for ondsindede eksekverbare angreb._

## Andre BIN-filer

Her er andre filtyper, der bruger filtypen **.bin**.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Referencer

* [Sådan udføres binære filer i Linux](https://linuxhint.com/execute-binary-files-in-linux/)



