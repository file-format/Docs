{
  "date" : "2019-10-11",
  "keywords" :[ "file aba", "formato file aba", "cos'è un file aba", "file", "esempio aba", "estensione file aba", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Formato file CemText",
  "description":"Scopri il formato di file ABA e le API che possono creare e aprire file ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Che cos'è un file ABA?

Un file con estensione .aba è un formato di file dell'Australian Bankers Association (ABA) o [Cemtext](https://www.cemtexaba.com/) utilizzato dalle banche per le transazioni batch. Viene utilizzato dalla maggior parte delle Banche per la tenuta dei registri finanziari. Conosciuto anche come file Direct Entry, il formato di file ABA è stato adottato dalla maggior parte delle banche australiane come formato predefinito per le transazioni batch. Non è ancora stato riconosciuto come formato Standard nonostante sia stato utilizzato da Bank of Queensland, NAB e Westpac. I file ABA possono essere aperti con qualsiasi editor di testo come Notepad ++.


## Formato file ABA

Un file ABA utilizza il formato ASCII per memorizzare i dati per l'inoltro o il caricamento nei sistemi bancari. Il formato è stato mantenuto semplice per facilitare l'integrazione nel sistema finanziario delle aziende per elaborare batch di transazioni. Ad esempio, in un sistema di gestione stipendi, un batch di transazioni può essere caricato per essere elaborato in un colpo solo. Le specifiche del formato di file ABA sono disponibili come trascrizione completa sul sito Web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) e possono essere consultate per riferimento degli sviluppatori .

Un file ABA è costituito da più righe in cui ogni riga è nota come "record". Ci sono tre record principali in un file ABA:

* Record descrittivo
* Registro dei dettagli
* File record totale

### Record descrittivo

Un "Registro descrittivo" contiene informazioni come il numero di sequenza della bobina, il nome dell'istituto finanziario dell'utente, il nome dell'uso che fornisce il file e altre informazioni.

### Record di dettagli

Il tipo "Detail Record" include informazioni come numero di banca/stato/filiale, numero di conto da accreditare/addebitare, indicatore, codice transazione, importo e altre informazioni.

### Record totale file

Il tipo "Record totale file" include Tipo di record 7, Riempitore formato BSB, Importo totale netto file (utente), Importo totale credito file (utente), Importo totale addebito file (utente) e altre informazioni.

### Codici di transazione

Un elenco di codici di transazione validi è il seguente. Il più delle volte, il codice "53 - Pay" viene utilizzato nei file ABA. Questi codici di transazione comprendono debiti, crediti e ritenute d'acconto.

|Codice|Descrizione transazione|
---|---|
|13|Posizioni di addebito avviate esternamente|
|50|Posizioni di credito avviate esternamente ad eccezione di quelle recanti codici di transazione|
|51|Interessi di sicurezza del governo australiano|
|52|Assegno familiare|
|53|Paga|
|54|Pensione|
|55|Riparto|
|56|Divido|
|57|Interessi su obbligazioni/note|

## Esempio di file ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Riferimenti

* [Cemtext ABA](https://www.cemtexaba.com/)

