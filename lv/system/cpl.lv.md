{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Vadības paneļa fails",
"Windows",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL — vadības paneļa fails",
  "description": "Uzziniet par CPL faila formātu un API, kas var izveidot un atvērt CPL failus.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-lvl"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir CPL fails? ##

CPL fails ir sistēmas faila veids. To izmanto operētājsistēma Windows. CPL fails ir saīsinājums no vadības paneļa faila. Šie faili ir binārie faili, kas tiek atvērti ar vadības paneli Microsoft Windows operētājsistēmā un tiek izmantoti, lai attēlotu un atvērtu vadības panelī pieejamos rīkus, piemēram, peli, displejus, tīklus un citus. CPL faili parasti tiek saglabāti jūsu ierīces sistēmas mapē. Šos failus nevajadzētu atvērt manuāli.


## CPL faila formāts ##

Dažādi CPL faili jūsu Windows operētājsistēmā ir savienoti, lai attēlotu dažādus vadības paneļa vienumus. Visi vadības paneļa vienumi ir saistīti ar CPL failu, un tiem ir pievienots sufikss .cpl”.

Daži izplatīti CPL failu veidi un to formāti ir:

* Inetcpl.cpl — interneta rekvizītiem jūsu ierīcē

* Appwiz.cpl — lai pievienotu vai noņemtu programmas rekvizītus savā ierīcē

* Desk.cpl — displeja rekvizītiem

* Main.cpl — rekvizīti, kas saistīti ar peli, fontiem, tastatūru un printeriem. 

* Netcpl.cpl — ar tīklu saistītiem īpašumiem

* System.cpl — ar sistēmu saistītiem rekvizītiem un jaunas aparatūras pievienošanas vednim

* TimeDate.cpl — datuma vai laika rekvizītiem

* Mlcfg32.cpl — Microsoft Exchange vai Windows Messaging rekvizītiem

* Intl.cpl — tas attiecas uz reģionālo iestatījumu rekvizītiem

* Modem.cpl — ar modemu saistītiem rekvizītiem

* Themes.cpl — tiek glabāti darbvirsmas motīvi un rekvizīti. 

* Password.cpl — paroles īpašībām

* Mmsys.cpl — multivides rekvizītiem

* Wgpocpl.cpl — attiecas uz Microsoft Mail Post Office


## Īsa vēsture ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. Tas joprojām tiek izmantots visās Windows versijās, un visi vadības paneļa vienumu rekvizīti tiek saglabāti, izmantojot šo faila tipu.

## CPL piemērs ##

CPL faila paraugu var redzēt zemāk:

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
