{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "fájlformátum", "fájltípus", "mi az .asa fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP konfigurációs fájl",
  "description" :"További információ az ASA-fájlokról és az API-król, amelyek ASA-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Mi az ASA fájl?

Az ASA-fájl az [ASP](/hu/web/asp/)/ASP.NET projektekhez létrehozott konfigurációs fájl. Változódeklarációkat tartalmaz, tartalmaz és függvényeket, amelyek célja, hogy globális szinten elérhetők legyenek az alkalmazásban. A projekt összes oldala hozzáférhet ezekhez a változókhoz és függvényekhez, így elkerülhető az átírásuk. Ilyen például a Global.asa oldal, amely a gyökérkönyvtárban van tárolva, hogy más ASP-weboldalak is elérhessék. A Global.asa fájlok nem kötelezőek, de ha használják, minden alkalmazásnak csak egy Global.asa fájlja lehet.

## ASA fájlformátum – További információ

Az ASA fájlok egyszerű szöveges fájlok a következő információkkal.

* Alkalmazási események
* Session események
* \<object> nyilatkozatok
* TypeLibrary deklarációk
* az #include direktíva

## ASA fájl példa

Egy Global.asa fájl valahogy így nézhet ki.

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

## Hivatkozások

* [ASP Global.asa fájl – w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

