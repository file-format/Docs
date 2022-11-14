{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "estensione", "formato", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file PML, Palm Markup Language e le API che possono creare e aprire file PML.",
  "title" :"PML - File del linguaggio di markup Palm",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Che cos'è un file PML?

Palm Inc ha introdotto il formato di file PML che sta per Palm Markup Language File. Il suo scopo è creare documenti per eReader che è un dispositivo di lettura di eBook simile al tablet. Il file PML fornisce il layout a un file [PDB](/it/ebook/pdb/) (contenente vari file di dati) da visualizzare su un dispositivo Palm.

## Dettagli tecnici dei file PML

La struttura dei file PML è costituita da tag per la creazione di un'impostazione di eBook, inclusi paragrafi, intestazioni, rientri e riferimenti. Consente inoltre la formattazione di tag come Grassetto, Maiuscolo e Apice. Gli sviluppatori possono anche aggiungere immagini agli eBook.

### Linguaggio di markup Palm
La tabella seguente specifica i comandi PML:

|Comando|Descrizione|
---|---|
| \p | Nuova pagina |
| \x | Nuovo capitolo; provoca anche una nuova interruzione di pagina. Racchiudi il titolo del capitolo (ed eventuali codici di stile) con \x e \x |
| \Xn | Nuovo capitolo, n livelli rientrati (n compresi tra 0 e 4 inclusi) nella finestra di dialogo del capitolo; non provoca un'interruzione di pagina. Racchiudi il titolo del capitolo (ed eventuali codici di stile) con \Xn e \Xn |
| \Cn="Titolo del capitolo" | Inserisci "Titolo del capitolo" nell'elenco dei capitoli, con livello n (come \Xn). Il testo non viene visualizzato sulla pagina e non forza un'interruzione di pagina. Questo a volte può essere utile per inserire un contrassegno di capitolo all'inizio di un'introduzione al capitolo, ad esempio. |
| \c | Centrare questo blocco di testo; chiudi con \c all'inizio della riga |
| \r | Giustifica a destra il blocco di testo; chiudi con \r all'inizio della riga |
| \i | Blocco in corsivo; chiudi con \i |
| \u | Blocco di sottolineatura; chiudi con \u |
| \o | Blocco overstrike; chiudi con \o |
| \v | Testo invisibile; chiudi con \v (può essere usato per i commenti) |
| \t | Blocco di rientro. Inizia all'inizio di una riga, chiudi con \t alla fine di una riga |
| \T="50%" | Indenta la percentuale specificata della larghezza dello schermo, in questo caso 50%. Se la posizione del disegno corrente è già oltre la posizione dello schermo specificata, questo tag viene ignorato. |
| \w="50%" | Incorpora una regola orizzontale di una data larghezza percentuale dello schermo, in questo caso 50%. Questo tag provoca un'interruzione di riga prima e dopo di esso. La regola è centrata. Il segno di percentuale è obbligatorio. |
| \n | Passa al carattere "normale", specificato dall'utente |
| \s | Passa a font std; chiudi con \s per ripristinare il carattere normale |
| \b | Passa a grassetto; chiudi con \b per ripristinare il carattere normale (obsoleto; usa invece \B) |
| \l | Passa a font grande; chiudi con \l per ripristinare il carattere normale |
| \B | Contrassegna il testo in grassetto. A differenza del tag \b, \B non cambia il carattere, quindi puoi avere un testo in grassetto grande. Non è possibile combinare \b e \B nello stesso file PML. |
| \Sp | Contrassegna il testo come apice. Non deve essere mescolato con altri stili come grassetto, corsivo, ecc. Racchiudi il testo in apice con \Sp. |
| \Sb | Contrassegna il testo come pedice. Non deve essere mescolato con altri stili come grassetto, corsivo, ecc. Racchiudere il testo in pedice con \Sb. |
| \k | Rendi il testo racchiuso in maiuscolo; chiudi con \k. Tutti i caratteri racchiusi nei tag \k (compresi quelli con accenti) vengono scritti in maiuscolo e visualizzati con una dimensione in punti inferiore rispetto a un normale carattere maiuscolo. |
| \\ | Rappresenta una singola barra rovesciata |
| \aXXX | Inserisci un carattere non ASCII il cui codice Windows-1252 è decimale XXX. Per i dettagli, vedere la tabella dei caratteri PML. |
| \UXXXX | Inserisci un carattere non ASCII il cui codice Unicode è XXXX esadecimale. Per i dettagli, vedere la tabella dei caratteri PML estesa. |
| \m="nomeimmagine.png" | Inserisci l'immagine con nome. Vedere la sezione sulle immagini di seguito. |
| \q="#linkanchor"Alcuni testi\q | Fare riferimento a un'ancora di collegamento che si trova in un altro punto del documento. La stringa dopo la specifica dell'àncora e prima del finale \q viene sottolineata o mostrata in altro modo come un collegamento durante la visualizzazione del documento. |
| \Q="linkanchor" | Specificare un'ancora di collegamento nel documento. |
| \- | Inserisci un trattino morbido. Un trattino morbido viene visualizzato solo se è necessario interrompere una parola su una riga. |
| \Fn="footnote1"1\Fn | Collega "1" a una nota a piè di pagina il cui nome è footnote1, contrassegnata alla fine del documento PML. Vedi la sezione sulle note a piè di pagina e le barre laterali di seguito. |
| \Sd="barra laterale1"Barra laterale\Sd | Collega il testo della "barra laterale" a una barra laterale il cui nome è sidebar1, contrassegnata alla fine del documento PML. Vedi la sezione sulle note a piè di pagina e le barre laterali di seguito. |
| \Io | Contrassegna come voce dell'indice di riferimento. Racchiudere l'elemento dell'indice (ed eventuali codici di stile) con \I e \I.|
 


## Riferimenti

* [Lingua di markup Palm - Di MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Da MobileRead](https://en.wikipedia.org/wiki/E-reader)

