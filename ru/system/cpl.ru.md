{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "расширение", "файл", "формат", "система", "Файл панели управления", "Windows", "программы", "компьютер", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - файл панели управления",
  "description":"Узнайте о формате файла CPL и API-интерфейсах, которые могут создавать и открывать файлы CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .CPL вариант № ##

Файл CPL представляет собой тип «системного» файла. Он используется операционной системой Windows. Файл CPL — это сокращение от «Файл панели управления». Эти файлы представляют собой двоичные файлы, которые открываются с помощью панели управления в операционной системе Microsoft Windows и используются для представления и открытия инструментов, доступных на панели управления, таких как мышь, дисплеи, сеть и другие. Файлы CPL обычно хранятся в системной папке на вашем устройстве. Эти файлы не следует открывать вручную.


## Формат файла CPL ##

Различные файлы CPL в вашей операционной системе Windows связаны для представления разных элементов панели управления. Все элементы панели управления связаны с файлом CPL и имеют суффикс «.cpl», прикрепленный к их элементам.

Некоторые распространенные типы файлов CPL с их форматами:

* Inetcpl.cpl — для свойств Интернета на вашем устройстве.
* Appwiz.cpl — для добавления или удаления свойств программ на вашем устройстве
* Desk.cpl — для свойств дисплея
* Main.cpl — для свойств, связанных с мышью, шрифтами, клавиатурой и принтерами.
* Netcpl.cpl — для свойств, связанных с сетью
* System.cpl — для свойств, связанных с системой, и для мастера добавления нового оборудования.
* TimeDate.cpl — для свойств даты или времени
* Mlcfg32.cpl — для свойств Microsoft Exchange или Windows Messaging.
* Intl.cpl — относится к свойствам региональных настроек.
* Modem.cpl — для свойств, связанных с модемом
* Themes.cpl — хранит темы и свойства рабочего стола.
* Password.cpl — для свойств пароля
* Mmsys.cpl — для свойств мультимедиа
* Wgpocpl.cpl — относится к почтовому отделению Microsoft Mail.

## Краткая история ##

Тип файла CPL был разработан Microsoft Windows и является неотъемлемой частью операционной системы Windows, начиная с Windows 1.0. Он по-прежнему используется во всех версиях Windows, и все свойства элементов панели управления хранятся в этом типе файла.

## Пример CPL ##

Пример файла CPL можно увидеть ниже:

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
