{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File SHSH2 - Formato file BLOB SHSH per iOS",
  "description":"Scopri cos'è un file SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Cos'è un file SHSH2?

Un file SHSH2, noto anche come BLOB SHSH o ECID SHSH, è una firma digitale utilizzata da Apple per autenticare e verificare gli aggiornamenti del firmware per dispositivi iOS come iPhone, iPad e iPod. Contiene un identificatore univoco per il dispositivo noto come ECID (Exclusive Chip ID). Contiene inoltre informazioni sulla versione del firmware installata sul dispositivo.

## Formato file SHSH2: ulteriori informazioni

I file SHSH2 vengono salvati su disco in formato file binario e i dettagli della struttura interna del file di questo formato file non sono disponibili pubblicamente.

Quando una nuova versione di iOS viene installata su un dispositivo Apple come iPhone, iPad o Mac, viene generato un file SHSH2. Questo file SHSH2 viene inviato ai server Apple che leggono e verificano questo file di firma digitale. Sulla base di queste informazioni, il server consente o impedisce l'installazione.

Lo stesso accade quando viene richiesto un aggiornamento. Quando un utente richiede un aggiornamento o un ripristino del proprio dispositivo tramite iTunes o un altro software, i server Apple controlleranno che il file SHSH2 corrisponda all'ECID del dispositivo e alla versione del firmware prima di consentire l'aggiornamento.

## Riferimenti

* [SHSH Blob - Da Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Risparmio TSS](https://tsssaver.1conan.com/v2/)

