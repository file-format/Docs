{
  "date": "2021-04-23",
  "keywords": [
"config fil",
"konfigurationsfiler",
"config filformat",
"udvidelse",
"format",
"git config-fil",
"Konfigurationsfiler i Linux",
"hvad er en konfigurationsfil",
"Konfigurationsfil php",
"ssh config fil eksempel",
"aws config fil eksempel",
"python config fil eksempel"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG - Konfigurationsfil",
  "description": "Lær om CONFIG filformat med CONFIG eksempel og API'er, der kan oprette og åbne CONFIG filer.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-dag"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er en CONFIG fil?
En CONFIG-fil er kendt som konfigurationsfil; bruges til at konfigurere parametrene og de primære indstillinger for flere computersoftware. Nogle software læser kun deres **konfigurationsfiler** ved deres opstart. Andre kontrollerer regelmæssigt konfigurationsfilerne for ændringer.

## CONFIG filformat
**CONFIG-filformatet** bruges til serverprocesser, softwareapplikationer og operativsystemindstillinger. En programmør kan skrive kode for at instruere en software til at læse konfigurationsfilerne igen og igen efter en bestemt periode og anvende ændringerne til den aktuelle proces. Der er ingen definitive standarder eller stærke konventioner for CONFIG-filsystemet. For eksempel hører Microsofts Web.config-fil til CONFIG-filformatet, som består af et [XML](/web/xml/)-baseret tagsæt; kan redigeres med Microsoft Visual Studio eller enhver anden teksteditor.

## Eksempler på konfigurationsfiler:
Da konfigurationsfilerne ikke er oprettet ved at følge nogen regler, standarder eller konventioner, kan disse filer være skrevet ved at bruge forskellige formater. En .config-fil kan være baseret på XML, [JSON](/web/json/) eller et hvilket som helst andet format. Følgende er eksempler på konfigurationsfiler til velkendte operativsystemer og software:

### Konfigurationsfiler i Linux
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Kategori|Eksempel| Kommentarer|
---|---|---|
|Adgang til filer|/etc/host.conf|Fortæller netværksdomæneserveren, hvordan man slår værtsnavne op.|
|Opstart og login/logud|/etc/rc.d/rc.local|Ikke officielt. Kan kaldes fra rc, rc.sysinit eller /etc/inittab.|
|Filsystem|/etc/mtools.conf|Konfiguration for alle operationer (mkdir, kopi, format osv.) på et DOS-type filsystem.|
|Systemadministration|/etc/shells|Indeholder listen over mulige skaller, der er tilgængelige for systemet.|
|Netværk|/etc/gated.conf|Konfiguration for gated. Bruges kun af den lukkede dæmon.|
|Systemkommandoer|/etc/logrotate.conf|Konfiguration for Dynamic Linker.|
|Daemons|/etc/httpd.conf|Konfigurationsfilen til Apache, webserveren. Denne fil er typisk ikke i /etc.|
|Brugerprogrammer| /etc/lynx.cfg| Proxyindstillinger|
### AWS CONFIG fil eksempel
De ofte brugte konfigurationsindstillinger og legitimationsoplysninger kan gemmes i CONFIG-filer, der vedligeholdes af AWS CLI. CONFIG-filen skal være en almindelig tekstfil, der bruger følgende format:
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
### SSH CONFIG fil eksempel
OpenSSH-konfigurationsfilen på klientsiden hedder CONFIG, og den er gemt i .ssh-mappen. SSH CONFIG-filen består af følgende struktur:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG fil eksempel
En Python CONFIG-fil kunne se sådan ud:

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



## Referencer

 * [Forstå Linux-konfigurationsfiler](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Konfigurationsfiler i Python](https://martin-thoma.com/configuration-files-in-python/)

