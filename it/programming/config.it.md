{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - File di configurazione",
  "description":"Scopri il formato di file CONFIG con l'esempio CONFIG e le API che possono creare e aprire file CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file CONFIG?
Un file CONFIG è noto come file di configurazione; utilizzato per configurare i parametri e le impostazioni primarie per diversi software per computer. Alcuni software leggono i loro **file di configurazione** solo all'avvio. Altri controllano periodicamente i file di configurazione per le modifiche.

## CONFIG Formato file
Il **formato file CONFIG** viene utilizzato per i processi server, le applicazioni software e le impostazioni del sistema operativo. Un programmatore può scrivere codice per istruire un software a leggere i file di configurazione ancora e ancora dopo un certo periodo di tempo e ad applicare le modifiche al processo corrente. Non ci sono standard definitivi o convenzioni forti per la sintassi dei file CONFIG. Ad esempio, il file Web.config di Microsoft appartiene al formato di file CONFIG, che consiste in un set di tag basato su [XML](https://docs.fileformat.com/web/xml/); può essere modificato con Microsoft Visual Studio o qualsiasi altro editor di testo.

## Esempi di file di configurazione:
Poiché i file di configurazione non vengono creati seguendo regole, standard o convenzioni, questi file potrebbero essere stati scritti utilizzando formati diversi. Un file .config potrebbe essere basato su XML, [JSON](https://docs.fileformat.com/web/json/) o qualsiasi altro formato. Di seguito sono riportati esempi di file di configurazione per sistemi operativi e software noti:

### File di configurazione in Linux
Ogni programma Linux è un file eseguibile che mantiene l'elenco di **opcode** che la CPU esegue per eseguire operazioni tipiche. Le operazioni di quasi tutti i programmi possono essere personalizzate in base alle proprie esigenze modificandone i file di configurazione. Diversi file di configurazione nel sistema Linux si trovano nella directory /etc. I file di configurazione possono essere classificati nelle seguenti categorie:
|Categoria|Esempio| Commenti|
---|---|---|
|Accesso ai file|/etc/host.conf|Indica al server del dominio di rete come cercare i nomi host.|
|Avvio e login/logout|/etc/rc.d/rc.local|Non ufficiale. Può essere chiamato da rc, rc.sysinit o /etc/inittab.|
|File system|/etc/mtools.conf|Configurazione per tutte le operazioni (mkdir, copia, formattazione, ecc.) su un filesystem di tipo DOS.|
|Amministrazione del sistema|/etc/shells|Contiene l'elenco delle possibili "shell" disponibili per il sistema.|
|Rete|/etc/gated.conf|Configurazione per gated. Utilizzato solo dal demone gated.|
|Comandi di sistema|/etc/logrotate.conf|Configurazione per Dynamic Linker.|
|Daemons|/etc/httpd.conf|Il file di configurazione per Apache, il server Web. Questo file in genere non è in /etc.|
|Programmi utente| /etc/lynx.cfg| Impostazioni proxy|
### Esempio di file CONFIG AWS
Le impostazioni di configurazione e le credenziali utilizzate di frequente possono essere salvate in file CONFIG gestiti dall'AWS CLI. Il file CONFIG deve essere un file di testo normale che utilizza il seguente formato:
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
### Esempio di file CONFIG SSH
Il file di configurazione lato client di OpenSSH è denominato CONFIG ed è archiviato nella directory .ssh. Il file SSH CONFIG è costituito dalla seguente struttura:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Esempio di file CONFIG Python
Un file Python CONFIG potrebbe assomigliare a questo:

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



## Riferimenti

* [Informazioni sui file di configurazione di Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Impostazioni file di configurazione e credenziali](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [File di configurazione in Python](https://martin-thoma.com/configuration-files-in-python/)

