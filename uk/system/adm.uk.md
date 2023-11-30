{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ADM - формат файлу адміністративного шаблону",
  "description":"Дізнайтеся про формат файлу ADM і як відкрити файли ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Що таке файл ADM?

Файл ADM — це файл шаблону, який використовується програмним забезпеченням Microsoft Group Policies для визначення розташування параметрів політики на основі реєстру у файлі реєстру. Він використовується системними адміністраторами для визначення політики керування групою комп’ютерів, які входять до групи. Ця інформація стає частиною об’єктів групової політики (GPO), створених для керування групою.

Файли ADM можна відкрити за допомогою редактора об’єктів групової політики Microsoft.

## Формат файлу ADM - Додаткова інформація

Файли ADM зберігаються як текстові файли у форматі Юнікод. Вони в основному використовувалися для опису розташування параметрів політики на основі реєстру в реєстрі Windows Vista та Windows 7.

Файли ADM більше не підтримуються та були замінені файлами [ADMX](/uk/system/admx/). GPA ігнорує такі файли ADM за замовчуванням на комп’ютерах під керуванням Microsoft Windows Vista з пакетом оновлень 1 або новішої версії.

* system.adm
* inetres.adm
* конф.адм
* wmplayer.adm
* wuau.adm

## Список літератури

* [Файли адміністративних шаблонів - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – керування файлами адміністративних шаблонів](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

