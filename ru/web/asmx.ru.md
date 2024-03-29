{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "файл asmx", "формат файла asmx", "тип файла asmx", "файл", "тип", "что такое файл asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX — файл веб-службы ASP.NET",
  "description" :"Узнайте, что такое файл ASMX и API, которые могут создавать и открывать файлы ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASMX вариант №

Файл с расширением .asmx — это файл веб-службы ASP.NET, который обеспечивает связь между двумя объектами через Интернет с использованием протокола SOAP. Он развертывается как служба на веб-сервере под управлением Windows для обработки входящего запроса и возврата ответа. В отличие от файлов [ASPX](/ru/web/aspx/), которые содержат код для визуального отображения веб-страниц ASP.NET, файлы ASMX запускаются на сервере в фоновом режиме и выполняют различные задачи, такие как подключение к базе данных, извлечение данных и их возврат в формат, в котором был сделан запрос. Они используются специально для веб-служб XML.

## Формат файла ASMX

Файлы ASMX имеют обычный текстовый формат и могут открываться или редактироваться в таких приложениях, как Microsoft Visual Studio или текстовых редакторах. Это собственный формат файлов Microsoft, который имеет четко определенный синтаксис для создания веб-сервисов. Ответ ASMX-файла в форме SOAP XML состоит из следующих элементов.

* `Envelop` — корневой элемент, идентифицирующий XML-документ как сообщение SOAP.
* «Заголовок» — необязательный элемент, который содержит информацию о приложении, такую как данные аутентификации. Если присутствует элемент Header, он должен быть первым дочерним элементом элемента Envelope.
* `Body` - Содержит SOAP-сообщение, предназначенное для получателя.
* `Fault` — необязательный элемент, используемый для обозначения сообщений об ошибках. Если присутствует элемент Fault, он должен быть дочерним элементом элемента Body.

Файлы ASMX могут быть написаны на языках .NET, таких как [C#](/ru/programming/cs/), [Visual Basic](/ru/programming/vb/) или JScript.

## Чем ASMX отличается от ASPX и ASCX?

Файлы ASMX отличаются от файлов ASPX и ASCX.

* ASPX, Active Server Pages, файлы — это программные файлы, созданные с использованием платформы Microsoft ASP.NET, работающей на веб-серверах. Они отображаются в веб-браузере клиента, когда пользователь запрашивает доступ к такой странице.
* ASCX, Active Server User Control, определяет пользовательские элементы управления, которые используются для определения повторно используемых элементов управления на веб-страницах ASP.NET или на всем веб-сайте.

## использованная литература

* [Использование службы ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Пользовательский контроль ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

