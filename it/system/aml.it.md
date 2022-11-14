{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AML - File linguaggio macchina ACPI",
  "description":"Scopri il formato di file AML ACPI e le API che possono creare e aprire file AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Che cos'è un file AML?

Un file AML è un file di sistema creato con il linguaggio ACPI (Advanced Configuration and Power Interface) utilizzato per configurare le proprietà hardware. Contiene codice byte indipendente dalla macchina che viene utilizzato per configurare l'hardware anche per operazioni semplici come lo spegnimento di un computer. I file AML possono contenere istruzioni a seconda dello scopo per cui devono essere installati sulla macchina. L'implementazione degli standard ACPI consente di migliorare la funzionalità di gestione dell'alimentazione e un'interfaccia robusta per la configurazione dei dispositivi della scheda madre come le schede madri P55.

## Formato file AML ACPI

I file AML vengono salvati come file binari su disco con contenuti scritti in byte code. Le specifiche del formato file dello standard ACPI sono disponibili su [uefi](https://uefi.org/node/735). Il linguaggio è stato progettato per offrire stabilità e compatibilità con le versioni precedenti, richiedendo meno riscritture o ricompilazioni dello stack dell'applicazione.

## Specifiche del formato file AML

Un file AML comprende tabelle DSDT e SSDT. Il codice byte AML viene letto e analizzato dall'inizio di ciascuna di queste tabelle. Questo fornisce informazioni sulle definizioni di dispositivi e oggetti nello spazio dei nomi ACPI. Utilizzando queste informazioni, l'interprete AML può generare un elenco di tutti i dispositivi disponibili nel sistema e le relative proprietà e funzioni supportate.

### Esempio di codice ASL per un DSDT

Un esempio di codice ASL per un DSDT è il seguente.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Riferimenti

* [AML ACPI](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

