{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Що таке файл APPX?",
  "description":"Дізнайтеся про формат файлу APPX та API, які можуть створювати та відкривати файли APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Що таке файл APPX?

Файл APPX — це формат файлу пакета, що розповсюджується, який використовується для розповсюдження та встановлення програми. Він був представлений разом з Windows 8 для публікації в Microsoft Windows Store. Він містить усі файли, необхідні для встановлення програми Windows. До них належать метадані, файли та інформація про облікові дані. Більш сучасним форматом пакувального файлу є MSIX, який зараз використовується частіше порівняно з APPX.

## Формат файлу APPX – додаткова інформація

Файли APPX зберігаються як стиснуті файли у форматі [ZIP](/uk/стиснення/zip/). Це робить весь пакет архівним файлом зі зменшеним розміром, який легко завантажити в Microsoft Store.

## Як переглянути файли у файлі APPX?

Щоб переглянути вміст або файли у файлі APPX, слід виконати наступні дії.

1. Оскільки файли APPX зберігаються як стислі файли ZIP, перейменуйте файл у розширення .zip
1. Скористайтеся будь-яким інструментом декомпресії, таким як 7-Zip, WinZip або WinRAR, щоб розпакувати файли, що містяться у файлі APPX

## Як створити файл APPX?

Для створення файлів APPX можна використовувати два методи.

1. Використання MakeApp.exe – [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) використовується для створення обох пакети програм (.msix або .appx) і файли пакетів програм .msixbundle або .appxbundle). Крім того, він може видобувати файли з пакета програми. MakeApp.exe доступний із Windows 10 SDK і може використовуватися з командного рядка.
1. Використання Microsoft Visual Studio – розробники зазвичай [створюють файли APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) за допомогою Microsoft Visual Studio. Після того, як розробка програми завершена і програма готова до публікації, файл пакета APPX можна створити, опублікувавши його в Visual Studio.

## Список літератури

* [Створіть пакет або комплект MSIX за допомогою MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Створіть файли APPX за допомогою Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

