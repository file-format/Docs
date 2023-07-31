{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "extensie", "fișier", "format", "sistem", "Inițiere", "extensie director", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI – Format fișier de inițiere",
  "description":"Aflați despre formatul de fișier INI și despre API-urile care pot crea și deschide fișiere INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Ce este un fișier INI? ##

Un fișier INI este un document de configurare a mesajelor pentru programe de calculator care conțin chei publice pentru caracteristici și secțiuni care organizează atributele într-un cadru și gramatică. Aceste documente de configurare în format de fișier de sistem își primesc numele de la extensia de director INI a sistemului de operare MS-DOS, care înseamnă inițiere. A popularizat această formă de configurare a software-ului. Multe programe din alte aplicații software folosesc diverse adăugări de nume de fișiere, cum ar fi CONF și [CFG](/ro/system/cfg/), deși formatul a stabilit un standard neoficial în multe situații de configurare.

## Scurt istoric al fișierelor INI##

Inițial, tehnica principală de configurare a programului Windows a fost un format de fișier text care consta din linii de text cu o pereche crucială pe linie, împărțită în secțiuni. Driverele de dispozitiv, fonturile și lansatoarele de pornire au fost toate stocate în acest format. De asemenea, setările individuale au fost stocate în mod obișnuit în fișierele INI de către aplicații.
Până la Windows 3.1x, formatul era acceptat pe platformele Microsoft Windows pe 16 biți. Începând cu Windows 95, Microsoft a început să încurajeze dezvoltatorii să folosească Registrul Windows în loc de fișiere INI pentru configurare.

## Fișier INI - Specificații de format de fișier

### Chei/Proprietăți ###

Cheia/proprietatea este elementul de bază al unui fișier INI. Un simbol egal (=) separă numele și valoarea fiecărei chei. În stânga semnului egal este locul în care se afișează numele. Simbolul egal și punctul și virgulă sunt litere discrete în sistemul Windows, prin urmare, nu pot fi utilizate în cheie. Orice caracter poate fi folosit în valoare.

```
name=value
```

### Secțiuni ###

Comentariul secțiunii apare între paranteze drepte ([]) pe propria linie. După definirea secțiunii, toate cheile sunt legate de acea secțiune. Secțiunile se termină chiar la următoarea desemnare a secțiunii sau la sfârșitul documentului; nu există un separator specific de „sfârșit de secțiune”. Secțiunile nu pot fi stivuite; pot fi denumite o singură dată și nu trebuie să fie conectate.

```
[section]
a=a
b=b
```

### Schimbarea caracteristicilor ###

Formatul de fișier INI nu are o definiție acceptată la nivel global. Multe aplicații de calculator includ și funcții în plus față de cele deja menționate. Lista de mai jos include câteva caracteristici comune care pot fi incluse sau nu în orice program individual.

* Comentarii
* Escape caractere
* Nume duplicat


## Exemplu INI ##

Exemplul de fișier INI arată după cum urmează:

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

## Referință ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

