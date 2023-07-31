{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - довідковий файл макросів Microsoft Office",
  "description":"Дізнайтеся про файл MSO та API, які можуть створювати та відкривати файли MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Що таке файл MSO?

Файл MSO — це формат файлу-контейнера даних, який створюється під час надсилання повідомлення HTML за допомогою Microsoft Outlook. Це відбувається переважно з програмами Microsoft Office 2000. У більшості випадків повідомлення електронної пошти вкладається з іменем файлу **Oledata.mso**. Одержувач електронної пошти, коли відкриває такий електронний лист, може правильно переглянути файл, навіть якщо у нього не встановлено те саме програмне забезпечення. Файли MSO стосуються [формату файлів складених документів Microsoft (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Формат файлу Microsoft MSO

Файли MSO зберігаються у форматі Microsoft Compound Document File Format (MCDF), який також відомий як Object Linking and Embedding (OLE) або Component Object Model (COM).

### Структура формату файлу MSO

Внутрішня структура формату файлу MSO чітко визначена в [Структурах](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) розділ документації MCDF. Таблиця розміщення файлів (FAT) керує розподілом секторів і ланцюжками секторів. Він містить масив 32-розрядних номерів секторів. Кожен індекс у масиві представляє номер сектора, тоді як його значення представляє наступний сектор у ланцюжку або спеціальне значення.

## Список літератури

* [Структуроване сховище COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Формат файлу складеного документа Microsoft (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

