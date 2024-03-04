{
  "date": "2021-04-23",
  "keywords": [
"konfigūracijos failas",
"konfigūracijos failus",
"config Failo formatas",
"pratęsimas",
"formatu",
"git konfigūracijos failą",
"Konfigūracijos failai Linux",
"kas yra konfigūracijos failas",
"Konfigūracijos failas php",
"ssh konfigūracijos failo pavyzdys",
"aws konfigūracijos failo pavyzdys",
"python konfigūracijos failo pavyzdys"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG – konfigūracijos failas",
  "description": "Sužinokite apie CONFIG failo formatą naudodami CONFIG pavyzdį ir API, kurios gali kurti ir atidaryti CONFIG failus.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-ltg"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra CONFIG failas?
CONFIG failas yra žinomas kaip konfigūracijos failas; naudojamas kelių kompiuterių programinės įrangos parametrams ir pirminiams parametrams konfigūruoti. Kai kurios programinės įrangos **konfigūracijos failus** nuskaito tik paleidžiant. Kiti periodiškai tikrina, ar konfigūracijos failuose nėra pakeitimų.

## CONFIG Failo formatas
**CONFIG failo formatas** naudojamas serverio procesams, programinės įrangos programoms ir operacinės sistemos nustatymams. Programuotojas gali parašyti kodą, kad nurodytų programinei įrangai vėl ir vėl skaityti konfigūracijos failus po tam tikro laikotarpio ir pritaikyti pakeitimus dabartiniam procesui. CONFIG failo sistemai nėra jokių galutinių standartų ar griežtų konvencijų. Pavyzdžiui, Microsoft Web.config failas priklauso CONFIG failo formatui, kurį sudaro [XML](/web/xml/) pagrįsti žymų rinkiniai; galima redaguoti naudojant Microsoft Visual Studio arba bet kurį kitą teksto rengyklę.

## Konfigūracijos failų pavyzdžiai:
Kadangi konfigūracijos failai nėra sukurti laikantis jokių taisyklių, standartų ar susitarimų, šie failai galėjo būti parašyti naudojant skirtingus formatus. .config failas gali būti pagrįstas XML, [JSON](/web/json/) arba bet kokiu kitu formatu. Toliau pateikiami gerai žinomų operacinių sistemų ir programinės įrangos konfigūracijos failų pavyzdžiai:

### Konfigūracijos failai sistemoje Linux.
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Kategorija|Pavyzdys| Komentarai|
---|---|---|
|Prieiga prie failų|/etc/host.conf|Nurodo tinklo domeno serveriui, kaip ieškoti prieglobos pavadinimų.|
|Paleidimas ir prisijungimas/atsijungimas|/etc/rc.d/rc.local|Ne oficialus. Gali būti iškviečiamas iš rc, rc.sysinit arba /etc/inittab.|
|Failų sistema|/etc/mtools.conf|Visų operacijų (mkdir, kopijavimo, formato ir kt.) DOS tipo failų sistemoje konfigūracija.|
|Sistemos administravimas|/etc/shells|Palaiko galimų sistemai prieinamų apvalkalų sąrašą.|
|Tinklo kūrimas|/etc/gated.conf|Konfigūracija, skirta vartams. Naudoja tik blokuojamas demonas.|
|Sistemos komandos|/etc/logrotate.conf|Dynamic Linker konfigūracija.|
|Daemons|/etc/httpd.conf|Apache, žiniatinklio serverio, konfigūracijos failas. Šio failo paprastai nėra /etc.|
|Vartotojo programos| /etc/lynx.cfg| Tarpinio serverio nustatymai|
### AWS CONFIG failo pavyzdys
Dažnai naudojami konfigūracijos nustatymai ir kredencialai gali būti išsaugoti CONFIG failuose, kuriuos prižiūri AWS CLI. CONFIG failas turi būti paprasto teksto failas, kuriame naudojamas toks formatas:
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
### SSH CONFIG failo pavyzdys
OpenSSH kliento konfigūracijos failas pavadintas CONFIG ir saugomas .ssh kataloge. SSH CONFIG failą sudaro tokia struktūra:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG failo pavyzdys
Python CONFIG failas gali atrodyti taip:

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



## Nuorodos

 * [Linux konfigūracijos failų supratimas](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Python konfigūracijos failai](https://martin-thoma.com/configuration-files-in-python/)

