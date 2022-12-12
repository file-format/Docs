{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "розширення", "файл", "формат", "система", "Файл панелі керування", "Windows", "програми", "комп'ютер", "програма" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - файл панелі керування",
  "description":"Дізнайтеся про формат файлу CPL та API, які можуть створювати та відкривати файли CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Що таке файл CPL? ##

Файл CPL є типом "системного" файлу. Він використовується операційною системою Windows. Файл CPL є скороченням від Control Panel File. Ці файли є двійковими файлами, які відкриваються за допомогою панелі керування в операційній системі Microsoft Windows і використовуються для представлення та відкриття інструментів, доступних на панелі керування, таких як миша, дисплеї, мережа тощо. Файли CPL зазвичай зберігаються в системній папці на вашому пристрої. Ці файли не можна відкривати вручну.


## Формат файлу CPL ##

Різні файли CPL у вашій операційній системі Windows підключаються, щоб представляти різні елементи панелі керування. Усі елементи панелі керування пов’язані з файлом CPL і мають суфікс «.cpl», доданий до їхніх елементів.

Деякі поширені типи файлів CPL з їх форматами:

* Inetcpl.cpl – для властивостей Інтернету на вашому пристрої
* Appwiz.cpl – для додавання або видалення властивостей програм на вашому пристрої
* Desk.cpl – для властивостей дисплея
* Main.cpl – для властивостей, пов’язаних із мишею, шрифтами, клавіатурою та принтерами.
* Netcpl.cpl – для мережевих властивостей
* System.cpl – для системних властивостей і майстра додавання нового обладнання
* TimeDate.cpl – для властивостей дати або часу
* Mlcfg32.cpl – для властивостей Microsoft Exchange або Windows Messaging
* Intl.cpl – це стосується властивостей регіональних налаштувань
* Modem.cpl – для властивостей, пов’язаних з модемом
* Themes.cpl – зберігає теми та властивості робочого столу.
* Password.cpl – для властивостей пароля
* Mmsys.cpl – для мультимедійних властивостей
* Wgpocpl.cpl – відноситься до Microsoft Mail Post Office

## Коротка історія ##

Тип файлу CPL був розроблений Microsoft Windows і є невід’ємною частиною операційної системи Windows, починаючи з Windows 1.0. Він досі використовується у всіх версіях Windows, і всі властивості елементів панелі керування зберігаються за допомогою цього типу файлу.

## Приклад CPL ##

Зразок файлу CPL можна побачити нижче:

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
