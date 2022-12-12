{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "soubor", "přípona", "formát souboru", "Skript jazyka Visual Basic", "Průvodce programováním", "příklad vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - soubor skriptu Visual Basic",
  "description":"Další informace o formátu souborů VBS a rozhraních API, která mohou vytvářet a otevírat soubory VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Co je soubor VBS?

VBS nebo VBScript je spojen s edicí skriptů Microsoft Visual Basic. Ve výpočetním prostředí je uživateli umožněn přístup a ovládání mnoha jeho aspektů. VBScript může používat model s názvem **Component Object Model** k využití prvků a nástrojů prostředí. Toto prostředí je určeno pro práci a spouštění VBScriptu.

Slouží jako obdoba Javascriptu, když k němu klient přistupuje v oblasti vývoje webu. Servery jej také využívají pro zpracování webových stránek. Může být uvažován v některých jiných typech skriptovacích souborů, jako jsou aplikace [HTML](/cs/web/html/).


## Stručná historie ##

Poprvé byl spuštěn v roce 1996 jako součást technologií používaných společností Microsoft určených pro skripty Windows. Původně byl speciálně vyvinut pro pomoc vývojářům webu. Ve stejném roce byl vydán průzkumník Microsoft Windows s názvem Internet Explorer spolu s funkcemi Visual Basic Script.

S pokrokem v technologii a vývoji webu bylo spuštěno mnoho verzí VBScript spolu s mnoha pokročilými funkcemi. Navíc v nadcházejícím roce bude tento skriptovací jazyk součástí Microsoft Windows s novými funkcemi.

## Technická specifikace ##

Pro webové stránky na straně serveru se spolu s VBScriptem používají nástroje jako **Active Server Pages**. Tento skriptovací jazyk lze také použít ve skriptovací součásti systému Windows. Soubory tohoto jazyka jsou ve Windows uloženy s příponou .vbs.

Existuje mnoho řídicích struktur, jako jsou smyčky, které se používají v kódu tohoto jazyka. Zahrnuje také argumenty, které jsou příkazovým řádkem a mohou být pojmenované nebo nepojmenované. Soubory tohoto jazyka mohou být uloženy jednoduše ve složkách nebo na ploše operačního systému Windows. Ačkoli neexistuje žádné specifické integrované vývojové prostředí pro programy VBScript, jako je Microsoft Script Editor, poskytuje možnost vývoje tohoto jazyka.

Když je VBScript hostován hostitelem Script systému Windows, poskytuje různé funkce, které jsou zcela běžné pro jazyky skriptování, ale nejsou dostupné ve Visual Basic 6.0. Funkce, které zahrnují snadný nebo přímý přístup, zahrnují síťové tiskárny, nepojmenované a pojmenované argumenty příkazového řádku, stdout a stdin, síťové sdílené položky, Windows Management Instrumentation, uživatelské informace sítí, jako je členství ve skupinách a mnoho dalšího.

## Příklad formátu souboru VBS ##

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

## reference ##

* [VBS – z Wikipedie](https://en.wikipedia.org/wiki/VBScript)



