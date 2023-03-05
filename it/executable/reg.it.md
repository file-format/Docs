{
  "date" : "2021-08-02",
  "keywords" :[ "file reg", "formato file reg", "che cos'è un file reg", "file", "esempio reg", "estensione file reg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file REG e le API che possono creare e aprire file REG.",
  "title" :"REG - File di registro di Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Che cos'è un file REG?
Un file REG è semplicemente un file di testo con estensione .reg. Questi file vengono solitamente creati esportando le chiavi tipiche dal Registro di sistema. Questi file possono essere utilizzati anche come backup del registro (in particolare questo passaggio è importante prima di apportare modifiche!). Puoi vedere che alcuni li hanno resi disponibili come file scaricabili sugli stessi siti che ti mostrano come eseguire un hack del Registro di sistema. Un file REG è utile per apportare modifiche manuali al Registro ed esportare tali modifiche. Pulisci un po' il file e poi condividilo con gli altri.

## Formato file REG
Il formato di file REG è stato progettato per l'esportazione e l'importazione di parti del registro di Windows utilizzando una sintassi basata su INI. Il registro di Windows è un database relazionale o gerarchico che mantiene le impostazioni di basso livello per il sistema operativo Microsoft Windows e altre applicazioni che utilizzano il registro di Windows. In alternativa, possiamo dire, il registro o registro di Windows è costituito da informazioni, opzioni, impostazioni e altri valori per programmi e hardware installati su tutte le versioni dei sistemi operativi Microsoft Windows.
### Sintassi del file REG
Ecco alcuni elementi chiave come parte della sintassi di un file REG:
- **RegistryEditorVersion**: ad es. "Editor del registro di Windows versione 5.00" per Windows 2000, Windows XP e Windows Server 2003.
- **Riga vuota**: identifica l'inizio di un nuovo percorso di registro.
- **RegistryPathx**: il percorso della sottochiave che contiene il primo valore che stai importando.
- **DataItemNamex**: il nome dell'elemento dati che si desidera importare.
- **DataTypex**: il tipo di dati per il valore del registro.

Le chiavi vengono archiviate in file .reg utilizzando la seguente sintassi:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
È possibile modificare il valore predefinito di una chiave utilizzando "@" anziché "Nome valore":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Esempio
Ecco un esempio di file REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Riferimenti

* [Registro di Windows- di Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Come aggiungere, modificare o eliminare sottochiavi e valori del registro utilizzando un file .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
