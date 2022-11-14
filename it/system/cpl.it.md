{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "estensione", "file", "formato", "sistema", "File del pannello di controllo", "Windows", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - File del pannello di controllo",
  "description":"Scopri il formato di file CPL e le API che possono creare e aprire file CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file CPL? ##

Un file CPL è un tipo di file di "sistema". È utilizzato dal sistema operativo Windows. Un file CPL è l'abbreviazione di Control Panel File. Questi file sono file binari che si aprono con il pannello di controllo in un sistema operativo Microsoft Windows e vengono utilizzati per rappresentare e aprire gli strumenti disponibili nel pannello di controllo, come mouse, display, rete, tra gli altri. I file CPL sono in genere archiviati nella cartella di sistema del dispositivo. Questi file non devono essere aperti manualmente.


## Formato file CPL ##

Diversi file CPL nel tuo sistema operativo Windows sono collegati per rappresentare diversi elementi del pannello di controllo. Tutti gli elementi del pannello di controllo sono collegati a un file CPL e hanno il suffisso ".cpl" allegato ai loro elementi.

Alcuni tipi comuni di file CPL con i relativi formati sono:

* Inetcpl.cpl – Per le proprietà Internet sul tuo dispositivo
* Appwiz.cpl – Per aggiungere o rimuovere le proprietà dei programmi sul tuo dispositivo
* Desk.cpl – Per le proprietà di visualizzazione
* Main.cpl: per le proprietà relative a mouse, caratteri, tastiera e stampanti.
* Netcpl.cpl – Per le proprietà relative alla rete
* System.cpl: per le proprietà relative al sistema e per la procedura guidata per l'aggiunta di nuovo hardware
* TimeDate.cpl – Per le proprietà Data o Ora
* Mlcfg32.cpl – Per le proprietà di Microsoft Exchange o Windows Messaging
* Intl.cpl: riguarda le proprietà delle impostazioni internazionali
* Modem.cpl – Per le proprietà relative al modem
* Themes.cpl – Memorizza temi e proprietà del desktop.
* Password.cpl – Per le proprietà della password
* Mmsys.cpl – Per le proprietà multimediali
* Wgpocpl.cpl – Riguarda l'ufficio postale di Microsoft Mail

## Breve storia ##

Il tipo di file CPL è stato sviluppato da Microsoft Windows ed è parte integrante del sistema operativo Windows da Windows 1.0. È ancora utilizzato in tutte le versioni di Windows e tutte le proprietà degli elementi del pannello di controllo vengono archiviate utilizzando questo tipo di file.

## Esempio CPL ##

Di seguito è possibile visualizzare un file CPL di esempio:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
