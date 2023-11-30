{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл VDISCO - формат файлу документа DISCO Dynamic Discovery",
  "description":"Дізнайтеся, що таке файл VDISCO?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Що таке файл VDISCO?

Файл VDISCO — це файл виявлення, який використовується Microsoft Visual Studio у своїх веб-службах. Він надає інформацію про доступні веб-сервіси, наприклад їхні URL-адреси, простори імен і методи. Файл VDISCO схожий на формат файлу [DISCO](/uk/web/disco/), але створюється під час виконання. Він зберігається в програмі веб-служб і використовується Visual Studio для динамічного виявлення та використання веб-служб у проекті. Файли VDISCO використовуються разом із файлом [.asmx](/uk/web/asmx/), який містить фактичний код веб-служби.

Ви можете відкрити файл VDISCO в будь-якому текстовому редакторі, наприклад Microsoft Notepad, Github Atom і Apple TextEdit. Його також можна відкрити за допомогою Microsoft Visual Studio 2012 і новішої версії для роботи з ним.

## Формат файлу VDISCO

Файл VDISCO зберігається та розміщується у форматі [XML](/uk/web/xml/), який є універсальним форматом для створення та публікації даних. Він містить URL-адресу служби, простори імен і методи в стандартних тегах XML, де кожен тег містить відповідне значення своєї інформації.

## Список літератури

* [ДИСКО](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Виявлення веб-служб](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Приклад C# класу DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

