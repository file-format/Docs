{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"uzadılması",
"fayl",
"format",
"sistemi",
"İdarəetmə Paneli Faylı",
"Windows",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL - İdarəetmə Paneli Faylı",
  "description": "CPL faylları yarada və aça bilən CPL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-azl"
}
},
  "lastmod": "2021-06-29"
}

## CPL faylı nədir? ##

CPL faylı sistem faylının bir növüdür. Windows əməliyyat sistemi tərəfindən istifadə olunur. CPL faylı İdarəetmə Paneli Faylı üçün qısadır. Bu fayllar Microsoft Windows əməliyyat sistemində idarəetmə paneli ilə açılan ikili fayllardır və idarəetmə panelində mövcud olan Siçan, Ekranlar, Şəbəkə və digər alətləri göstərmək və açmaq üçün istifadə olunur. CPL faylları adətən cihazınızda sistem qovluğunda saxlanılır. Bu fayllar əl ilə açılmamalıdır.


## CPL Fayl Format ##

Windows əməliyyat sisteminizdəki müxtəlif CPL faylları müxtəlif idarəetmə paneli elementlərini təmsil etmək üçün birləşdirilir. Bütün idarəetmə paneli elementləri CPL faylı ilə əlaqələndirilir və onların elementlərinə .cpl” şəkilçisi əlavə olunur.

Formatları ilə bəzi ümumi CPL fayl növləri bunlardır:

* Inetcpl.cpl – Cihazınızdakı İnternet xüsusiyyətləri üçün

* Appwiz.cpl – Cihazınızda Proqram xüsusiyyətlərini əlavə etmək və ya silmək üçün

* Desk.cpl – Ekran xassələri üçün

* Main.cpl – Siçan, Şriftlər, Klaviatura və Printerlərlə əlaqəli xüsusiyyətlər üçün. 

* Netcpl.cpl – Şəbəkə ilə əlaqəli xüsusiyyətlər üçün

* System.cpl – Sistemlə əlaqəli xüsusiyyətlər və Yeni Avadanlıq Sihirbazı əlavə etmək üçün

* TimeDate.cpl – Tarix və ya Saat xassələri üçün

* Mlcfg32.cpl – Microsoft Exchange və ya Windows Mesajlaşma xassələri üçün

* Intl.cpl – Bu, Regional Parametrlər xassələrinə aiddir

* Modem.cpl – Modemlə əlaqəli xüsusiyyətlər üçün

* Themes.cpl – Desktop Mövzularını və xassələrini saxlayır. 

* Password.cpl – Parol xassələri üçün

* Mmsys.cpl – Multimedia xassələri üçün

* Wgpocpl.cpl – Microsoft Mail Post Office-ə aiddir


## Qısa tarix ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. O, hələ də bütün Windows versiyalarında istifadə olunur və bütün idarəetmə paneli elementləri bu fayl növündən istifadə edərək saxlanılır.

## CPL Nümunəsi ##

Nümunə CPL faylı aşağıda görünə bilər:

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
