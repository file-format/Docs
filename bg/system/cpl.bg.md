{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "разширение", "файл", "формат", "система", "Файл на контролния панел", "Windows", "програми", "компютър", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Файл на контролния панел",
  "description":"Научете за CPL файловия формат и API, които могат да създават и отварят CPL файлове.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Какво е CPL файл? ##

CPL файлът е тип "системен" файл. Използва се от операционната система Windows. CPL файлът е съкращение от файл на контролния панел. Тези файлове са двоични файлове, които се отварят с контролния панел в операционна система Microsoft Windows и се използват за представяне и отваряне на инструментите, налични в контролния панел, като например мишка, дисплеи, мрежи и други. CPL файловете обикновено се съхраняват в системната папка на вашето устройство. Тези файлове не трябва да се отварят ръчно.


## CPL файлов формат ##

Различни CPL файлове във вашата операционна система Windows са свързани, за да представляват различни елементи на контролния панел. Всички елементи на контролния панел са свързани към CPL файл и имат суфикс „.cpl“, прикачен към техните елементи.

Някои често срещани типове CPL файлове с техните формати са:

* Inetcpl.cpl – За интернет свойства на вашето устройство
* Appwiz.cpl – За добавяне или премахване на свойства на програми на вашето устройство
* Desk.cpl – За свойствата на дисплея
* Main.cpl – За свойства, свързани с мишка, шрифтове, клавиатура и принтери.
* Netcpl.cpl – За свойства, свързани с мрежата
* System.cpl – За свързани със системата свойства и за съветника за добавяне на нов хардуер
* TimeDate.cpl – За свойства за дата или час
* Mlcfg32.cpl – За свойства на Microsoft Exchange или Windows Messaging
* Intl.cpl – Това се отнася за свойствата на регионалните настройки
* Modem.cpl – За свойства, свързани с модема
* Themes.cpl – Съхранява теми и свойства за работния плот.
* Password.cpl – За свойствата на паролата
* Mmsys.cpl – За мултимедийни свойства
* Wgpocpl.cpl – Отнася се за Microsoft Mail Post Office

## Кратка история ##

Файловият тип CPL е разработен от Microsoft Windows и е неразделна част от операционната система Windows от Windows 1.0. Той все още се използва във всички версии на Windows и всички свойства на елементи от контролния панел се съхраняват с помощта на този тип файл.

## Пример за CPL ##

Примерен CPL файл може да се види по-долу:

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
