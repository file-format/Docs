{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Konfigurationsfil",
  "description":"Lär dig om CONFIG-filformat med CONFIG-exempel och API:er som kan skapa och öppna CONFIG-filer.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är en CONFIG fil?
En CONFIG-fil kallas konfigurationsfil; används för att konfigurera parametrarna och primära inställningar för flera datorprogram. Vissa program läser bara sina **konfigurationsfiler** vid uppstart. Andra kontrollerar konfigurationsfilerna för ändringar med jämna mellanrum.

## CONFIG Filformat
**CONFIG-filformatet** används för serverprocesser, programvaror och operativsysteminställningar. En programmerare kan skriva kod för att instruera en programvara att läsa konfigurationsfilerna om och om igen efter en viss tidsperiod och tillämpa ändringarna på den aktuella processen. Det finns inga definitiva standarder eller starka konventioner för CONFIG-filsysntax. Till exempel, Microsofts Web.config-fil tillhör filformatet CONFIG, som består av en [XML](https://docs.fileformat.com/web/xml/)-baserad taggset; kan redigeras med Microsoft Visual Studio eller någon annan textredigerare.

## Exempel på konfigurationsfiler:
Eftersom konfigurationsfilerna inte skapas genom att följa några regler, standarder eller konventioner, kan dessa filer ha skrivits med olika format. En .config-fil kan vara baserad på XML, [JSON](https://docs.fileformat.com/web/json/) eller något annat format. Följande är exempel på konfigurationsfiler för välkända operativsystem och programvara:

### Konfigurationsfiler i Linux
Varje Linux-program är en körbar fil som innehåller listan över **opkoder** som CPU:n kör för att utföra typiska operationer. Driften av nästan alla program kan anpassas till dina krav genom att ändra dess konfigurationsfiler. Flera konfigurationsfiler i Linux-systemet finns i katalogen /etc. Konfigurationsfilerna kan klassificeras i följande kategorier:
|Kategori|Exempel| Kommentarer|
---|---|---|
|Åtkomstfiler|/etc/host.conf|Berättar för nätverksdomänservern hur man söker upp värdnamn.|
|Starta och logga in/logga ut|/etc/rc.d/rc.local|Inte officiellt. Kan anropas från rc, rc.sysinit eller /etc/inittab.|
|Filsystem|/etc/mtools.conf|Konfiguration för alla operationer (mkdir, copy, format, etc.) på ett DOS-typ filsystem.|
|Systemadministration|/etc/shells|Innehåller listan över möjliga "skal" som är tillgängliga för systemet.|
|Nätverk|/etc/gated.conf|Konfiguration för gated. Används endast av den gated daemon.|
|Systemkommandon|/etc/logrotate.conf|Konfiguration för Dynamic Linker.|
|Daemons|/etc/httpd.conf|Konfigurationsfilen för Apache, webbservern. Den här filen finns vanligtvis inte i /etc.|
|Användarprogram| /etc/lynx.cfg| Proxyinställningar|
### AWS CONFIG-filexempel
De ofta använda konfigurationsinställningarna och autentiseringsuppgifterna kan sparas i CONFIG-filer som underhålls av AWS CLI. CONFIG-filen måste vara en klartextfil som använder följande format:
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
### Exempel på SSH CONFIG-fil
OpenSSH-konfigurationsfilen på klientsidan heter CONFIG och den lagras i .ssh-katalogen. SSH CONFIG-filen består av följande struktur:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG-filexempel
En Python CONFIG-fil kan se ut så här:

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



## Referenser

* [Förstå Linux-konfigurationsfiler](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Inställningar för konfigurations- och autentiseringsfil](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Konfigurationsfiler i Python](https://martin-thoma.com/configuration-files-in-python/)

