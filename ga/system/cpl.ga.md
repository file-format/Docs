{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"síneadh",
"comhad",
"formáid",
"córas",
"Comhad Painéal Rialúcháin",
"Windows",
"cláir",
"ríomhaire",
"iarratas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL - Comhad Painéal Rialúcháin",
  "description": "Foghlaim faoi fhormáid comhaid CPL agus APIs ar féidir leo comhaid CPL a chruthú agus a oscailt.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-gal"
}
},
  "lastmod": "2021-06-29"
}

## Cad is comhad CPL ann? ##

Is cineál comhaid córais é comhad CPL. Úsáideann córas oibriúcháin Windows é. Tá comhad CPL gearr do Chomhad Painéil Rialaithe. Is comhaid dhénártha iad na comhaid seo a osclaíonn leis an bpainéal rialaithe i gcóras oibriúcháin Microsoft Windows agus úsáidtear iad chun na huirlisí atá ar fáil sa phainéal rialaithe a léiriú agus a oscailt, mar shampla Luch, Taispeántais, Líonrú, i measc daoine eile. Go hiondúil déantar na comhaid CPL a stóráil i bhfillteán an chórais ar do ghléas. Níor cheart na comhaid seo a oscailt de láimh.


## Formáid Chomhaid CPL ##

Tá comhaid CPL éagsúla i do chóras oibriúcháin Windows ceangailte chun míreanna painéil rialaithe éagsúla a léiriú. Tá gach mír den phainéal rialaithe nasctha le comhad CPL agus tá an iarmhír .cpl” ceangailte dá míreanna.

Seo a leanas roinnt cineálacha coitianta de chomhaid CPL lena gcuid formáidí:

* Inetcpl.cpl - Le haghaidh airíonna Idirlín ar do ghléas

* Appwiz.cpl - Chun airíonna Cláir a Chur leis nó a Bhaint ar do ghléas

* Desk.cpl – Maidir leis na hairíonna Taispeáin

* Main.cpl – I gcás maoine a bhaineann le Luch, Clónna, Méarchlár, agus Printéirí. 

* Netcpl.cpl – Le haghaidh maoine a bhaineann le Líonra

* System.cpl – Le haghaidh airíonna a bhaineann leis an gCóras agus chun draoi Crua-earraí Nua a Chur Leis

* TimeDate.cpl – Do Dáta nó Am airíonna

* Mlcfg32.cpl – Le haghaidh airíonna Microsoft Exchange nó Windows Teachtaireachtaí

* Intl.cpl – Baineann sé seo le réadmhaoin i Socruithe Réigiúnacha

* Modem.cpl - Le haghaidh maoine a bhaineann le Móideim

* Themes.cpl - Stores Deisce Téamaí agus airíonna. 

* Password.cpl - Le haghaidh airíonna Pasfhocal

* Mmsys.cpl – Le haghaidh airíonna Ilmheáin

* Wgpocpl.cpl – Baineann sé le Microsoft Mail Oifig an Phoist


## Stair Ghearr ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. Úsáidtear é fós i ngach leagan de Windows, agus stóráiltear airíonna uile na míre painéil rialaithe ag baint úsáide as an gcineál comhaid seo.

## Sampla CPL ##

Is féidir comhad CPL samplach a fheiceáil thíos:

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
