{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "file", "estensione", "formato file", "Valori separati da virgola", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file CSV e le API che possono creare e aprire file CSV.",
  "title" :"Formato file CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file CSV?

I file con estensione .csv (Comma Separated Values) rappresentano file di testo normale che contengono record di dati con valori separati da virgole. Ogni riga in un file CSV è un nuovo record dall'insieme di record contenuti nel file. Tali file vengono generati quando si intende trasferire i dati da un sistema di archiviazione a un altro. Poiché tutte le applicazioni possono riconoscere record separati da virgole, l'importazione di tali file di dati nel database viene eseguita in modo molto conveniente. Quasi tutte le applicazioni per fogli di calcolo come Microsoft Excel o OpenOffice Calc possono importare CSV senza troppi sforzi. I dati importati da tali file sono organizzati in celle di un foglio di calcolo per la rappresentazione all'utente.

## Breve storia ##

Di seguito sono riportati alcuni brevi fatti sull'origine e la cronologia del formato di file CSV.

* 1972 - Il compilatore IBM Fortran (livello H esteso) li supportava sotto OS/360

* 1978 - L'input/output diretto dall'elenco è stato supportato da FORTRAN 77 che utilizzava virgole e spazi per i delimitatori

* 2005 - CSV è stato standardizzato con [RFC4180](https://tools.ietf.org/html/rfc4180) come tipo di contenuto MIME.

* 2013 - Le carenze di RFC4180 sono state gestite da una raccomandazione del W3C

* 2015 - Il W3C ha realizzato le prime bozze di raccomandazioni per gli standard dei metadati CSV, iniziate come raccomandazione nel dicembre 2015

## Converti file CSV ##

I file CSV possono essere convertiti in diversi formati di file utilizzando le applicazioni in grado di aprire questi file. Ad esempio, Microsoft Excel può importare dati dal formato di file CSV e salvarli in XLS, [XLSX](/it/spreadsheet/xlsx/), [PDF](/it/pdf/), [TXT](/it/word-processing/txt/) , XML e [HTML](/it/web/html/). Allo stesso modo, altri servizi desktop e online offrono la possibilità di esportare file CSV in HTML, ODS e [RTF](/it/word-processing/rtf/).

## Formato file CSV ##

È noto che il formato del file CSV è specificato in [RFC4180](https://tools.ietf.org/html/rfc4180). Definisce qualsiasi file conforme a CSV se:

* Ogni record si trova su una riga separata, delimitata da un'interruzione di riga (CRLF). Per esempio:
* aaa,bbb,ccc CRLF
* zzz,aaa,xxx CRLF
* L'ultimo record nel file può avere o meno un'interruzione di riga finale. Per esempio:
* aaa,bbb,ccc CRLF
* zzz, aaa, xxx
* Potrebbe esserci una riga di intestazione opzionale che appare come prima riga del file con lo stesso formato delle normali righe di record. Tale intestazione conterrà i nomi corrispondenti ai campi del file e dovrà contenere lo stesso numero di campi dei record nel resto del file (la presenza o l'assenza della riga di intestazione deve essere indicata tramite il parametro facoltativo "intestazione" di questo tipo MIME). Per esempio:
* nome_campo, nome_campo, nome_campo CRLF
* aaa,bbb,ccc CRLF
* zzz,aaa,xxx CRLF
* ﻿All'interno dell'intestazione e di ogni record possono essere presenti uno o più campi, separati da virgole. Ogni riga dovrebbe contenere lo stesso numero di campi in tutto il file. Gli spazi sono considerati parte di un campo e non devono essere ignorati. L'ultimo campo del record non deve essere seguito da una virgola. Per esempio:
* aaa, bbb, ccc
* Ciascun campo può essere racchiuso o meno tra virgolette doppie (tuttavia alcuni programmi, come Microsoft Excel, non utilizzano affatto le virgolette). Se i campi non sono racchiusi tra virgolette doppie, è possibile che le virgolette doppie non vengano visualizzate all'interno dei campi. Per esempio:\
* CRLF "aaa", "bbb", "ccc".
* zzz, aaa, xxx
* I campi contenenti interruzioni di riga (CRLF), virgolette e virgole devono essere racchiusi tra virgolette. Per esempio:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz, aaa, xxx
* Se le virgolette doppie vengono utilizzate per racchiudere i campi, è necessario eseguire l'escape di una virgoletta doppia che appare all'interno di un campo precedendola con un'altra virgoletta doppia. Per esempio:
* "aaa","b""bb","ccc"

Tuttavia, alla luce dell'uso moderno, il delimitatore non è limitato alla sola virgola e può essere anche punto e virgola, tabulazione o spazi. Applicazioni come Microsoft Excel offrono l'opzione per specificare il carattere delimitatore per l'importazione di record da un file CSV.

## Riferimenti

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

