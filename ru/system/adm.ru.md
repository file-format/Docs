{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ADM — формат файла административного шаблона",
  "description":"Узнайте о формате файла ADM и о том, как открыть файлы ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADM вариант №

Файл ADM — это файл шаблона, используемый программным обеспечением групповых политик Microsoft для указания местоположения параметров политики на основе реестра в файле реестра. Он используется системными администраторами для определения политики управления группой компьютеров, входящих в группу. Эта информация становится частью объектов групповой политики (GPO), созданных для управления группой.

Вы можете открыть файлы ADM с помощью редактора объектов групповой политики Microsoft.

## Формат файла ADM — дополнительная информация

Файлы ADM хранятся как текстовые файлы в формате Юникода. В основном они использовались для описания расположения параметров политики на основе реестра в реестре Windows Vista и Windows 7.

Файлы ADM больше не поддерживаются и заменены файлами [ADMX](/ru/system/admx/). GPA игнорирует следующие файлы ADM по умолчанию на компьютерах под управлением Microsoft Windows Vista с пакетом обновления 1 или более поздней версии.

* система.адм
* inetres.adm
* конф.адм
* wmplayer.adm
* wuau.adm

## Рекомендации

* [Файлы административных шаблонов — ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ — Управление файлами административных шаблонов] (https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

