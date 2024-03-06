{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"failu",
"pagarinājumu",
"faila formātā",
"Visual Basic skripts",
"Programmēšanas rokasgrāmata",
"vbs piemērs",
"Microsoft Visual Basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS — Visual Basic skripta fails",
  "description": "Uzziniet par VBS failu formātu un API, kas var izveidot un atvērt VBS failus.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-lvs"
}
},
  "lastmod": "2021-08-24"
}

## Kas ir VBS fails?

VBS vai VBScript ir savienots ar Microsoft Visual Basic skriptu izdevumu. Skaitļošanas vidē lietotājam ir atļauts piekļūt daudziem tās aspektiem un kontrolēt tos. VBScript ir atļauts izmantot modeli ar nosaukumu **Component Object Model**, lai izmantotu vides elementus un rīkus. Šī vide ir paredzēta darbam un VBScript palaišanai.

Tas kalpo kā līdzīgs Javascript, ja klients tam piekļūst Web izstrādes jomā. To izmanto arī serveri tīmekļa lapu apstrādei. To var izmantot dažos citos skriptu failu veidos, piemēram, [HTML](/web/html/) lietojumprogrammās.


## Īsa vēsture ##

Tas pirmo reizi tika palaists 1996. gadā kā daļa no Microsoft izmantotajām tehnoloģijām, kas noteiktas Windows skriptiem. Sākotnēji tas tika īpaši izstrādāts tīmekļa izstrādātāju palīdzībai. Tajā pašā gadā tika izlaists Microsoft Windows pārlūks ar nosaukumu Internet Explorer kopā ar Visual Basic Script funkcijām.

Attīstoties tehnoloģijām un tīmekļa izstrādē, tika palaistas daudzas VBScript versijas, kā arī daudzas uzlabotas funkcijas. Turklāt nākamajā gadā šī skriptu valoda būs daļa no Microsoft Windows ar jaunām funkcijām.

## Tehniskā specifikācija Nr.

Tīmekļa lapām servera pusē kopā ar VBScript tiek izmantoti tādi rīki kā **Aktīvās servera lapas**. Šo skriptu valodu var izmantot arī Windows skriptu komponentā. Šīs valodas faili sistēmā Windows tiek glabāti ar paplašinājumu .vbs.

Šīs valodas kodā tiek izmantotas daudzas vadības struktūras, piemēram, cilpas. Tas ietver arī argumentus, kas ir komandrindas un var būt nosaukti vai nenosaukti. Šīs valodas failus var vienkārši saglabāt Windows operētājsistēmas mapēs vai darbvirsmā. Lai gan VBScript programmām, piemēram, Microsoft Script Editor, nav īpašas integrētas izstrādes vides, kas nodrošina šīs valodas izstrādes iespēju.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. Funkcijas, kas ietver vieglu vai tiešu piekļuvi, ietver tīkla printerus, nenosauktus un nosauktus komandrindas argumentus, stdout un stdin, tīkla koplietojumus, Windows pārvaldības instrumentus, lietotāju informāciju par tīkliem, piemēram, dalību grupā, un daudz ko citu. 

## VBS faila formāta piemērs ##

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

## Atsauce Nr.

* [VBS — Wikipedia](https://en.wikipedia.org/wiki/VBScript)




