{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "файл", "разширение", "файлов формат", "Visual Basic Script", "Ръководство за програмиране", "vbs пример", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - файл със скрипт на Visual Basic",
  "description":"Научете за VBS файловия формат и API, които могат да създават и отварят VBS файлове.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Какво е VBS файл?

VBS или VBScript е свързан със скриптовото издание на Microsoft Visual Basic. В компютърната среда на потребителя е разрешен достъп и контрол на много аспекти от нея. VBScript има право да използва модел, наречен **Component Object Model**, за да се възползва от елементите и инструментите на средата. Тази среда е определена за работа и изпълнение на VBScript.

Той служи като подобен на Javascript, когато е достъпен от клиента в областта на уеб разработката. Използва се и от сървърите за обработка на уеб страници. Може да се има предвид в някои други типове скриптови файлове като приложения на [HTML](/bg/web/html/).


## Кратка история ##

Той беше пуснат за първи път през 1996 г. като част от технологиите, използвани от Microsoft, определени за Windows Scripts. Първоначално е разработен специално за помощ на уеб разработчиците. През същата година беше пуснат изследователят на Microsoft Windows, наречен Internet Explorer, заедно с функциите на Visual Basic Script.

С напредъка в технологиите и уеб разработката бяха пуснати много версии на VBScript заедно с много разширени функции. Освен това през следващата година този скриптов език ще бъде част от Microsoft Windows с нови функции.

## Техническа спецификация ##

За уеб страниците от страната на сървъра се използват инструменти като **Active Server Pages** заедно с VBScript. Този скриптов език може да се използва и в скриптовия компонент на Windows. Файловете на този език се съхраняват с разширение .vbs в Windows.

Има много контролни структури като цикли, които се използват в кода на този език. Той също така включва аргументи, които са команден ред и могат да бъдат именувани или неименувани. Файловете на този език могат да се съхраняват просто в папките или на работния плот на операционна система Windows. Въпреки че няма специфична интегрирана среда за разработка на VBScript програми като Microsoft Script Editor, предоставят възможност за разработка на този език.

Когато VBScript се хоства от Script хоста на Windows, той предоставя различни функции, които са доста общи за езиците на скриптове, но не са налични във Visual Basic 6.0. Функциите, които включват лесен или директен достъп, включват мрежови принтери, ненаименувани и наименувани аргументи на командния ред, stdout и stdin, мрежови споделяния, Windows Management Instrumentation, потребителска информация за мрежи като членство в група и много други.

## Пример за VBS файлов формат ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Референция ##

* [VBS - от Wikipedia](https://en.wikipedia.org/wiki/VBScript)



