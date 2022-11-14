{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "file", "estensione", "formato file", "implementazione ICI", "Guida alla programmazione", "esempio ici", "linguaggio di programmazione ICI", "moduli di ICI", "modello dati di ICI ", "documentazione di ICI", "linguaggio ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - File del linguaggio di programmazione",
  "description":"Scopri il formato di file ICI e le API che possono creare e aprire file ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Che cos'è un file ICI?

Un linguaggio di programmazione generico che viene interpretato e contiene diverse funzionalità come la digitazione dinamica insieme ai tipi di dati flessibili è noto come linguaggio di programmazione ICI (non acronimo). È considerato simile al linguaggio [Perl](/it/programmazione/pl/). Questo linguaggio ICI comprende costrutti di controllo del flusso e contiene anche alcuni operatori del linguaggio C. Non è un linguaggio orientato agli oggetti, ma alcune delle caratteristiche dell'OOP possono essere raggiunte da un metodo di ereditarietà specifico noto come sovrastrutture. Simile a [C](/it/programmazione/c), questo linguaggio di programmazione ICI ha la stessa interfaccia di sistema e una libreria standard per le funzioni integrate.


## Breve storia ##

Alla fine degli anni '80, è stato sviluppato da Tim Long come linguaggio di programmazione interpretato per uso generale. La maggior parte delle funzionalità di questo linguaggio sono simili al C e può anche ottenere alcune funzionalità applicando alcuni metodi speciali. Questa lingua è di dominio pubblico ed è disponibile come lingua rivendibile e nessuno è tenuto a menzionare da dove ha ottenuto il codice sorgente. La documentazione di ICI è protetta da copyright di Canon Information System Research Australia.

## Specifiche tecniche ##

Esistono due diversi tipi di dati utilizzati in questa lingua. Questi due sono tipi di dati Primitive e Aggregate. Entrambi includono espressioni diverse in base alla loro composizione predefinita nella lingua. Diversi moduli come nidificati e subroutine sono supportati da questo linguaggio. Poiché alcune delle sue proprietà sono simili a Perl, ha una stretta integrazione con le espressioni regolari.

Gli insiemi sono limitati per essere eterogenei e nidificati. Questi set forniscono supporto per operazioni di set di uso comune come Union e Intersection, ecc. Viene utilizzato principalmente come linguaggio per il bene dell'implementazione di base per applicazioni di proprietà di organizzazioni multinazionali.

Quasi tutti i tipi di programmi possono essere scritti in questo linguaggio e la maggior parte dei programmi specifici che coinvolgono strutture dati complesse sono scritti nel linguaggio di programmazione ICI. Le domande possono comportare l'implementazione dell'ICI in un modo che dovrebbero essere scritte in essa. Porzioni funzionali dell'applicazione possono essere implementate dai moduli di ICI. Il linguaggio di ICI assomiglia in qualche modo al linguaggio C, ma il modello di dati di ICI è di livello piuttosto superiore e diverso con tipi come dizionari (struct), set, array dinamici, espressioni regolari e stringhe (reali).


## Esempio di formato file ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Riferimento ##

* [Linguaggio di programmazione ICI](http://atrn.org/ici/doc/ici.html)



