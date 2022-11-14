{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file CMS - File profilo servizio Connection Manager",
  "description":"Scopri il file CMS e le API che possono creare e aprire file CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Che cos'è un file CMS?

Un file CMS è un file di dati che contiene informazioni sul profilo utilizzate da Microsoft Windows Connection Manager. Consente agli utenti remoti di connettersi a una rete utilizzando queste informazioni sul profilo. Le informazioni archiviate all'interno di un file CMS includono i dati sul sistema operativo dell'utente e le autorizzazioni utilizzate per stabilire una connessione tra un utente remoto e la rete. Gli amministratori CMS utilizzano il Connection Manager Administrator Kit (CMAK) per generare file CMS.

## Formato file CMS - Ulteriori informazioni

I file CMS non si trovano comunemente sulle macchine degli utenti. Poiché vengono utilizzati specificamente per consentire agli utenti remoti di accedere a una rete, li troverai sui computer utilizzati per la connessione a una rete aziendale o a un ufficio specifico. Nella maggior parte dei casi, viene utilizzato per connettersi a una rete organizzativa come Virtual Private Network (VPN) dedicata solo a un'azienda. Essendo un amministratore di rete, imposterai l'accesso a tale rete con Connection Manager per consentirgli di accedere alla rete aziendale da una posizione remota.

### Cos'è Insdie CMS?

Un file di profilo CMS viene creato utilizzando Connection Manager e viene impacchettato con altri file di configurazione prima di essere fornito all'utente remoto. Questi file aggiuntivi possono includere un CMP e un file INF che sono impacchettati insieme in un file [EXE](/it/executable/exe/). Questo pacchetto completo viene fornito all'utente remoto per la connessione alla rete.

## Riferimenti

* [Comprensione e configurazione di Windows Connection Manager](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

