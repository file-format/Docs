{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File P7S - Messaggio e-mail firmato digitalmente",
  "description":"Scopri il formato di file P7S e le API che possono creare e aprire file P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Che cos'è un file P7S?

Un file P7S è una firma digitale che viene ricevuta con un'e-mail con firma digitale. La presenza di questo file come allegato all'e-mail verifica che l'e-mail sia stata inviata da una fonte autentica. Ciò garantisce che il mittente disponga di un certificato di firma e-mail installato sul proprio computer. Quando una tale e-mail firmata viene inviata dal computer dell'utente, viene allegato il file P7S che contiene il nome del mittente. I client di posta elettronica che supportano le e-mail firmate possono vedere le informazioni del mittente.

## Formato file P7S - Ulteriori informazioni

I file P7S S/MIME (Secure/Multipurpose Internet Mail Extensions) contengono le informazioni in formato testo normale leggibile dall'uomo. I client di posta elettronica come Microsoft Outlook, Apple Mail e Mozilla Thunderbird supportano la lettura delle informazioni con firma digitale da un'e-mail S/MIME. La firma di un'e-mail verifica l'identità del mittente e indica al destinatario che il messaggio è autentico. Quando le e-mail vengono scaricate dai client di posta (come [EML](/it/email/eml/) o [MSG](/it/email/msg/)), questi file P7S vengono trovati allegati a queste e-mail.

Un file P7S contiene le seguenti informazioni:

* Fonte di origine dell'e-mail
* Data e ora di invio,
* Se è stato modificato durante la trasmissione

Queste informazioni vengono incorporate utilizzando la tecnologia Public-Key Cryptography Standard #7 (PKCS7) per allegare digitalmente le firme crittografate all'e-mail.

## Riferimenti ##

* [Strumento firma Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

