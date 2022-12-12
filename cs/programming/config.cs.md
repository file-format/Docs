{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - konfigurační soubor",
  "description":"Další informace o formátu souboru CONFIG s příkladem CONFIG a rozhraními API, která mohou vytvářet a otevírat soubory CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Co je soubor CONFIG?
Soubor CONFIG je známý jako konfigurační soubor; slouží ke konfiguraci parametrů a primárních nastavení pro několik počítačových softwarů. Některé programy čtou pouze své **konfigurační soubory** při spuštění. Ostatní pravidelně kontrolují změny v konfiguračních souborech.

## CONFIG Formát souboru
Formát **CONFIG File** se používá pro serverové procesy, softwarové aplikace a nastavení operačního systému. Programátor může napsat kód, který dá softwaru pokyn, aby po určité době znovu a znovu četl konfigurační soubory a aplikoval změny na aktuální proces. Neexistují žádné definitivní standardy nebo přísné konvence pro sysntax souboru CONFIG. Například soubor Web.config společnosti Microsoft patří do formátu souboru CONFIG, který se skládá ze sad značek založených na [XML](https://docs.fileformat.com/web/xml/); lze upravovat pomocí Microsoft Visual Studio nebo jiného textového editoru.

## Příklady konfiguračních souborů:
Protože konfigurační soubory nejsou vytvářeny podle žádných pravidel, standardů nebo konvencí, mohly být tyto soubory napsány v různých formátech. Soubor .config může být založen na XML, [JSON](https://docs.fileformat.com/web/json/) nebo jakémkoli jiném formátu. Níže jsou uvedeny příklady konfiguračních souborů pro dobře známé operační systémy a software:

### Konfigurační soubory v Linuxu
Každý linuxový program je spustitelný soubor, který uchovává seznam **operačních kódů**, které CPU provádí k provádění typických operací. Operace téměř každého programu lze upravit podle vašich požadavků změnou jeho konfiguračních souborů. Několik konfiguračních souborů v systému Linux je v adresáři /etc. Konfigurační soubory lze rozdělit do následujících kategorií:
|Kategorie|Příklad| Komentáře|
---|---|---|
|Přístup k souborům|/etc/host.conf|Říká serveru síťové domény, jak vyhledat názvy hostitelů.|
|Bootování a přihlášení/odhlášení|/etc/rc.d/rc.local|Neoficiální. Může být voláno z rc, rc.sysinit nebo /etc/inittab.|
|Souborový systém|/etc/mtools.conf|Konfigurace pro všechny operace (mkdir, kopírování, formátování atd.) na souborovém systému typu DOS.|
|Správa systému|/etc/shells|Uchovává seznam možných „skořápek“, které má systém k dispozici.|
|Networking|/etc/gated.conf|Konfigurace pro gated. Používá pouze démon brány.|
|Systémové příkazy|/etc/logrotate.conf|Konfigurace pro Dynamic Linker.|
|Démoni|/etc/httpd.conf|Konfigurační soubor pro Apache, webový server. Tento soubor obvykle není v /etc.|
|Uživatelské programy| /etc/lynx.cfg| Nastavení proxy|
### Příklad souboru AWS CONFIG
Často používaná konfigurační nastavení a přihlašovací údaje lze uložit do souborů CONFIG, které jsou spravovány rozhraním AWS CLI. Soubor CONFIG musí být soubor ve formátu prostého textu, který používá následující formát:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Příklad souboru CONFIG SSH
Konfigurační soubor OpenSSH na straně klienta se jmenuje CONFIG a je uložen v adresáři .ssh. Soubor SSH CONFIG se skládá z následující struktury:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Příklad souboru Python CONFIG
Soubor Python CONFIG by mohl vypadat takto:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Reference

* [Pochopení konfiguračních souborů Linuxu](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Nastavení souboru konfigurace a přihlašovacích údajů](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Konfigurační soubory v Pythonu](https://martin-thoma.com/configuration-files-in-python/)

