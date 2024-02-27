{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"udvidelse",
"fil",
"format",
"system",
"Kontrolpanel fil",
"Windows",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL - Kontrolpanelfil",
  "description": "Lær om CPL-filformat og API'er, der kan oprette og åbne CPL-filer.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-dal"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er en CPL fil? ##

En CPL fil er en type system fil. Det bruges af Windows-operativsystemet. En CPL-fil er en forkortelse for Control Panel File. Disse filer er binære filer, der åbnes med kontrolpanelet i et Microsoft Windows-operativsystem og bruges til at repræsentere og åbne de tilgængelige værktøjer i kontrolpanelet, såsom mus, skærme, netværk, blandt andre. CPL-filerne gemmes typisk i systemmappen på din enhed. Disse filer bør ikke åbnes manuelt.


## CPL-filformat ##

Forskellige CPL-filer i dit Windows-operativsystem er forbundet for at repræsentere forskellige kontrolpanelelementer. Alle kontrolpanelelementer er knyttet til en CPL-fil og har suffikset .cpl knyttet til deres elementer.

Nogle almindelige typer CPL-filer med deres formater er:

* Inetcpl.cpl – Til internetejendomme på din enhed

* Appwiz.cpl – For at tilføje eller fjerne programmer egenskaber på din enhed

* Desk.cpl – Til skærmegenskaberne

* Main.cpl – For egenskaber relateret til mus, skrifttyper, tastatur og printere. 

* Netcpl.cpl – Til netværksrelaterede egenskaber

* System.cpl – Til systemrelaterede egenskaber og guiden Tilføj ny hardware

* TimeDate.cpl – For egenskaber for dato eller klokkeslæt

* Mlcfg32.cpl – Til Microsoft Exchange eller Windows Messaging-egenskaber

* Intl.cpl – Dette vedrører egenskaber for regionale indstillinger

* Modem.cpl – Til modemrelaterede egenskaber

* Themes.cpl – Gemmer skrivebordstemaer og egenskaber. 

* Password.cpl – Til adgangskodeegenskaber

* Mmsys.cpl – Til multimedieegenskaber

* Wgpocpl.cpl – Vedrører Microsoft Mail Post Office


## Kort historie ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. Det bruges stadig i alle Windows-versioner, og alle kontrolpanelets egenskaber gemmes ved hjælp af denne filtype.

## CPL eksempel ##

Et eksempel på CPL-fil kan ses nedenfor:

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
