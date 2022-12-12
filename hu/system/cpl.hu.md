{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extension", "file", "format", "system", "Control Panel File", "Windows", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Vezérlőpult fájl",
  "description":"További információ a CPL fájlformátumról és az API-król, amelyek CPL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a CPL fájl? ##

A CPL-fájl egyfajta "rendszer"-fájl. A Windows operációs rendszer használja. A CPL fájl a Vezérlőpult fájl rövidítése. Ezek a fájlok bináris fájlok, amelyek a Microsoft Windows operációs rendszer vezérlőpultjával nyílnak meg, és a vezérlőpulton elérhető eszközök megjelenítésére és megnyitására szolgálnak, mint például az egér, a kijelzők, a hálózatkezelés stb. A CPL-fájlok általában az eszköz rendszermappájában tárolódnak. Ezeket a fájlokat nem szabad kézzel megnyitni.


## CPL fájlformátum ##

A Windows operációs rendszerben különböző CPL-fájlok vannak csatlakoztatva, hogy a vezérlőpult különböző elemeit képviseljék. A vezérlőpult minden eleme egy CPL-fájlhoz van kapcsolva, és az elemekhez a „.cpl” utótag tartozik.

A CPL-fájlok néhány gyakori típusa a formátumukkal együtt:

* Inetcpl.cpl – Az eszköz internetes tulajdonságaihoz
* Appwiz.cpl – Programok hozzáadása vagy eltávolítása tulajdonságai az eszközön
* Desk.cpl – A kijelző tulajdonságaihoz
* Main.cpl – Az egérrel, betűtípusokkal, billentyűzettel és nyomtatókkal kapcsolatos tulajdonságokhoz.
* Netcpl.cpl – Hálózattal kapcsolatos tulajdonságokhoz
* System.cpl – A rendszerrel kapcsolatos tulajdonságokhoz és az Új hardver hozzáadása varázslóhoz
* TimeDate.cpl – Dátum vagy idő tulajdonságokhoz
* Mlcfg32.cpl – A Microsoft Exchange vagy a Windows Messaging tulajdonságaihoz
* Intl.cpl – Ez a Regionális beállítások tulajdonságaira vonatkozik
* Modem.cpl – A modemmel kapcsolatos tulajdonságokhoz
* Themes.cpl – Asztali témákat és tulajdonságokat tárol.
* Password.cpl – A jelszó tulajdonságaihoz
* Mmsys.cpl – Multimédiás tulajdonságokhoz
* Wgpocpl.cpl – A Microsoft Mail Post Office-ra vonatkozik

## Rövid története ##

A CPL fájltípust a Microsoft Windows fejlesztette ki, és a Windows 1.0 óta a Windows operációs rendszer szerves részét képezi. Továbbra is minden Windows-verzióban használatos, és a vezérlőpult összes elemtulajdonsága ebben a fájltípusban tárolódik.

## CPL példa ##

Az alábbiakban egy minta CPL fájl látható:

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
