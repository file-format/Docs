{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "che cos'è un file yaml", "come aprire il file yaml", "estensione", "file", "file yaml", "formato file yaml", "estensione .yaml" , "yaml vs json" ,"Esempio di file YAML", "Esempio di file yaml docker"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Scopri il formato di file YAML e le API che possono creare e aprire un file YAML.",
  "title" :"Formato file YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Che cos'è un file YAML? ##

**Il file YAML** è costituito da un linguaggio YAML (YAML Ain't Markup Language) che è un linguaggio di serializzazione dei dati basato su Unicode; utilizzato per i file di configurazione, la messaggistica Internet, la persistenza degli oggetti, ecc. YAML utilizza l'estensione .yaml per i suoi file. La sua sintassi è indipendente da un linguaggio di programmazione specifico. Fondamentalmente, YAML è progettato per l'interazione umana e per funzionare bene con i moderni linguaggi di programmazione. Il supporto per la serializzazione di strutture dati native arbitrarie ha aumentato la leggibilità dei file YAML, ma ha reso un po' complicato il processo di analisi e generazione dei file.

## Breve storia ##

YAML è stato proposto per la prima volta nel 2001 ed è stato sviluppato da Clark Evans, Ingy döt Net e Oren Ben-Kiki. Inizialmente si diceva che YAML significasse "Ancora un altro linguaggio di markup" per indicare il suo scopo come linguaggio di markup. Successivamente è stato riproposto come "YAML Aint Markup Language" per indicare il suo scopo come orientato ai dati.


## Formato file YAML ##

Il file YAML è costituito dai seguenti tipi di dati

- **Scalari**: gli scalari sono valori come stringhe, numeri interi, booleani, ecc.
- **Sequenze**: le sequenze sono elenchi con ogni elemento che inizia con un trattino (-). Gli elenchi possono anche essere nidificati.
- **Mappatura**: la mappatura offre la possibilità di elencare chiavi con valori.

### Sintassi ###

- **Spazi bianchi**: il rientro degli spazi bianchi viene utilizzato per indicare l'annidamento e la struttura generale.

```yaml
nome: John Smith
contatto:
casa: 1012355532
ufficio: 5002586256
indirizzo:
strada: |
123 vicolo Tornado
Suite 16
città: East Centerville
stato: KS
```

- **Commenti**: i commenti vengono scritti iniziando con il simbolo "#".

```yaml
# Questo è un commento YAML
```

- **Elenchi**: il trattino (-) viene utilizzato per indicare i membri dell'elenco con ciascun membro su una riga separata. I membri dell'elenco possono anche essere racchiusi tra parentesi quadre ([...]) con i membri separati da virgole (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A, B, C]
```

- **Matrice associativa**: una matrice associativa è racchiusa tra parentesi graffe ({...}). Le chiavi e i valori sono separati da due punti(:) e ogni coppia è separata da virgola (,).

```yaml
  {name: John Smith, age: 20}
```

- **Stringhe**: la stringa può essere scritta con o senza virgolette doppie (") o virgolette singole (').

```yaml
Esempio di stringa
"Stringa campione"
'Stringa campione'
```

- **Contenuto del blocco scalare**: il contenuto scalare può essere scritto in notazione a blocchi utilizzando quanto segue:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
dati: |
YAML
(YAML non è un linguaggio di markup)
è un linguaggio di serializzazione dei dati
```

```yaml
dati: ?
YAML (YAML non è un linguaggio di markup)
è un linguaggio di serializzazione dei dati
```

- **Documenti multipli**: più documenti sono separati da tre trattini (---) in un unico flusso. I trattini indicano l'inizio del documento. I trattini vengono utilizzati anche per separare le direttive dal contenuto del documento. La fine del documento è indicata da tre punti (...).

```yaml
  ---
Documento 1
  ---
Documento 2
...
```

- **Tipo**: per specificare il tipo di valore, vengono utilizzati i doppi punti esclamativi (!!).

```yaml
a: !! galleggiante 123
b: !!str 123
```

- **Tag**: per assegnare un tag a una nota, viene utilizzata una e commerciale (&) e per fare riferimento a quel nodo, viene utilizzato un asterisco (*).

```yaml
nome: John Smith
fattura a: &id01
strada: |
123 vicolo Tornado
Suite 16
città: East Centerville
stato: KS

spedizione a: *id01
```

- **Direttive**: i documenti YAML possono essere preceduti da direttive in un flusso. Le direttive iniziano con un segno di percentuale (%) seguito dal nome e poi dai parametri separati da spazi.

```yaml
%YAML 1.2
  ---
Contenuto del documento
```
## Esempio di file YAML
Qui puoi vedere un **esempio di file yaml docker** di seguito:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Fondamentalmente, sia JSON che YAML sono sviluppati per fornire un formato di interscambio di dati leggibile dall'uomo. YAML è realizzato come un superset del formato JSON. Significa che possiamo analizzare JSON usando un parser YAML. Sebbene l'implementazione pratica di questa teoria sia poco complicata. Pertanto, alcune differenze di base tra YAML e JSON sono riportate di seguito:

|YAML| JSON|
---|---|
|Processo complesso e dispendioso in termini di tempo per l'analisi dei dati serializzati |Analizza i dati serializzati JSON in modo rapido e semplice grazie al suo design più semplice|
|Meno supporto della comunità| Supporto e popolarità della community più ampia|
|Supporta i commenti| Non supporta i commenti|
|Possibilità di utilizzare il riferimento di altri oggetti di dati| Impossibile serializzare strutture complesse con riferimenti a oggetti|
|La gerarchia è indicata utilizzando caratteri a doppio spazio. I caratteri di tabulazione non sono consentiti|Gli oggetti e gli array sono indicati tra parentesi graffe e parentesi quadre.|
|Le virgolette delle stringhe sono facoltative ma supportano le virgolette singole e doppie.|Le stringhe devono essere racchiuse tra virgolette doppie.|
|Il nodo radice può essere uno qualsiasi dei tipi di dati validi|Il nodo radice deve essere un array o un oggetto.|


## Riferimenti ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

