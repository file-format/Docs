{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM файл – файлов формат на административен шаблон",
  "description":"Научете за файловия формат ADM и как да отваряте ADM файлове.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Какво е ADM файл?

ADM файлът е шаблонен файл, използван от софтуера на Microsoft Group Policies за указване на местоположението на настройките на правилата, базирани на регистъра, във файла на системния регистър. Използва се от системните администратори за определяне на правилата за управление на група компютри, които са част от групата. Тази информация става част от обектите на груповата политика (GPO), които са създадени за управление на групата.

Можете да отваряте ADM файлове с помощта на Microsoft Group Policy Object Editor.

## ADM файлов формат - повече информация

ADM файловете се съхраняват като форматирани в Unicode текстови файлове. Те бяха използвани предимно за описване на местоположението на настройките на правилата, базирани на регистъра, в системния регистър на Windows Vista и Windows 7.

ADM файловете вече не се поддържат и са заменени от [ADMX](/bg/system/admx/) файловете. GPA игнорира следните ADM файлове по подразбиране на компютри с Microsoft Windows Vista Service Pack 1 или по-нова версия.

* system.adm
* inetres.adm
* конф.адм
* wmplayer.adm
* wuau.adm

## Препратки

* [Файлове с административни шаблони - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Управление на файлове с административни шаблони](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

