{
  "date": "2021-08-24",
  "keywords": [
"vbs",
"failą",
"pratęsimas",
"Dokumento formatas",
"Visual Basic scenarijus",
"Programavimo vadovas",
"vbs pavyzdys",
"Microsoft Visual Basic",
"VBScript"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VBS – „Visual Basic“ scenarijaus failas",
  "description": "Sužinokite apie VBS failo formatą ir API, kurios gali kurti ir atidaryti VBS failus.",
  "linktitle": "VBS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vb-lts"
}
},
  "lastmod": "2021-08-24"
}

## Kas yra VBS failas?

VBS arba VBScript yra sujungti su Microsoft Visual Basic scenarijaus leidimu. Skaičiavimo aplinkoje vartotojui leidžiama pasiekti ir valdyti daugelį jos aspektų. VBScript leidžiama naudoti modelį, pavadintą **Component Object Model**, kad būtų galima pasinaudoti aplinkos elementais ir įrankiais. Ši aplinka skirta darbui ir VBScript paleidimui.

Jis veikia kaip Javascript, kai klientas jį pasiekia interneto kūrimo srityje. Jį taip pat naudoja serveriai tinklalapiams apdoroti. Jis gali būti naudojamas kai kurių kitų tipų scenarijų failuose, pvz., [HTML](/web/html/) programose.


## Trumpa istorija ##

Pirmą kartą jis buvo paleistas 1996 m. kaip Microsoft naudojamų Windows Scripts technologijų dalis. Iš pradžių jis buvo specialiai sukurtas žiniatinklio kūrėjų pagalbai. Tais pačiais metais buvo išleista Microsoft Windows naršyklė, pavadinta Internet Explorer, kartu su Visual Basic Script funkcijomis.

Tobulėjant technologijoms ir žiniatinklio kūrimui, buvo išleista daug VBScript versijų ir daug pažangių funkcijų. Be to, ateinančiais metais ši scenarijų kalba bus Microsoft Windows dalis su naujomis funkcijomis.

## Techninė specifikacija Nr.

Serverio puslapiuose kartu su VBScript naudojami įrankiai, tokie kaip **Active Server Pages**. Šią scenarijų kalbą taip pat galima naudoti Windows scenarijaus komponente. Šios kalbos failai sistemoje Windows saugomi su plėtiniu .vbs.

Šios kalbos kode yra daug valdymo struktūrų, tokių kaip kilpos. Tai taip pat apima argumentus, kurie yra komandinės eilutės ir gali būti pavadinti arba neįvardinti. Šios kalbos failus galima laikyti tiesiog aplankuose arba Windows operacinės sistemos darbalaukyje. Nors nėra specialios integruotos VBScript programų kūrimo aplinkos, tokios kaip Microsoft Script Editor, suteikia galimybę kurti šią kalbą.

When VBScript is hosted by the Script host of Windows, it provides various features that are quite common to the languages of scripting but are not available in Visual Basic 6.0. Funkcijos, kurios apima lengvą arba tiesioginę prieigą, apima tinklo spausdintuvus, neįvardytus ir įvardintus komandų eilutės argumentus, stdout ir stdin, tinklo dalis, Windows valdymo instrumentus, vartotojų informaciją apie tinklus, pvz., grupės narystę, ir daug daugiau. 

## VBS failo formato pavyzdys ##

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

## Nuoroda ##

* [VBS – pateikė Vikipedija](https://en.wikipedia.org/wiki/VBScript)




