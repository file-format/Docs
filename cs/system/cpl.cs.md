{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "rozšíření", "soubor", "formát", "systém", "Soubor ovládacího panelu", "Windows", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - soubor ovládacího panelu",
  "description":"Další informace o formátu souboru CPL a rozhraních API, která mohou vytvářet a otevírat soubory CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor CPL? ##

Soubor CPL je typ "systémového" souboru. Používá jej operační systém Windows. Soubor CPL je zkratka pro soubor ovládacího panelu. Tyto soubory jsou binární soubory, které se otevírají pomocí ovládacího panelu v operačním systému Microsoft Windows a používají se k reprezentaci a otevírání nástrojů dostupných v ovládacím panelu, jako jsou mimo jiné myš, displeje, sítě. Soubory CPL jsou obvykle uloženy v systémové složce na vašem zařízení. Tyto soubory by se neměly otevírat ručně.


## Formát souboru CPL ##

Různé soubory CPL ve vašem operačním systému Windows jsou připojeny tak, aby reprezentovaly různé položky ovládacího panelu. Všechny položky ovládacího panelu jsou propojeny se souborem CPL a mají ke svým položkám připojenou příponu „.cpl“.

Některé běžné typy souborů CPL s jejich formáty jsou:

* Inetcpl.cpl – Pro internetové vlastnosti ve vašem zařízení
* Appwiz.cpl – Přidání nebo odebrání vlastností programů na vašem zařízení
* Desk.cpl – Pro vlastnosti zobrazení
* Main.cpl – Pro vlastnosti týkající se myši, písem, klávesnice a tiskáren.
* Netcpl.cpl – pro vlastnosti související se sítí
* System.cpl – pro vlastnosti související se systémem a průvodce přidáním nového hardwaru
* TimeDate.cpl – pro vlastnosti Date nebo Time
* Mlcfg32.cpl – Pro vlastnosti Microsoft Exchange nebo Windows Messaging
* Intl.cpl – Týká se vlastností Místní nastavení
* Modem.cpl – Pro vlastnosti související s modemem
* Themes.cpl – Ukládá motivy a vlastnosti plochy.
* Password.cpl – pro vlastnosti hesla
* Mmsys.cpl – pro multimediální vlastnosti
* Wgpocpl.cpl – Týká se Microsoft Mail Post Office

## Stručná historie ##

Typ souboru CPL byl vyvinut společností Microsoft Windows a je nedílnou součástí operačního systému Windows od Windows 1.0. Stále se používá ve všech verzích Windows a všechny vlastnosti položek ovládacího panelu jsou uloženy pomocí tohoto typu souboru.

## Příklad CPL ##

Ukázkový soubor CPL si můžete prohlédnout níže:

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
