{
"date":"20.07.2023",
   "keywords":[
"ZÁSOBNÍK",
"Soubor BIN",
"soubor",
"Přípona souboru BIN",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru BIN - spustitelný soubor Unix",
   "description":"Další informace o formátu BIN a rozhraních API, která mohou vytvářet a otevírat soubory BIN.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Co je soubor BIN?

Soubor BIN je spustitelný soubor v operačních systémech založených na Unixu, jako je Linux nebo FreeBSD. Obsahuje zkompilovaný program složený z binárního kódu odvozeného ze zdrojového kódu, díky čemuž je kompatibilní se základní architekturou systému. Soubory Unix Executable BIN lze přirovnat k souborům Windows .EXE a macOS .APP, pokud jde o jejich roli jako spustitelné formáty.

V oblasti vývoje softwaru pro systémy Unix jsou soubory BIN běžně využívány vývojáři k balení a distribuci programů. Nabízejí pohodlný způsob dodávání softwaru uživatelům, což umožňuje snadnou instalaci a spuštění. Kromě souborů BIN existují další typy unixových spustitelných souborů, včetně [.ELF](/cs/executable/elf/), .X86, [.RUN](/cs/executable/run/) a .X86_64, každý přizpůsobený konkrétnímu hardwaru nebo Požadavky na systém.

Pokud jde o vnitřní strukturu souboru BIN, skládá se ze zakódovaných dat, která operační systém Unix využívá k identifikaci, čtení a provádění přiloženého programu. Systém se spoléhá na specifické podpisy souborů nebo hlavičky, aby rozpoznal soubor BIN jako spustitelný soubor, po kterém následuje interpretace a provedení binárních instrukcí v něm obsažených.

Soubory BIN jsou často dodávány s doprovodným souborem **INSTALL.TXT**, který poskytuje podrobné pokyny, jak správně nainstalovat a nastavit program. Tato dokumentace zajišťuje, že uživatelé mohou úspěšně procházet instalačním procesem a začít používat software bez komplikací.

## Jak otevřít soubor BIN?

Soubory BIN nejsou určeny k přímému otevírání a prohlížení. Můžete však spouštět programy nebo extrahovat data, která obsahují. Chcete-li získat přístup k obsahu souboru BIN, postupujte podle následujících kroků na příkazovém řádku za předpokladu, že název souboru BIN je „sample.bin“:

1. **Zajistěte oprávnění ke spustitelnému souboru:**

Před spuštěním souboru BIN se ujistěte, že má potřebná oprávnění ke spuštění jako spustitelný soubor. Použijte příkaz:

```
$ chmod +x sample.bin
```

Tento příkaz uděluje spustitelný soubor oprávnění.

2. **Spusťte soubor BIN:**

Po nastavení oprávnění ke spustitelnému souboru můžete spustit soubor BIN zadáním následujícího příkazu:

```
$ ./sample.bin
```

**Varování**

_Buďte opatrní při práci se staženými nebo e-mailovými soubory BIN, protože je mohou potenciálně využít kyberzločinci k distribuci malwaru. Spouštějte soubory BIN pouze z důvěryhodných zdrojů, abyste snížili riziko škodlivých útoků na spustitelné soubory._

## Další soubory BIN

Zde jsou další typy souborů, které používají příponu souboru **.bin**.

- [BIN - MacBinary Encoded File](/cs/compression/bin/)
- [BIN - soubor s obrázkem binárního disku](/cs/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/cs/settings/bin/)
- [BIN - Sega Genesis Game ROM](/cs/game/bin/)
- [BIN - Obrázek PSX PlayStation BIOS](/cs/game/bin-pcsx/)

## Reference

* [Jak spustit binární soubory v Linuxu](https://linuxhint.com/execute-binary-files-in-linux/)


