{
  "date": "2021-04-23",
  "keywords": [
"konfigurācijas fails",
"konfigurācijas faili",
"konfigurācijas faila formāts",
"pagarinājumu",
"formātā",
"git konfigurācijas fails",
"Konfigurācijas faili operētājsistēmā Linux",
"kas ir konfigurācijas fails",
"Konfigurācijas fails php",
"ssh konfigurācijas faila piemērs",
"aws konfigurācijas faila piemērs",
"python konfigurācijas faila piemērs"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG — konfigurācijas fails",
  "description": "Uzziniet par CONFIG faila formātu, izmantojot CONFIG piemēru un API, kas var izveidot un atvērt CONFIG failus.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-lvg"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir CONFIG fails?
CONFIG fails ir pazīstams kā konfigurācijas fails; izmanto, lai konfigurētu parametrus un primāros iestatījumus vairākām datoru programmatūrām. Dažas programmatūras palaišanas laikā nolasa tikai savus **konfigurācijas failus**. Citi periodiski pārbauda, vai konfigurācijas failos nav veiktas izmaiņas.

## CONFIG Faila formāts
**CONFIG faila formāts** tiek izmantots servera procesiem, programmatūras lietojumprogrammām un operētājsistēmas iestatījumiem. Programmētājs var rakstīt kodu, lai norādītu programmatūrai pēc noteikta laika atkal un atkal lasīt konfigurācijas failus un piemērot izmaiņas pašreizējam procesam. CONFIG faila sintaksei nav noteiktu standartu vai stingru konvenciju. Piemēram, Microsoft Web.config fails pieder CONFIG faila formātam, kas sastāv no tagu kopām, kuru pamatā ir [XML](/web/xml/); var rediģēt ar Microsoft Visual Studio vai jebkuru citu teksta redaktoru.

## Konfigurācijas failu piemēri:
Tā kā konfigurācijas faili netiek izveidoti, ievērojot nekādus noteikumus, standartus vai konvencijas, šie faili var būt ierakstīti, izmantojot dažādus formātus. .config fails var būt balstīts uz XML, [JSON](/web/json/) vai jebkuru citu formātu. Tālāk ir sniegti labi zināmu operētājsistēmu un programmatūras konfigurācijas failu piemēri.

### Konfigurācijas faili operētājsistēmā Linux
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Kategorija|Piemērs| Komentāri|
---|---|---|
|Piekļuve failiem|/etc/host.conf|Pasaka tīkla domēna serverim, kā meklēt resursdatora nosaukumus.|
|Sāknēšana un pieteikšanās/atteikšanās|/etc/rc.d/rc.local|Nav oficiāla. Var izsaukt no rc, rc.sysinit vai /etc/inittab.|
|Failu sistēma|/etc/mtools.conf|Konfigurācija visām darbībām (mkdir, kopēšana, formāts utt.) DOS tipa failu sistēmā.|
|Sistēmas administrēšana|/etc/shells|Satur sistēmai pieejamo iespējamo čaulu” sarakstu.|
|Networking|/etc/gated.conf|Konfigurācija vārtiem. Izmanto tikai ierobežotais dēmons.|
|Sistēmas komandas|/etc/logrotate.conf|Dinamiskā linkera konfigurācija.|
|Daemons|/etc/httpd.conf|Apache, tīmekļa servera, konfigurācijas fails. Šis fails parasti neatrodas mapē /etc.|
|Lietotāju programmas| /etc/lynx.cfg| Starpniekservera iestatījumi|
### AWS CONFIG faila piemērs
Bieži lietotos konfigurācijas iestatījumus un akreditācijas datus var saglabāt CONFIG failos, kurus uztur AWS CLI. CONFIG failam ir jābūt vienkārša teksta failam, kas izmanto šādu formātu:
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
### SSH CONFIG faila piemērs
OpenSSH klienta puses konfigurācijas faila nosaukums ir CONFIG, un tas tiek saglabāts .ssh direktorijā. SSH CONFIG fails sastāv no šādas struktūras:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG faila piemērs
Python CONFIG fails varētu izskatīties šādi:

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



## Atsauces

 * [Informācija par Linux konfigurācijas failiem](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Konfigurācijas faili programmā Python](https://martin-thoma.com/configuration-files-in-python/)

