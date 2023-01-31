{
  "date" : "2019-10-11",
  "keywords" :[ "файл vstx", "формат файлу vstx", "що таке файл vstx", "файл", "приклад vstx", "розширення файлу vstx", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - формат файлу Microsoft Visio",
  "description":"Дізнайтеся про формат файлу VSTX та API, які можуть створювати та відкривати файли VSTX.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл VSTX?

Файли з розширенням .vstx — це файли шаблонів малюнків, створені за допомогою Microsoft Visio 2013 і новіших версій. Ці файли VSTX є відправною точкою для створення креслень Visio, збережених як файли [.VSDX](/uk/image/vsdx/) із макетом і параметрами за замовчуванням. Загалом файли Visio використовуються для створення креслень, які містять візуальні об’єкти, блок-схеми, діаграми UML, потік інформації, організаційні діаграми, діаграми програмного забезпечення, макет мережі, моделі бази даних, відображення об’єктів та іншу подібну інформацію. Файли, створені за допомогою Visio, також можна експортувати в різні формати файлів, наприклад [PNG](/uk/Image/PNG/), [BMP](/uk/Image/BMP/), [PDF](/uk/pdf/) та інші. Програми, які відкривають файли VSTX, включають Microsoft Visio для Windows і Mac, які дозволяють відкривати ці файли для перегляду та редагування. Він також дозволяє конвертувати формати файлів Visio у низку інших форматів.

# Формат файлу VSTX #

«X» у розширенні файлу означає формат файлу OpenOffice, який Microsoft представила як формат архівного файлу [ZIP](/uk/compression/zip/) для заміни двійкових форматів файлів, які підтримувалися раніше. Таким чином, файли VSTX базуються на форматі файлу XML специфікацій OpenOffice, на відміну від формату файлу [.VST](/uk/image/vst/), який має двійковий формат.

Файли VSDX базуються на Open Packaging Conventions і XML, і розробники можуть скористатися цим форматом, навчившись працювати з цими файлами програмно. Цей формат успадковує багато тих самих XML-структур як його частини від формату файлу Visio XML Drawing (.vdx). Сумісність із файлами Visio значно покращена, оскільки програмне забезпечення сторонніх виробників може маніпулювати файлами Visio на рівні формату файлу.

Певні інші типи файлів, які складають формат файлу Visio 2013, включають:

* .vsdm (креслення Visio із підтримкою макросів)
* .vssx (трафарет Visio)
* .vssm (трафарет Visio із підтримкою макросів)
* .vstx (шаблон Visio)
* .vstm (шаблон Visio із підтримкою макросів)

Під капотом у форматі файлів Visio 2013 використовуються структуровані засоби для зберігання даних програми разом із пов’язаними ресурсами в архіві, наприклад [ZIP](/uk/Compression/ZIP/). ZIP-файл можна розпакувати за допомогою будь-якої стандартної утиліти видобування, якщо він також містить файли інших типів. Ви можете просто замінити розширення файлу .VSTX на .ZIP у вікні огляду, щоб побачити вміст у файлі VSTX.

Кожен файл Visio називається пакетом, який містить інші файли або частини. Частина пакета може бути файлом XML, зображенням або навіть рішенням VBA. Частини всередині пакета можна розділити на частини «документ» і «відносини».

### Документ ###

Частини документа містять фактичний вміст і метадані файлу Visio, наприклад назву файлу, першу сторінку та всі фігури, які він містить, і навіть зв’язки даних для фігур. Зображення та текстові файли в пакеті вважаються частинами документа.

### стосунки ###

Частини зв’язку у файлі Visio зберігаються в папці «_rels» і описують, як частини в пакеті пов’язані з кожною. Він також забезпечує структуру файлу. Автономний XML-документ використовує зв’язок батьків/дочірніх елементів для визначення зв’язку сутностей один з одним. Дійсний формат файлу Visio 2013 містить правильний набір частин, а пакет містить зв’язки між частинами.

Частини зв’язку — це документи XML, які описують зв’язки між різними частинами документа в пакеті. Вони визначають зв’язок між двома елементами: вказаним джерелом (визначеним іменем і розташуванням файлу зв’язку) і зазначеною цільовою частиною документа. Наприклад, частини зв’язку використовуються для опису того, які зразки фігур пов’язані з файлом, як сторінки пов’язані з файлом і одна з одною або як зображення та об’єкти пов’язані з певною сторінкою.

## Посилання ##

* [Знайомство з форматом файлу Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
