{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Fișier de configurare",
  "description":"Aflați despre formatul fișierului CONFIG cu exemplul CONFIG și API-urile care pot crea și deschide fișiere CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Ce este un fișier CONFIG?
Un fișier CONFIG este cunoscut ca fișier de configurare; folosit pentru a configura parametrii și setările primare pentru mai multe programe de calculator. Unele programe software își citesc **fișierele de configurare** doar la pornire. Alții verifică periodic fișierele de configurare pentru modificări.

## CONFIG Format de fișier
Formatul **CONFIG File** este utilizat pentru procesele serverului, aplicațiile software și setările sistemului de operare. Un programator poate scrie cod pentru a instrui un software să citească fișierele de configurare din nou și din nou după o anumită perioadă de timp și să aplice modificările procesului curent. Nu există standarde definitive sau convenții puternice pentru sintaxa fișierelor CONFIG. De exemplu, fișierul Web.config al Microsoft aparține formatului de fișier CONFIG, care constă dintr-un set de etichete bazat pe [XML](/web/xml/); poate fi editat cu Microsoft Visual Studio sau orice alt editor de text.

## Exemple de fișiere de configurare:
Deoarece fișierele de configurare nu sunt create respectând nicio regulă, standard sau convenție, este posibil ca aceste fișiere să fi scris folosind diferite formate. Un fișier .config se poate baza pe XML, [JSON](/web/json/) sau orice alt format. Următoarele sunt exemple de fișiere de configurare pentru sisteme de operare și software bine cunoscute:

### Fișiere de configurare în Linux
Fiecare program Linux este un fișier executabil care păstrează lista de **coduri operaționale** pe care CPU le execută pentru a realiza operațiuni tipice. Operațiunile aproape fiecărui program pot fi personalizate conform cerințelor dumneavoastră prin modificarea fișierelor de configurare. Mai multe fișiere de configurare din sistemul Linux se află în directorul /etc. Fișierele de configurare pot fi clasificate în următoarele categorii:
|Categorie|Exemplu| Comentarii|
---|---|---|
|Fișiere de acces|/etc/host.conf|Spune serverului de domeniu de rețea cum să caute numele de gazdă.|
|Pornire și autentificare/logout|/etc/rc.d/rc.local|Nu este oficial. Poate fi apelat din rc, rc.sysinit sau /etc/inittab.|
|Sistem de fișiere|/etc/mtools.conf|Configurare pentru toate operațiunile (mkdir, copiere, format, etc.) pe un sistem de fișiere de tip DOS.|
|Administrare sistem|/etc/shells|Pastreaza lista de posibile „shell-uri” disponibile sistemului.|
|Rețea|/etc/gated.conf|Configurare pentru gated. Folosit numai de daemonul îngăduit.|
|Comenzi de sistem|/etc/logrotate.conf|Configurare pentru Dynamic Linker.|
|Daemons|/etc/httpd.conf|Fișierul de configurare pentru Apache, serverul Web. Acest fișier nu este de obicei în /etc.|
|Programe utilizator| /etc/lynx.cfg| Setări proxy|
### Exemplu de fișier AWS CONFIG
Setările de configurare utilizate frecvent și acreditările pot fi salvate în fișierele CONFIG care sunt menținute de AWS CLI. Fișierul CONFIG trebuie să fie un fișier text simplu care utilizează următorul format:
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
### Exemplu de fișier SSH CONFIG
Fișierul de configurare pe partea clientului OpenSSH se numește CONFIG și este stocat în directorul .ssh. Fișierul SSH CONFIG constă din următoarea structură:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Exemplu de fișier Python CONFIG
Un fișier Python CONFIG ar putea arăta astfel:

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



## Referințe

* [Înțelegerea fișierelor de configurare Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Setări ale fișierului de configurare și acreditări](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Fișiere de configurare în Python](https://martin-thoma.com/configuration-files-in-python/)

