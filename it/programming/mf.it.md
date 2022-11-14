{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Formato file manifest Java",
  "description":"Scopri il formato di file MF e le API che possono creare e aprire file MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file MF?

Un file con estensione .mf è un file Manifest Java che contiene informazioni sulle singole voci del file [JAR](/it/programming/jar/). Il file MF stesso è contenuto all'interno del file JAR e fornisce tutta l'estensione e la definizione relativa al pacchetto. I file JAR possono essere prodotti per essere utilizzati come file eseguibili. In tal caso, il file mainfest specifica la classe principale dell'applicazione che contiene l'istruzione **`public static void main`**. I file manifest sono denominati MANIFEST.MF e possono essere aperti con qualsiasi editor di testo su sistemi operativi Windows, MacOS e Linux.

## Specifiche del formato file manifest

[Specifiche del formato file manifest](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) sono disponibili da Oracle nella loro guida per il formato file JAR. Un file manifest è composto da sezioni principali seguite da un elenco di sezioni per singole voci di file JAR. Ogni sezione segue alcune regole e restrizioni.

### Sezioni principali

Una sezione principale:

* contiene informazioni sulla sicurezza e la configurazione del file JAR
* contiene informazioni sull'applicazione o sull'estensione di cui fa parte il file JAR
* definisce gli attributi principali per ogni singolo elemento del manifest

**Nota**: nessun attributo in questa sezione può essere denominato "Nome".

### Sezioni individuali

Una singola sezione definisce vari attributi per pacchetti o file di un file JAR. Ogni sezione deve iniziare con un attributo denominato "Nome" il cui valore deve essere un percorso relativo al file o un URL assoluto che fa riferimento a dati esterni all'archivio.

### Specifiche del manifesto

|Attributi|Descrizione|
---|---|
|file-manifest|nuova riga della sezione principale *sezione-individuale|
|sezione-principale|info-versione nuova riga *attributo-principale|
|info-versione|Versione-manifest: numero-versione|
|numero-versione|cifra+{.cifra+}*|
|attributo-principale|(qualsiasi attributo principale legittimo) newline|
|sezione-individuale|Nome : valore newline *attributo-perentry|
|perentry-attribute|(qualsiasi attributo perentry legittimo) newline|
|nuova riga|CR LF | LF | CR (non seguito da LF)|
|cifra|{0-9}|

## Riferimenti

* [Oracle - Formato file JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Formato file JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,in%20one%20file%20for% 20distribution.&text=Loro%20sono%20costruiti%20su%20estensione,jar%20file%20.)

