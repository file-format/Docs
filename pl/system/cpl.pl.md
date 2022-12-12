{
  "date" : "2021-06-29",
  "keywords" :["CPL", "rozszerzenie", "plik", "format", "system", "Plik panelu sterowania", "Windows", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Plik Panelu Sterowania",
  "description":"Dowiedz się o formacie pliku CPL i interfejsach API, które mogą tworzyć i otwierać pliki CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik CPL? ##

Plik CPL jest rodzajem pliku „systemowego”. Jest używany przez system operacyjny Windows. Plik CPL jest skrótem od pliku panelu sterowania. Pliki te są plikami binarnymi, które otwierają się za pomocą panelu sterowania w systemie operacyjnym Microsoft Windows i służą do reprezentowania i otwierania narzędzi dostępnych w panelu sterowania, takich jak między innymi Mysz, Wyświetlacze, Sieć. Pliki CPL są zwykle przechowywane w folderze systemowym na twoim urządzeniu. Tych plików nie należy otwierać ręcznie.


## Format pliku CPL ##

Różne pliki CPL w systemie operacyjnym Windows są połączone w celu reprezentowania różnych elementów panelu sterowania. Wszystkie elementy panelu sterowania są połączone z plikiem CPL i mają dołączony do nich przyrostek „.cpl”.

Niektóre popularne typy plików CPL wraz z ich formatami to:

* Inetcpl.cpl — dla właściwości internetowych na Twoim urządzeniu
* Appwiz.cpl – Aby dodać lub usunąć właściwości programów na urządzeniu
* Desk.cpl — dla właściwości wyświetlania
* Main.cpl — dla właściwości związanych z myszą, czcionkami, klawiaturą i drukarkami.
* Netcpl.cpl — dla właściwości związanych z siecią
* System.cpl — dla właściwości związanych z systemem i kreatora dodawania nowego sprzętu
* TimeDate.cpl – dla właściwości daty lub godziny
* Mlcfg32.cpl — dla właściwości Microsoft Exchange lub Windows Messaging
* Intl.cpl — dotyczy właściwości ustawień regionalnych
* Modem.cpl – dla właściwości związanych z modemem
* Themes.cpl – Przechowuje motywy i właściwości pulpitu.
* Password.cpl — dla właściwości hasła
* Mmsys.cpl – dla właściwości multimedialnych
* Wgpocpl.cpl — dotyczy poczty Microsoft Mail

## Krótka historia ##

Typ pliku CPL został opracowany przez Microsoft Windows i jest integralną częścią systemu operacyjnego Windows od wersji Windows 1.0. Jest nadal używany we wszystkich wersjach systemu Windows, a wszystkie właściwości elementów panelu sterowania są przechowywane przy użyciu tego typu pliku.

## CPL Przykład ##

Przykładowy plik CPL można zobaczyć poniżej:

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
