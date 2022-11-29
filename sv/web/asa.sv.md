{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "filformat", "filtyp", "vad är en .asa-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP-konfigurationsfil",
  "description" :"Läs mer om vad en ASA-fil och API:er är som kan skapa och öppna ASA-filer.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Vad är ASA fil?

En ASA-fil är en konfigurationsfil, skapad för [ASP](/sv/web/asp/)/ASP.NET-projekt. Den innehåller deklarationer av variabler, innehåller och funktioner som är avsedda att vara tillgängliga på global nivå i applikationen. Alla sidor i projektet kan komma åt dessa variabler och funktioner och på så sätt undvika kravet på att skriva om dessa. Ett sådant exempel är Global.asa-sidan som lagras i rotkatalogen för att vara tillgänglig för andra ASP-webbsidor. Global.asa-filer är valfria, men om de används kan varje applikation bara ha en Global.asa-fil.

## ASA-filformat - Mer information

ASA-filer är vanliga textfiler med följande information.

* Ansökningshändelser
* Sessionshändelser
* \<object> deklarationer
* TypeLibrary-deklarationer
* direktivet #include

## Exempel på ASA-fil

En Global.asa-fil kan se ut ungefär så här.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referenser

* [ASP Global.asa-fil - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

