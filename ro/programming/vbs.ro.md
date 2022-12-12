{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "fișier", "extensie", "format fișier", "Visual Basic Script", "Ghid de programare", "exemplu vbs", "Microsoft Visual Basic", "VBScript"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Fișier Script Visual Basic",
  "description":"Aflați despre formatul de fișier VBS și despre API-urile care pot crea și deschide fișiere VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Ce este un fișier VBS?

VBS sau VBScript este conectat cu ediția de script Microsoft Visual Basic. În mediul de calcul, utilizatorului i se permite să acceseze și să controleze multe aspecte ale acestuia. VBScript are permisiunea de a utiliza un model numit **Component Object Model** pentru a beneficia de elementele și instrumentele mediului. Acest mediu este specificat pentru funcționarea și rularea VBScript.

Acesta servește la fel de similar cu Javascript atunci când este accesat de client în domeniul dezvoltării Web. De asemenea, este folosit de servere pentru prelucrarea paginilor web. Poate fi luat în considerare în alte tipuri de fișiere de scripting, cum ar fi aplicațiile [HTML](/ro/web/html/).


## Scurt istoric ##

A fost lansat pentru prima dată în 1996, ca parte a tehnologiilor utilizate de Microsoft specificate pentru Windows Scripts. A fost dezvoltat special pentru ajutorul dezvoltatorilor web inițial. În același an, exploratorul Microsoft Windows numit Internet Explorer a fost lansat împreună cu caracteristicile Visual Basic Script.

Odată cu progresul în tehnologie și dezvoltare web, au fost lansate multe versiuni de VBScript împreună cu multe caracteristici avansate. Mai mult, în anul viitor, acest limbaj de scripting va face parte din Microsoft Windows cu noi funcții.

## Specificatii tehnice ##

Pentru paginile web de pe partea serverului, instrumentele precum **Active Server Pages** sunt utilizate împreună cu VBScript. Acest limbaj de scripting poate fi folosit și în componenta de script din Windows. Fișierele acestei limbi sunt stocate cu o extensie .vbs în Windows.

Există multe structuri de control, cum ar fi bucle, care sunt utilizate în codul acestui limbaj. Include, de asemenea, argumente care sunt în linie de comandă și pot fi numite sau nenumite. Fișierele din această limbă pot fi stocate pur și simplu în folderele sau pe desktopul unui sistem de operare Windows. Deși nu există un mediu de dezvoltare integrat specific pentru programele VBScript, cum ar fi Microsoft Script Editor, oferă facilitatea de dezvoltare a acestui limbaj.

Când VBScript este găzduit de gazda Script din Windows, acesta oferă diverse caracteristici care sunt destul de comune pentru limbajele de scriptare, dar nu sunt disponibile în Visual Basic 6.0. Caracteristicile care implică acces ușor sau direct implică imprimante de rețea, argumente de linie de comandă nenumite și denumite, stdout și stdin, partajări de rețea, instrumente de gestionare Windows, informații despre utilizatori din rețele precum apartenența la grup și multe altele.

## Exemplu de format de fișier VBS ##

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

## Referință ##

* [VBS - de Wikipedia](https://en.wikipedia.org/wiki/VBScript)



