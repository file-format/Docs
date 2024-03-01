{
  "date": "2021-04-23",
  "keywords": [
"konfigurointitiedosto",
"asetustiedostot",
"config Tiedostomuoto",
"laajennus",
"muoto",
"git asetustiedosto",
"Asetustiedostot Linuxissa",
"mikä on asetustiedosto",
"Asetustiedosto php",
"Esimerkki ssh-asetustiedostosta",
"aws-asetustiedosto esimerkki",
"python-asetustiedosto esimerkki"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG - Asetustiedosto",
  "description": "Opi CONFIG-tiedostomuodosta CONFIG-esimerkillä ja API-liittymillä, jotka voivat luoda ja avata CONFIG-tiedostoja.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-fig"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on CONFIG-tiedosto?
CONFIG-tiedosto tunnetaan konfigurointitiedostona; käytetään parametrien ja ensisijaisten asetusten määrittämiseen useille tietokoneohjelmistoille. Jotkut ohjelmistot lukevat vain **määritystiedostonsa** käynnistyksen yhteydessä. Toiset tarkistavat määritystiedostot säännöllisesti muutosten varalta.

## CONFIG Tiedostomuoto
**CONFIG-tiedostomuotoa** käytetään palvelinprosesseihin, ohjelmistosovelluksiin ja käyttöjärjestelmän asetuksiin. Ohjelmoija voi kirjoittaa koodin ohjeistaakseen ohjelmistoa lukemaan määritystiedostot uudelleen ja uudelleen tietyn ajan kuluttua ja soveltamaan muutoksia nykyiseen prosessiin. CONFIG-tiedoston sysntaksille ei ole olemassa tarkkoja standardeja tai vahvoja käytäntöjä. Esimerkiksi Microsoftin Web.config-tiedosto kuuluu CONFIG-tiedostomuotoon, joka koostuu [XML](/web/xml/)-pohjaisista tunnistejoukoista; voidaan muokata Microsoft Visual Studiolla tai millä tahansa muulla tekstieditorilla.

## Esimerkkejä asetustiedostoista:
Koska asetustiedostoja ei luoda noudattamalla sääntöjä, standardeja tai käytäntöjä, nämä tiedostot on saatettu kirjoitettua käyttämällä eri muotoja. .config-tiedosto voi perustua XML-, {{HYPERLINKKI}}- tai mihin tahansa muuhun muotoon. Seuraavassa on esimerkkejä tunnettujen käyttöjärjestelmien ja ohjelmistojen määritystiedostoista:

### Asetustiedostot Linuxissa
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Luokka|Esimerkki| Kommentit|
---|---|---|
|Käytä tiedostoja|/etc/host.conf|Kertoo verkkoalueen palvelimelle, kuinka isäntänimiä etsitään.|
|Käynnistys ja sisään-/uloskirjautuminen|/etc/rc.d/rc.local|Ei virallinen. Voidaan kutsua osoitteesta rc, rc.sysinit tai /etc/inittab.|
|Tiedostojärjestelmä|/etc/mtools.conf|Kaikkien toimintojen (mkdir, kopiointi, muoto jne.) asetukset DOS-tyyppisessä tiedostojärjestelmässä.|
|Järjestelmänhallinta|/etc/shells|Säilyttää luettelon mahdollisista shells-kuorista järjestelmän käytettävissä.|
|Networking|/etc/gated.conf|Gatedin asetukset. Vain portitetun demonin käyttämä.|
|Järjestelmäkomennot|/etc/logrotate.conf|Dynaamisen linkittimen asetukset.|
|Daemons|/etc/httpd.conf|Web-palvelimen Apachen määritystiedosto. Tämä tiedosto ei yleensä ole /etc.|:ssä
|Käyttäjäohjelmat| /etc/lynx.cfg| Välityspalvelimen asetukset|
### Esimerkki AWS CONFIG -tiedostosta
Usein käytetyt kokoonpanoasetukset ja tunnistetiedot voidaan tallentaa AWS-CLI:n ylläpitämiin CONFIG-tiedostoihin. CONFIG-tiedoston on oltava pelkkä tekstitiedosto, joka käyttää seuraavaa muotoa:
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
### Esimerkki SSH CONFIG -tiedostosta
OpenSSH-asiakaspuolen määritystiedosto on nimeltään CONFIG, ja se tallennetaan .ssh-hakemistoon. SSH CONFIG -tiedosto koostuu seuraavasta rakenteesta:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG -tiedostoesimerkki
Python CONFIG -tiedosto voisi näyttää tältä:

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



## Viitteet

 * [Linux-määritystiedostojen ymmärtäminen](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Pythonin määritystiedostot](https://martin-thoma.com/configuration-files-in-python/)

