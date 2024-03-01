{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Ohjauspaneelin tiedosto",
"Windows",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL - Ohjauspaneelin tiedosto",
  "description": "Opi CPL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CPL-tiedostoja.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-fil"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on CPL-tiedosto? ##

CPL-tiedosto on järjestelmä-tiedoston tyyppi. Sitä käyttää Windows-käyttöjärjestelmä. CPL-tiedosto on lyhenne sanoista Ohjauspaneelitiedosto. Nämä tiedostot ovat binääritiedostoja, jotka avautuvat ohjauspaneelin kanssa Microsoft Windows -käyttöjärjestelmässä ja joita käytetään edustamaan ja avaamaan ohjauspaneelissa käytettävissä olevia työkaluja, kuten hiiri, näytöt, verkko jne. CPL-tiedostot tallennetaan yleensä laitteesi järjestelmäkansioon. Näitä tiedostoja ei saa avata manuaalisesti.


## CPL-tiedostomuoto ##

Windows-käyttöjärjestelmän eri CPL-tiedostot on yhdistetty edustamaan eri ohjauspaneelin kohteita. Kaikki ohjauspaneelin kohteet on linkitetty CPL-tiedostoon ja niihin on liitetty pääte .cpl.

Joitakin yleisiä CPL-tiedostotyyppejä muodoineen ovat:

* Inetcpl.cpl – Laitteesi Internet-ominaisuuksille

* Appwiz.cpl – Laitteen ohjelmien lisääminen tai poistaminen

* Desk.cpl – Näytön ominaisuudet

* Main.cpl – Hiireen, Fonteihin, Näppäimistöön ja Tulostimiin liittyville ominaisuuksille. 

* Netcpl.cpl – Verkkoon liittyville ominaisuuksille

* System.cpl – Järjestelmään liittyvät ominaisuudet ja ohjattu uuden laitteiston asennus

* TimeDate.cpl – Päivämäärä- tai aika-ominaisuuksille

* Mlcfg32.cpl – Microsoft Exchange- tai Windows Messaging -ominaisuuksille

* Intl.cpl – Tämä koskee alueellisten asetusten ominaisuuksia

* Modem.cpl – Modeemiin liittyville ominaisuuksille

* Themes.cpl – Tallentaa työpöydän teemoja ja ominaisuuksia. 

* Password.cpl – Salasanan ominaisuudet

* Mmsys.cpl – Multimediaominaisuuksille

* Wgpocpl.cpl – Koskee Microsoft Mail Post Officea


## Lyhyt historia ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. Sitä käytetään edelleen kaikissa Windows-versioissa, ja kaikki ohjauspaneelin kohteiden ominaisuudet tallennetaan tällä tiedostotyypillä.

## CPL-esimerkki ##

Esimerkki CPL-tiedostosta näkyy alla:

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
