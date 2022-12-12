{
  "date" : "2021-08-24", 
  "keywords" :["vbs", "plik", "rozszerzenie", "format pliku", "Skrypt Visual Basic", "Przewodnik programowania", "przykład vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - plik skryptu języka Visual Basic",
  "description":"Poznaj format plików VBS i interfejsy API, które mogą tworzyć i otwierać pliki VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Czym jest plik VBS?

VBS lub VBScript jest powiązany ze skryptową edycją Microsoft Visual Basic. W środowisku komputerowym użytkownik ma dostęp do wielu jego aspektów i może je kontrolować. VBScript może używać modelu o nazwie **Component Object Model** w celu wykorzystania elementów i narzędzi środowiska. To środowisko jest przeznaczone do pracy i uruchamiania języka VBScript.

Służy jako podobny do Javascript, gdy klient uzyskuje do niego dostęp w dziedzinie tworzenia stron internetowych. Jest również używany przez serwery do przetwarzania stron internetowych. Można to rozważyć w niektórych innych typach plików skryptów, takich jak aplikacje [HTML](/pl/web/html/).


## Krótka historia ##

Po raz pierwszy został uruchomiony w 1996 roku jako część technologii używanych przez Microsoft, określonych dla skryptów Windows. Został on początkowo opracowany specjalnie z myślą o pomocy programistom internetowym. W tym samym roku został wydany eksplorator Microsoft Windows o nazwie Internet Explorer wraz z funkcjami Visual Basic Script.

Wraz z postępem technologii i rozwoju sieci pojawiło się wiele wersji VBScript wraz z wieloma zaawansowanymi funkcjami. Co więcej, w nadchodzącym roku ten język skryptowy będzie częścią systemu Microsoft Windows z nowymi funkcjami.

## Specyfikacja techniczna ##

W przypadku stron internetowych po stronie serwera narzędzia takie jak **Active Server Pages** są używane wraz z VBScript. Ten język skryptowy może być również używany w komponencie skryptowym systemu Windows. Pliki tego języka są przechowywane w systemie Windows z rozszerzeniem .vbs.

Istnieje wiele struktur kontrolnych, takich jak pętle, które są używane w kodzie tego języka. Zawiera również argumenty, które są wierszem poleceń i mogą być nazwane lub nienazwane. Pliki tego języka można po prostu przechowywać w folderach lub na pulpicie systemu operacyjnego Windows. Chociaż nie ma określonego zintegrowanego środowiska programistycznego dla programów VBScript, takie jak Microsoft Script Editor zapewniają łatwość rozwoju tego języka.

Gdy język VBScript jest hostowany przez hosta skryptów systemu Windows, zapewnia różne funkcje, które są dość wspólne dla języków skryptowych, ale nie są dostępne w języku Visual Basic 6.0. Funkcje wymagające łatwego lub bezpośredniego dostępu obejmują drukarki sieciowe, nienazwane i nazwane argumenty wiersza poleceń, stdout i stdin, udziały sieciowe, Instrumentację zarządzania Windows, informacje o użytkownikach sieci, takie jak członkostwo w grupach i wiele innych.

## Przykład formatu pliku VBS ##

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

## Odniesienie ##

* [VBS – z Wikipedii](https://en.wikipedia.org/wiki/VBScript)



