{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Configuratiebestand",
  "description":"Meer informatie over de CONFIG-bestandsindeling met CONFIG-voorbeeld en API's die CONFIG-bestanden kunnen maken en openen.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een CONFIG-bestand?
Een CONFIG-bestand staat bekend als configuratiebestand; gebruikt om de parameters en primaire instellingen voor verschillende computersoftware te configureren. Sommige software lezen hun **configuratiebestanden** pas bij het opstarten. Anderen controleren de configuratiebestanden regelmatig op wijzigingen.

## CONFIG-bestandsindeling
De **CONFIG-bestandsindeling** wordt gebruikt voor serverprocessen, softwaretoepassingen en instellingen van het besturingssysteem. Een programmeur kan code schrijven om een software te instrueren om de configuratiebestanden na een bepaalde periode steeds opnieuw te lezen en de wijzigingen op het huidige proces toe te passen. Er zijn geen definitieve standaarden of sterke conventies voor CONFIG-bestandssysntax. Het Web.config-bestand van Microsoft behoort bijvoorbeeld tot de CONFIG-bestandsindeling, die bestaat uit op [XML](https://docs.fileformat.com/web/xml/) gebaseerde tagsets; kan worden bewerkt met Microsoft Visual Studio of een andere teksteditor.

## Voorbeelden van configuratiebestanden:
Aangezien de configuratiebestanden niet zijn gemaakt door het volgen van regels, standaarden of conventies, zijn deze bestanden mogelijk geschreven met verschillende indelingen. Een .config-bestand kan gebaseerd zijn op XML, [JSON](https://docs.fileformat.com/web/json/) of een ander formaat. Hieronder volgen de voorbeelden van configuratiebestanden voor bekende besturingssystemen en software:

### Configuratiebestanden in Linux
Elk Linux-programma is een uitvoerbaar bestand met de lijst van **opcodes** die de CPU uitvoert om typische bewerkingen uit te voeren. De bewerkingen van bijna elk programma kunnen aan uw eisen worden aangepast door de configuratiebestanden te wijzigen. Verschillende configuratiebestanden in het Linux-systeem bevinden zich in de map /etc. De configuratiebestanden kunnen in de volgende categorieën worden ingedeeld:
|Categorie|Voorbeeld| Opmerkingen|
---|---|---|
|Toegang tot bestanden|/etc/host.conf|Vertelt de netwerkdomeinserver hoe hostnamen moeten worden opgezocht.|
|Opstarten en inloggen/uitloggen|/etc/rc.d/rc.local|Niet officieel. Kan worden aangeroepen vanuit rc, rc.sysinit of /etc/inittab.|
|Bestandssysteem|/etc/mtools.conf|Configuratie voor alle bewerkingen (mkdir, kopiëren, formatteren, etc.) op een DOS-bestandssysteem.|
|Systeembeheer|/etc/shells|Bewaart de lijst met mogelijke "shells" die beschikbaar zijn voor het systeem.|
|Netwerken|/etc/gated.conf|Configuratie voor gated. Alleen gebruikt door de gated daemon.|
|Systeemcommando's|/etc/logrotate.conf|Configuratie voor de Dynamic Linker.|
|Daemons|/etc/httpd.conf|Het configuratiebestand voor Apache, de webserver. Dit bestand staat meestal niet in /etc.|
|Gebruikersprogramma's| /etc/lynx.cfg| Proxy-instellingen|
### AWS CONFIG-bestand voorbeeld
De veelgebruikte configuratie-instellingen en referenties kunnen worden opgeslagen in CONFIG-bestanden die worden onderhouden door de AWS CLI. Het CONFIG-bestand moet een tekstbestand zijn met de volgende indeling:
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
### SSH CONFIG-bestand voorbeeld
Het configuratiebestand aan de clientzijde van OpenSSH heet CONFIG en wordt opgeslagen in de .ssh-directory. Het SSH CONFIG-bestand bestaat uit de volgende structuur:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG-bestand voorbeeld
Een Python CONFIG-bestand kan er als volgt uitzien:

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



## Referenties

* [Linux-configuratiebestanden begrijpen](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Instellingen voor configuratie- en referentiebestanden](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Configuratiebestanden in Python](https://martin-thoma.com/configuration-files-in-python/)

