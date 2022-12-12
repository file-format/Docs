{
  "date" : "2021-06-24",
  "keywords" :[ "soubor bat", "co je soubor bat", "soubor", "příklad souboru bat", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů BAT a rozhraních API, která mohou vytvářet a otevírat soubory BAT.",
  "title" :"BAT - dávkový formát souboru",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Co je soubor BAT?
Soubor BAT je známý jako dávkový soubor, který běží v DOSu a všech verzích Windows pod cmd.exe. Skládá se ze série řádkových příkazů v prostém textu, které má provádět interpret příkazového řádku při provádění různých úkolů, jako je spouštění nástrojů údržby v systému Windows nebo spouštění typických programů. Dávkový soubor může obsahovat jakýkoli příkaz, který může být interaktivně přijat interpretem a používat strukturu kódu, která umožňuje podmíněné větvení a smyčkování, jak je zapsáno v dávkovém souboru.
## Formát souboru BAT
Formát souboru BAT je jednoduše skript začleněný k automatizaci sekvencí příkazů, které se svou povahou opakují. Termín "dávka" se používá pro dávkové zpracování, lze jej považovat za "neinteraktivní provádění". Dávkový soubor proto nemusí zpracovat dávku více dat. Ve starém diskovém operačním systému (DOS) byl dávkový soubor spouštěn v rozhraní příkazového řádku zadáním názvu souboru a přípony .bat. Dřívější operační systém Microsoft založený na grafickém rozhraní, jako je Microsoft Windows, byl závislý na DOSu. Uživatelé museli používat DOS k provádění typických operací, jako je oprava, optimalizace nebo přeinstalace Windows. Později Microsoft představil Windows NT, který nebyl závislý na operačním systému DOS. Proto lze dávkové soubory spustit pomocí příkazového řádku nebo **cmd.exe** v moderních operačních systémech Microsoft.
### Parametry dávkového souboru
Příkazový řádek podporuje řadu speciálních proměnných, jako je **%0, %1 až %9**, aby bylo možné odkazovat na název a cestu dávkové úlohy a devět parametrů volání z dávkové úlohy. Neexistující parametry jsou nahrazeny řetězcem s nulovou délkou. I když je lze použít podobně jako proměnné prostředí, ale v prostředí se neukládají. Microsoft a IBM označují tyto proměnné jako náhradní parametry, zatímco Novell, Digital Research a Caldera pro ně zavedly termín náhradní proměnné.

Zde jsou některé užitečné příkazy dávkového souboru:
| Příkaz | Popis |
------|------------|
| VER | Tento dávkový příkaz zobrazuje verzi systému MS-DOS, kterou používáte. |
|ASSOC| Toto je dávkový příkaz, který přidruží příponu k typu souboru (FTYPE), zobrazí existující přidružení nebo přidružení odstraní. |
|CD| Tento dávkový příkaz pomáhá při provádění změn v jiném adresáři nebo zobrazuje aktuální adresář. |
|CLS| Tento dávkový příkaz vymaže obrazovku. |
|KOPÍROVAT| Tento dávkový příkaz se používá pro kopírování souborů z jednoho umístění do druhého. |
|DEL| Tento dávkový příkaz odstraní soubory, nikoli adresáře. |
|DIR| Tento dávkový příkaz vypíše obsah adresáře. |
|DATUM| Tento dávkový příkaz pomůže najít systémové datum. |
|ECHO| Tento dávkový příkaz zobrazuje zprávy nebo zapíná nebo vypíná odezvu příkazu. |
|EXIT| Tento dávkový příkaz ukončí konzolu DOS. |
|MD| Tento dávkový příkaz vytvoří nový adresář v aktuálním umístění. |
|POHYB| Tento dávkový příkaz přesouvá soubory nebo adresáře mezi adresáři. |
|CESTA| Tento dávkový příkaz zobrazí nebo nastaví proměnnou cesty. |
|PAUZA| Tento dávkový příkaz vyzve uživatele a čeká na zadání řádku vstupu. |
|PROMPT| Tento dávkový příkaz lze použít ke změně nebo resetování příkazového řádku cmd.exe. |
|RD| Tento dávkový příkaz odstraní adresáře, ale před odstraněním musí být adresáře prázdné. |
|REN| Přejmenuje soubory a adresáře |
|REM| Tento dávkový příkaz se používá pro poznámky v dávkových souborech, čímž zabraňuje spuštění obsahu poznámky. |
|START| Tento dávkový příkaz spustí program v novém okně nebo otevře dokument. |
|ČAS| Tento dávkový příkaz nastavuje nebo zobrazuje čas. |
|TYP| Tento dávkový příkaz vytiskne obsah souboru nebo souborů na výstup. |
|VOL| Tento dávkový příkaz zobrazí jmenovky svazků. |
|ATTRIB| Zobrazí nebo nastaví atributy souborů v aktuálním adresáři |
|CHKDSK| Tento dávkový příkaz zkontroluje, zda na disku nejsou nějaké problémy. |
|VOLBA| Tento dávkový příkaz poskytuje uživateli seznam voleb. |
|CMD| Tento dávkový příkaz vyvolá další instanci příkazového řádku. |
|COMP| Tento dávkový příkaz porovná 2 soubory na základě velikosti souboru. |
|Převést| Tento dávkový příkaz převede svazek ze systému souborů FAT16 nebo FAT32 na systém souborů NTFS. |
|DRIVERQUERY| Tento dávkový příkaz zobrazí všechny nainstalované ovladače zařízení a jejich vlastnosti. |
|ROZŠÍŘIT| Tento dávkový příkaz extrahuje soubory z komprimovaných souborů CAB. |
|NAJÍT| Tento dávkový příkaz hledá řetězec v souborech nebo vstupu a vypisuje odpovídající řádky. |
|FORMÁT| Tento dávkový příkaz naformátuje disk tak, aby používal systém souborů podporovaný systémem Windows, jako je FAT, FAT32 nebo NTFS, čímž se přepíše předchozí obsah disku. |
|POMOC| Tento dávkový příkaz zobrazuje seznam příkazů dodávaných systémem Windows. |
|IPCONFIG| Tento dávkový příkaz zobrazí konfiguraci IP Windows. Zobrazuje konfiguraci podle připojení a název tohoto připojení. |
|ŠTÍTEK| Tento dávkový příkaz přidá, nastaví nebo odebere štítek disku. |
|VÍCE| Tento dávkový příkaz zobrazí obsah souboru nebo souborů, jednu obrazovku po druhé. |
|NET| Poskytuje různé síťové služby v závislosti na použitém příkazu. |
|PING| Tento dávkový příkaz odesílá pakety ICMP/IP „echo“ přes síť na určenou adresu. |
|VYPNUTÍ| Tento dávkový příkaz vypne počítač nebo odhlásí aktuálního uživatele. |
|ŘADIT| Tento dávkový příkaz převezme vstup ze zdrojového souboru a seřadí jeho obsah abecedně, od A do Z nebo Z do A. Vytiskne výstup na konzole. |
|SUBST| Tento dávkový příkaz přiřadí písmeno jednotky místní složce, zobrazí aktuální přiřazení nebo přiřazení odstraní. |
|SYSTÉMOVÉ INFORMACE| Tento dávkový příkaz ukazuje konfiguraci počítače a jeho operačního systému. |
|TASKKILL| Tento dávkový příkaz ukončí jednu nebo více úloh. |
|SEZNAM ÚKOL| Tento dávkový příkaz uvádí úlohy, včetně názvu úlohy a id procesu (PID). |
|XCOPY| Tento dávkový příkaz zkopíruje soubory a adresáře pokročilejším způsobem. |
|STROM| Tento dávkový příkaz zobrazí strom všech podadresářů aktuálního adresáře na libovolnou úroveň rekurze nebo hloubky. |
|FC |Tento dávkový příkaz uvádí skutečné rozdíly mezi dvěma soubory. |
|DISKPART |Tento dávkový příkaz zobrazuje a konfiguruje vlastnosti diskových oddílů. |
|TITLE |Tento dávkový příkaz nastaví titulek zobrazený v okně konzoly. |
|SET | Zobrazí seznam proměnných prostředí v aktuálním systému. |

## Příklad souboru BAT
Dávkové skripty se obvykle ukládají jako jednoduché textové soubory; obsahující příkazy, které se provádějí v sekvenci. Tyto soubory jsou uloženy s příponou .bat; rozpoznán a proveden pomocí softwaru **Command Interpreter**. Tento software je nativně dostupný v Microsoft Windows pod názvem **cmd.exe**.

Zde je ukázkový dávkový skript, který odstraní všechny soubory v aktuálním adresáři:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Reference

* [Batch Script – Stručný průvodce](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Dávkový soubor – od Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

