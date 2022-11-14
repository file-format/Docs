{
  "date" : "2019-10-11",
  "keywords" :[ "html","file html", "formato file html", "tipo di file html", "file", "tipo", "che cos'è un file html" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file HTML",
  "description":"Scopri il formato di file HTML e le API che possono creare e aprire file HTML.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file HTML?

HTML (Hyper Text Markup Language) è l'estensione per le pagine web create per la visualizzazione nei browser. Conosciuto come linguaggio del web, l'HTML si è evoluto con i requisiti di nuovi requisiti informativi da visualizzare come parte delle pagine web. L'ultima variante è nota come HTML 5 che offre molta flessibilità per lavorare con la lingua. Le pagine HTML vengono ricevute dal server, dove sono ospitate, oppure possono essere caricate anche dal sistema locale. Ogni pagina HTML è composta da elementi HTML come moduli, testo, immagini, animazioni, collegamenti, ecc. Questi elementi sono rappresentati da tag e molti altri in cui ogni tag ha inizio e fine. Può anche incorporare applicazioni scritte in linguaggi di scripting come JavaScript e fogli di stile (CSS) per la rappresentazione generale del layout.

## Breve storia ##

Sin dal suo inizio e dalla prima implementazione, le specifiche HTML sono state mantenute dal World Wide Web Consortium (W3C) dal 1996. Nel 2000 sono diventate anche uno standard internazionale (ISO/IEC 15445:2000). Nel 1999 è stato pubblicato HTML 4.01. Nel 2004, il Web Hypertext Application Technology Working Group (WHATWG) ha iniziato a lavorare sulla versione HTML5 che è diventata un prodotto congiunto con il W3C nel 2008. È stata completata e standardizzata il 28 ottobre 2014.

## Struttura del formato file HTML ##

Un documento HTML 4 è composto da tre parti:

1. una riga contenente informazioni sulla versione HTML
1. una sezione di intestazione dichiarativa
1. un corpo, che contiene il contenuto effettivo del documento. Il corpo può essere implementato dall'elemento BODY o dall'elemento FRAMESET per contenere il corpo in frame

Ogni sezione può essere iniziale o seguita da spazi bianchi, newline, tabulazioni e commenti. Un esempio di un semplice documento HTML è il seguente:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Informazioni sulla versione ###

La prima riga di codice, \<!DOCTYPE html> , è chiamata dichiarazione doctype e indica al browser in quale versione di HTML è scritta la pagina. A seconda della versione di HTML, esistono diverse dichiarazioni di doctype che denominano la definizione del tipo di documento (DTD) in uso per il documento. Ogni DTD differisce dagli altri per gli elementi che supporta e differiscono come segue:

* HTML 4.01 Strict - include tutti gli elementi e gli attributi che non sono stati [deprecati](https://www.w3.org/TR/html401/conform.html#deprecated) o non compaiono nei documenti del set di frame
* HTML 4.01 Transitional - include tutto nella DTD rigorosa più elementi e attributi deprecati (la maggior parte dei quali riguarda la presentazione visiva
* HTML 4.01 Frameset - include tutto anche nel DTD di transizione più i frame

Per **HTML5**, le informazioni sulla versione sono semplicemente come indicato di seguito.

```
<!DOCTYPE html>
```

### Informazioni sull'intestazione HTML ###

L'intestazione di un documento HTML può includere un numero di elementi HTML che non vengono visualizzati dal browser. Tali elementi sono metadati che descrivono informazioni sulla pagina o includono sezioni utilizzate per recuperare informazioni da risorse esterne come fogli di stile CSS o file JavaScript. L'intestazione di una pagina è rappresentata dal tag head.

Per impostare il titolo della pagina, l'elemento **titolo** è l'unico richiesto all'interno del<head> tag. Lo stesso viene utilizzato dai motori di ricerca per identificare il titolo di una pagina.

### Informazioni sul corpo HTML ###

Questa è la sezione principale del file che contiene tutti i contenuti del file che vengono visualizzati dai browser. Il corpo HTML può contenere markup che possono fare riferimento a vari blocchi costitutivi sotto forma di tag. Può contenere diversi tipi di informazioni come testo, immagini, colori, grafica, ecc. Inoltre, gli elementi audio e video possono anche essere incorporati nel corpo html per il rendering da parte dei browser. In presenza di moderne applicazioni di fogli di stile per la rappresentazione visiva, gli attributi di presentazione di BODY come il colore di sfondo, il colore del collegamento, il colore del testo, ecc. sono stati deprecati. Pertanto, gli stessi effetti possono essere ottenuti utilizzando fogli di stile come mostrato di seguito:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

I fogli di stile in linea sono facili da incorporare e per applicazioni rapide agli effetti visivi, i fogli di stile esterni lo rendono più comodo da distribuire una volta e accedervi in più punti.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Elementi HTML ###

Come accennato in precedenza, i contenuti all'interno del corpo HTML sono rappresentati da tag, noti anche come elementi HTML. Ogni tag può avere informazioni aggiuntive sotto forma di attributi che sono scritti come<tag attribute1#"value1" attribute2#"value2"> , sebbene non sia necessario avere attributi con ogni tag. Se gli attributi non sono menzionati, in ogni caso vengono utilizzati i valori predefiniti. Di seguito sono riportati alcuni degli esempi di Element:

#### Intestazione ####

```
<head>
  <title>The Title</title>
</head>
```

#### Intestazioni ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragrafi ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Riferimenti ##

* [La struttura globale del documento HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

