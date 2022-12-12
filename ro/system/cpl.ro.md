{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extensie", "fișier", "format", "sistem", "Fișier panou de control", "Windows", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL – Fișierul panoului de control",
  "description":"Aflați despre formatul de fișier CPL și despre API-urile care pot crea și deschide fișiere CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier CPL? ##

Un fișier CPL este un tip de fișier „sistem”. Este folosit de sistemul de operare Windows. Un fișier CPL este prescurtarea pentru Control Panel File. Aceste fișiere sunt fișiere binare care se deschid cu panoul de control într-un sistem de operare Microsoft Windows și sunt folosite pentru a reprezenta și deschide instrumentele disponibile în panoul de control, cum ar fi mouse-ul, afișajele, rețeaua, printre altele. Fișierele CPL sunt de obicei stocate în folderul de sistem de pe dispozitiv. Aceste fișiere nu trebuie deschise manual.


## Format fișier CPL ##

Diferite fișiere CPL din sistemul dvs. de operare Windows sunt conectate pentru a reprezenta diferite elemente din panoul de control. Toate elementele panoului de control sunt legate la un fișier CPL și au sufixul „.cpl” atașat la articolele lor.

Unele tipuri comune de fișiere CPL cu formatele lor sunt:

* Inetcpl.cpl – Pentru proprietățile Internet de pe dispozitivul dvs
* Appwiz.cpl – Pentru a adăuga sau elimina proprietăți de programe de pe dispozitiv
* Desk.cpl – Pentru proprietățile de afișare
* Main.cpl – Pentru proprietăți legate de mouse, fonturi, tastatură și imprimante.
* Netcpl.cpl – Pentru proprietățile legate de rețea
* System.cpl – Pentru proprietățile legate de sistem și pentru expertul Add New Hardware
* TimeDate.cpl – Pentru proprietățile Date sau Time
* Mlcfg32.cpl – Pentru proprietățile Microsoft Exchange sau Windows Messaging
* Intl.cpl – Se referă la proprietățile Setărilor regionale
* Modem.cpl – Pentru proprietăți legate de modem
* Themes.cpl – Stochează teme și proprietăți desktop.
* Password.cpl – Pentru proprietățile parolei
* Mmsys.cpl – Pentru proprietăți multimedia
* Wgpocpl.cpl – Se referă la oficiul poștal Microsoft Mail

## Scurt istoric ##

Tipul de fișier CPL a fost dezvoltat de Microsoft Windows și este o parte integrantă a sistemului de operare Windows începând cu Windows 1.0. Este încă folosit în toate versiunile de Windows și toate proprietățile elementelor din panoul de control sunt stocate folosind acest tip de fișier.

## Exemplu CPL ##

Un exemplu de fișier CPL poate fi văzut mai jos:

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
