{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Valdymo skydo failas",
"Windows",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL – valdymo skydelio failas",
  "description": "Sužinokite apie CPL failo formatą ir API, kurios gali kurti ir atidaryti CPL failus.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-ltl"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra CPL failas? ##

CPL failas yra sistemos failo tipas. Jį naudoja Windows operacinė sistema. CPL failas yra Valdymo skydo failo trumpinys. Šie failai yra dvejetainiai failai, kurie atidaromi naudojant Microsoft Windows operacinės sistemos valdymo skydelį ir naudojami valdymo skydelyje esantiems įrankiams, pvz., pelė, ekranai, tinklas ir kt., vaizduoti ir atidaryti. CPL failai paprastai saugomi jūsų įrenginio sistemos aplanke. Šių failų negalima atidaryti rankiniu būdu.


## CPL failo formatas ##

Skirtingi CPL failai jūsų Windows operacinėje sistemoje yra prijungti, kad atspindėtų skirtingus valdymo skydelio elementus. Visi valdymo skydelio elementai yra susieti su CPL failu ir prie jų elementų pridedama priesaga .cpl.

Kai kurie įprasti CPL failų tipai su jų formatais yra šie:

* Inetcpl.cpl – jūsų įrenginio interneto ypatybėms

* Appwiz.cpl – Norėdami pridėti arba pašalinti programų ypatybes jūsų įrenginyje

* Desk.cpl – ekrano ypatybėms

* Main.cpl – ypatybėms, susijusioms su pele, šriftais, klaviatūra ir spausdintuvais. 

* Netcpl.cpl – su tinklu susijusioms ypatybėms

* System.cpl – su sistema susijusioms ypatybėms ir naujos aparatinės įrangos įtraukimo vedliui

* TimeDate.cpl – datos arba laiko ypatybėms

* Mlcfg32.cpl – „Microsoft Exchange“ arba „Windows Messaging“ ypatybėms

* Intl.cpl – tai susiję su regioninių nustatymų savybėmis

* Modem.cpl – su modemu susijusioms ypatybėms

* Themes.cpl – saugo darbalaukio temas ir ypatybes. 

* Password.cpl – slaptažodžio ypatybėms

* Mmsys.cpl – daugialypės terpės savybėms

* Wgpocpl.cpl – susijęs su „Microsoft Mail Post Office“.


## Trumpa istorija ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. Jis vis dar naudojamas visose Windows versijose, o visos valdymo skydelio elementų ypatybės saugomos naudojant šį failo tipą.

## CPL pavyzdys Nr.

CPL failo pavyzdį galite pamatyti žemiau:

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
