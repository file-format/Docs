{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Script di shell: come eseguirlo su Ubuntu e Linux",
  "description":"Scopri cos'è Shell Script e come eseguirlo su Ubuntu e Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-it",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Cos'è lo script Shell?

Lo scripting di shell prevede la scrittura di una serie di comandi in un file di testo semplice, spesso definito **script di shell**. Questi script vengono eseguiti da una shell, che è un interprete della riga di comando. Le conchiglie più comuni includono

1. Bash (Bourne Again SHell)
2. Zsh (guscio Z)
3. Pescare.

Gli script di shell possono variare da semplici righe a programmi complessi e vengono utilizzati per eseguire un'ampia varietà di attività, come la manipolazione di file, l'amministrazione di sistema e l'automazione di attività ripetitive.

## Vantaggi dello scripting di shell:

1.  **Automazione:** gli script di shell consentono agli utenti di automatizzare le attività ripetitive, risparmiando tempo e riducendo la possibilità di errore umano.
    
2.  **Personalizzazione:** gli utenti possono creare script su misura per le loro esigenze specifiche, fornendo un elevato grado di personalizzazione.
    
3.  **Elaborazione batch:** gli script di shell sono eccellenti per gestire attività di elaborazione batch, in cui è necessario eseguire più comandi in sequenza.
    
4.  **Amministrazione del sistema:** gli script della shell vengono comunemente utilizzati per attività di amministrazione del sistema, come backup, rotazione dei registri e installazione di software.

## Scrivere un semplice script di shell:

Creiamo uno script di shell di base che stampi un messaggio di saluto. Apri un editor di testo e crea un file chiamato greeting.sh. Aggiungi le seguenti righe:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Salvare il file e renderlo eseguibile eseguendo il seguente comando nel terminale:

```
chmod +x greeting.sh
```

Ora puoi eseguire lo script:

```
./greeting.sh
```

L'output dovrebbe essere:

```
Hello, welcome to the world of shell scripting!
```

## Esecuzione di script di shell su Ubuntu e Linux:

Ora discuteremo di **come eseguire un file .sh in Ubuntu e Linux**.

1.  **Rendi eseguibile lo script:** prima di eseguire uno script di shell, assicurati che sia eseguibile. Utilizza il comando `chmod` come mostrato in precedenza.
    
2.  **Vai alla directory degli script:** apri un terminale e utilizza il comando `cd` per navigare nella directory contenente lo script della shell.
    
3.  **Esegui lo script:** Esegui lo script digitando `./scriptname.sh` nel terminale, sostituendo scriptname con il nome effettivo dello script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Utilizzo del comando Bash:** se il tuo script inizia con `#!/bin/bash` (noto come **shebang**), puoi anche eseguirlo utilizzando il comando `bash`.

```
bash greeting.sh
```

## Cosa significa $@ nello script Shell?

Nello script di shell, `$@` rappresenta tutti gli argomenti della riga di comando passati allo script. Viene spesso utilizzato per fare riferimento a un elenco di argomenti come entità separate. Se utilizzato tra virgolette doppie, come `$@`, conserva i singoli argomenti, tenendo conto degli spazi e dei caratteri speciali.

Ecco una breve spiegazione:

- `$@`: rappresenta tutti i parametri posizionali (argomenti) passati allo script o alla funzione. Ogni argomento viene trattato come una parola separata.
    
- `$@`: Se racchiuso tra virgolette doppie, preserva la separazione degli argomenti, consentendo spazi o caratteri speciali all'interno dei singoli argomenti.
    

Ecco un semplice esempio per illustrare:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Quando esegui questo script con argomenti, ad esempio:

```
bash example.sh arg1 "argument 2" arg3
```

Verrebbe prodotto:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Come puoi vedere, `$@` rappresenta tutti gli argomenti e `$@` preserva i singoli argomenti, anche se contengono spazi.

