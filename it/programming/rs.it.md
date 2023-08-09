{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "file", "estensione", "formato file", "Linguaggio di programmazione Rust", "Guida alla programmazione", "Esempio RS", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - File di programmazione ruggine",
  "description":"Scopri il formato di file RS e le API che possono creare e aprire file RS.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Che cos'è un file RS?

Un file con estensione RS appartiene al linguaggio di programmazione Rust, è un linguaggio di programmazione multi-paradigma, di alto livello e di uso generale progettato per prestazioni e sicurezza, soprattutto una competizione sicura. Rust è sintatticamente simile a С++ ma può garantire la sicurezza della memoria utilizzando un controllo di prestito per convalidare i riferimenti. Il linguaggio Rust ottiene la sicurezza della memoria senza raccolta di rifiuti e il conteggio dei riferimenti è opzionale.

## Formato file RS ##

Rust è stato originariamente progettato da Graydon Hore presso Mozilla Research, con i contributi di Dave Herman, Brendan Eiсh e altri. Ha ottenuto un uso crescente nell'industria e Microsoft ha sperimentato la lingua per componenti software sicuri e critici per la sicurezza.

Rust è stato votato come il "linguaggio di programmazione più amato" nello Stack Оverflоw Developer Survey ogni anno dal 2016, anche se utilizzato solo dal 7% degli intervistati nel sondaggio del 2021. Oltre alla digitazione statica convenzionale, prima della versione 0.4, Rust supportava anche i caratteri tipografici.

Il sistema tipografico ha modellato le affermazioni prima e dopo le dichiarazioni del programma, attraverso l'uso di una specifica dichiarazione di controllo. Le discrepanze potrebbero essere scoperte a tempo pieno, piuttosto che in fase di esecuzione, come potrebbe essere il caso con le affermazioni in С o С++ code. Il concetto tipografico non era unico per Rust, poiché è stato introdotto per la prima volta nella lingua NIL. I tipi sono stati rimossi perché in pratica erano poco utilizzati, anche se la stessa funzionalità può essere ottenuta sfruttando le semantiche di movimento di Rust.

La lingua di programmazione Rust ti aiuta a scrivere un software più veloce e affidabile. Ergonomia di alto livello e controllo di basso livello sono spesso in contrasto nella progettazione del linguaggio di programmazione; La ruggine sfida il conflitto. Attraverso l'equilibrio di potenti capacità tecniche e una grande esperienza di sviluppo, Rust ti dà l'opzione di controllare i dettagli di basso livello (come l'uso della memoria) senza tutta la seccatura tradizionale contro i danni.

 

## Breve storia ##

La lingua è nata da un progetto personale iniziato nel 2006 dal dipendente di Mozilla Graydоn Hoare, il quale ha affermato che il progetto è stato probabilmente chiamato dopo la famiglia di funghi della ruggine. Mozilla ha iniziato a sponsorizzare il progetto nel 2009 e lo ha annunciato nel 2010. Rust 1.0, la prima versione stabile, è stata rilasciata il 15 maggio 2015. Dopo la versione 1.0, le versioni stabili vengono consegnate ogni sei settimane, mentre Ruily è stato sviluppato in una notte rilasci, poi testati con beta rilasci che durano sei settimane. Il 6 aprile 2021, Gооgle ha annunciato il supporto per Rust all'interno di Аndrоid Open Sоurсe Рrоjeсt аt come alternativa a С/С++.

## Specifiche tecniche ##

La ruggine è destinata ad essere una lingua per sistemi altamente contemporanei e altamente sicuri, e la programmazione in grandi dimensioni, ovvero la creazione e il mantenimento di confini che preservano l'integrità del sistema di grandi dimensioni. Ciò ha portato a un set di funzionalità con un'enfasi sulla sicurezza, il controllo della disposizione della memoria e la relazione.


Il linguaggio Rust è progettato per essere sicuro per la memoria. Non consente puntatori nulli, puntatori penzolanti o corse di dati. I valori dei dati possono essere inizializzati solo attraverso un insieme fisso di moduli, tutti i quali richiedono che i loro input siano già inizializzati. Per replicare che i puntatori sono validi o NULL, come nell'elenco collegato o nelle strutture di dati dell'albero binario, la libreria Rust соre fornisce un tipo di opzione. Rust ha aggiunto la sintassi per gestire le vite. Il codice non sicuro può sovvertire alcune di queste restrizioni usando la parola chiave non sicura.


La lingua Rust non utilizza la raccolta di rifiuti automatizzata. La memoria e le altre risorse sono gestite attraverso l'acquisizione delle risorse è un'iniziativa di inizializzazione, con un conteggio di riferimento opzionale.


Rust fornisce una gestione deterministica delle risorse, con spese generali molto basse. I favori della ruggine accumulano l'allocazione dei valori e non eseguono il pugilato implicito. C'è il concetto di riferimenti (usando il simbolo), che non coinvolge il conteggio dei riferimenti in fase di esecuzione. La sicurezza di tali puntatori è verificata a tempo ravvicinato, prevenendo i puntatori penzolanti e altre forme di comportamento indefinito.


Rust ha un sistema di proprietà in cui tutti i valori hanno un proprietario unico. I valori possono essere passati per riferimento immutabile, usando &T, per riferimento mutabile, usando & mut T, o per valore, usando T. Il compilatore Rust applica queste regole a tempo debito e controlla anche che tutti i riferimenti siano validi.


## Esempio di formato file RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Riferimento ##

* [RS - di Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))



