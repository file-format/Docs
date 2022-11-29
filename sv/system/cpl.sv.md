{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "tillägg", "fil", "format", "system", "Kontrollpanelsfil", "Windows", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Kontrollpanelsfil",
  "description":"Läs mer om CPL-filformat och API:er som kan skapa och öppna CPL-filer.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är en CPL fil? ##

En CPL-fil är en typ av "system"-fil. Det används av operativsystemet Windows. En CPL-fil är en förkortning för Control Panel File. Dessa filer är binära filer som öppnas med kontrollpanelen i ett Microsoft Windows-operativsystem och används för att representera och öppna de verktyg som finns tillgängliga i kontrollpanelen, som mus, bildskärmar, nätverk, bland annat. CPL-filerna lagras vanligtvis i systemmappen på din enhet. Dessa filer bör inte öppnas manuellt.


## CPL-filformat ##

Olika CPL-filer i ditt Windows-operativsystem är anslutna för att representera olika kontrollpanelobjekt. Alla kontrollpanelobjekt är länkade till en CPL-fil och har suffixet ".cpl" kopplat till sina objekt.

Några vanliga typer av CPL-filer med deras format är:

* Inetcpl.cpl – För Internetegenskaper på din enhet
* Appwiz.cpl – För att lägga till eller ta bort programegenskaper på din enhet
* Desk.cpl – För skärmegenskaperna
* Main.cpl – För egenskaper relaterade till mus, teckensnitt, tangentbord och skrivare.
* Netcpl.cpl – För nätverksrelaterade egenskaper
* System.cpl – För systemrelaterade egenskaper och guiden Lägg till ny maskinvara
* TimeDate.cpl – För egenskaper för datum eller tid
* Mlcfg32.cpl – För Microsoft Exchange- eller Windows Messaging-egenskaper
* Intl.cpl – Detta avser egenskaper för regionala inställningar
* Modem.cpl – För modemrelaterade egenskaper
* Themes.cpl – Lagrar skrivbordsteman och egenskaper.
* Password.cpl – För lösenordsegenskaper
* Mmsys.cpl – För multimediaegenskaper
* Wgpocpl.cpl – Avser Microsoft Mail Post Office

## Kortfattad bakgrund ##

CPL-filtypen utvecklades av Microsoft Windows och är en integrerad del av Windows-operativsystemet sedan Windows 1.0. Det används fortfarande i alla Windows-versioner, och alla egenskaper för kontrollpanelobjekt lagras med den här filtypen.

## CPL exempel ##

Ett exempel på CPL-fil kan ses nedan:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>,
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
