{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "estensione", "file", "formato", "sistema", "Cold Fusion Markup Language", "lingua", "Pagine web CFM", "Motore CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Markup sulla fusione fredda",
  "description":"Scopri il formato di file CFM e le API che possono creare e aprire file CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Che cos'è un file CFM? ##

Le pagine Web e i file utilizzati in **Cold Fusion Markup Language** contengono estensioni di CFM e sono denominati pagine Web CFM. Questo linguaggio di scripting per lo sviluppo Web viene eseguito su Google App Engine, .NET Framework e JVM. Può contenere un linguaggio di programmazione o un codice del linguaggio. Quando l'utente accede a una qualsiasi delle sue pagine, il server web di ColdFusion lo esegue. CFScript (che è simile a JavaScript) o tag possono essere utilizzati per scrivere CFML. CFML può essere utilizzato per generare altri linguaggi oltre a [HTML](/it/web/html/) come [CSS](/it/web/css/), [JavaScript](/it/web/js/), [XML](/it/web/xml/), e altro ancora.

L'uso di questo linguaggio e dei tag che supporta è principalmente nello sviluppo di applicazioni web dinamiche. I file possono essere eseguiti direttamente nel browser online se si verifica un errore durante l'utilizzo offline della piattaforma di sviluppo dell'applicazione.
 

CFML funziona in modo tale da fornire estensioni di file del server specifiche (.cfc, .cfm) per l'elaborazione al motore CFML. Se i motori sono basati su Java, si ottiene utilizzando i servlet Java. Il motore di CFML elabora solo funzioni e tag e restituisce funzioni e testo al di fuori dei tag CFML al server web senza alcuna modifica.


## Breve storia ##

Nel 1995 è stato creato per la prima volta da una società chiamata Allaire. Nel 2005 Adobe lo ha acquisito e fornisce ancora oggi servizi per lo sviluppo di ColdFusion. Con il passare degli anni, è stato sviluppato e aggiornato da molte persone e aziende. Nel 2012 è stata lanciata una fondazione denominata OpenCFML. Successivamente, nel 2015, l'ex Railo ha fornito i suoi servizi per migliorare le prestazioni di CFM e ha ridotto le risorse per una migliore funzionalità. L'aggiornamento più recente è stato lanciato nel 2020 e si annuncia che continuerà fino al 2028.

## Formato file CFM ##

Il codice dei file CFM e delle pagine web comprende principalmente i tag come HTML ma con una leggera differenza. Questi file sono responsabili dell'esecuzione di varie operazioni che gli script ColdFusion consentono di eseguire.
* È possibile accedere a questi file ed eseguirli direttamente su Windows e macOS utilizzando il browser di qualsiasi sistema operativo.
* Adobe ColdFusion fornisce la piattaforma per lo sviluppo di pagine web e applicazioni dinamiche su PC.
* Qualsiasi editor di testo come Blocco note o qualsiasi altro editor di testo in un sistema operativo può essere utilizzato per aprire questi file poiché questi file sono basati su testo.
* Quando un file CFM viene aperto in un editor di testo, viene visualizzato un codice composto da tag e script che non si comprenderebbero a meno che non si sia uno sviluppatore web.

## Esempio di utilizzo CFM ##

Di seguito viene mostrato un semplice file CFM di esempio di utilizzo.

### Documento CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Riferimenti ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

