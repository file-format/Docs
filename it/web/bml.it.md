{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file BML - File del linguaggio di markup Bean",
  "description":"Scopri il formato di file BML e le API che possono creare e aprire file BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Che cos'è un file BML?

Un file con estensione .bml è un file Bean Markup Language che memorizza le classi Java per supportare le app Java. Ciò consente l'accesso a oggetti e metodi Java e non è necessario creare nuove funzionalità utilizzando le classi Java. Specifica come i componenti sono collegati tra loro per eseguire attività utili. BML è stato sviluppato da IBM alphaWorks per descrivere le strutture e le relazioni dei componenti. I file BML possono essere aperti e visualizzati utilizzando qualsiasi editor di testo come browser Web, Microsoft Notepad e Notepad ++.

## Formato file BML

Il sito Web di IBM alphaworks ha fornito due implementazioni di BML. La prima implementazione è un interprete che "riproduce" uno script BML per generare la gerarchia di bean desiderata. La seconda implementazione è un compilatore che compila qualsiasi script BML in codice Java privo di riflessi. Ciò è vantaggioso nel senso che consente di acquisire la struttura intercomponente dell'applicazione utilizzando un linguaggio progettato per questo scopo specifico con la possibilità aggiuntiva di compilarlo in codice Java "normale".

## Tag BML

Quella che segue è una spiegazione di alcuni dei tag utilizzati nel linguaggio BML:

### Il<bean> etichetta:

Il<bean> viene utilizzato per creare nuovi bean o per cercare i bean per nome. Il<bean> il tag è del formato:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
L'"id" nel tag è associato al registro degli oggetti per JavaBean.

### Il<string> etichetta

Esistono due modi in cui è possibile utilizzare il tag stringa:

1. Per creare una stringa non vuota:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Per creare una stringa vuota:

```
<string/>
```
## Riferimenti

* [Messaggistica orientata agli oggetti con XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)


