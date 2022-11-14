{
  "date" : "2021-04-08",
  "keywords" :[ "file deb", "formato file deb", "cos'è un file deb", "file", "esempio deb", "estensione file deb", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Archivio Tar compresso Bzip",
  "description":"Scopri il formato di file DEB e le API che possono creare e aprire file DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Che cos'è un file DEB?

Un file con estensione .deb è un formato di file di pacchetto binario Debian disponibile per la distribuzione di pacchetti software su sistema operativo Linux. È costituito da due file di archivio [TAR](/it/compression/tar/). Il DPKG fornisce il meccanismo per leggere e installare i pacchetti DEB. I pacchetti DEB possono essere installati utilizzando l'interfaccia di gestione del software del pacchetto APT. I file DEB hanno Internet Media Type come `application/vnd.debian.binary-package`.

## Formato file DEB

Un file DEB è costituito da due file di archivio [TAR](/it/compression/tar/). Un archivio contiene le informazioni di controllo e un altro contiene i dati installabili.

### Organizzazione del pacchetto

Il file DEB è un file di archivio **ar** che ha un valore magico di `!<arch> `. A partire da Debian 0.93, il meccanismo di archiviazione dei file DEB contiene tre file in un ordine specifico.

1. `Debian Binary` - È destinato ad avere una serie di righe, separate da nuove righe. Al momento, è presente solo una singola riga che descrive il numero di versione. Il numero di versione corrente è 2.0.
1. `Control Archive` - Contiene un archivio control.tar che ha script di manutenzione e meta-informazioni sul pacchetto come nome del pacchetto, versione, dipendenze e manutentore.
1. `Data Archive` - È un archivio tar chiamato data.tar e contiene i file multimediali installabili effettivi. L'archivio può essere compresso con gz, bz2, lzma o xz e l'estensione del file dell'archivio dati cambia di conseguenza.

### Archivio di controllo

L'archivio di controllo può includere i contenuti come segue.

* `control` - Contiene una breve descrizione del pacchetto e altre informazioni come le sue dipendenze.
* `md5sums` - Contiene i checksum MD5 di tutti i file nel pacchetto per rilevare file corrotti o incompleti.
* `conffiles` - Elenca i file del pacchetto che dovrebbero essere trattati come file di configurazione. I file di configurazione non vengono sovrascritti durante un aggiornamento a meno che non sia specificato.
* `preinst`, postinst, prerm e postrm - Script opzionali che vengono eseguiti prima o dopo l'installazione o la rimozione del pacchetto
* `config` è uno script opzionale che supporta il meccanismo di configurazione debconf.
* `shlibs` - È un elenco di dipendenze di librerie condivise.

## Riferimenti

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Formato pacchetto binario Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

