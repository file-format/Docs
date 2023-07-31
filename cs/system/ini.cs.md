{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "rozšíření", "soubor", "formát", "systém", "Spuštění", "přípona adresáře", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - formát iniciačního souboru",
  "description":"Další informace o formátu souboru INI a rozhraních API, která mohou vytvářet a otevírat soubory INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Co je soubor INI? ##

Soubor INI je dokument konfigurace zpráv pro počítačové programy, které obsahují veřejné klíče pro charakteristiky a sekce, které organizují atributy v rámci a gramatice. Tyto konfigurační dokumenty formátu systémových souborů získaly svůj název podle přípony adresáře INI operačního systému MS-DOS, což je zkratka pro zahájení. Popularizovala tuto formu nastavení softwaru. Mnoho programů v jiných softwarových aplikacích používá různé přídavky k názvům souborů, jako je CONF a [CFG](/cs/system/cfg/), ačkoli tento formát v mnoha situacích konfigurace vytvořil neoficiální standard.

## Stručná historie souborů INI##

Zpočátku byla hlavní technika konfigurace programu Windows formát textového souboru, který se skládal z řádků textu s jedním rozhodujícím párem na řádek, rozdělených do sekcí. V tomto formátu byly uloženy ovladače zařízení, typy písma a spouštěcí spouštěče. Jednotlivá nastavení byla také běžně uložena v INI souborech aplikacemi.
Až do Windows 3.1x byl formát podporován na 16bitových platformách Microsoft Windows. Počínaje Windows 95 začal Microsoft podporovat vývojáře, aby pro konfiguraci používali registr Windows namísto souborů INI.

## Soubor INI - Specifikace formátu souboru

### Klíče/Vlastnosti ###

Klíč/vlastnost je nejzákladnějším prvkem souboru INI. Symbol rovná se (=) odděluje název a hodnotu každého klíče. Vlevo od rovnítka je místo, kde se zobrazuje název. Symbol rovná se a středník jsou v systému Windows diskrétní písmena, a proto je nelze v klíči použít. V hodnotě lze použít libovolný znak.

```
name=value
```

### Sekce ###

Komentář sekce se zobrazí v hranatých závorkách ([]) na samostatném řádku. Po definici sekce jsou všechny klíče propojeny s touto sekcí. Sekce končí u dalšího označení sekce nebo na konci dokumentu; neexistuje žádný specifický oddělovač "konec sekce". Sekce nelze stohovat; mohou být pojmenovány pouze jednou a není nutné je propojovat.

```
[section]
a=a
b=b
```

### Změna funkcí ###

Formát souboru INI nemá celosvětově uznávanou definici. Mnoho počítačových aplikací obsahuje funkce navíc k již zmíněným. Níže uvedený seznam obsahuje některé společné charakteristiky, které mohou, ale nemusí být obsaženy v žádném jednotlivém programu.

* Komentáře
* Útěk postavy
* Duplicitní jména


## Příklad INI ##

Ukázkový soubor INI vypadá následovně:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## reference ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

