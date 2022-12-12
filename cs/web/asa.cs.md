{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "formát souboru", "typ souboru", "co je soubor .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - konfigurační soubor ASP",
  "description" :"Zjistěte, co je soubor ASA a rozhraní API, která mohou vytvářet a otevírat soubory ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Co je soubor ASA?

Soubor ASA je konfigurační soubor vytvořený pro projekty [ASP](/cs/web/asp/)/ASP.NET. Obsahuje deklarace proměnných, obsahuje a funkce, které mají být v aplikaci přístupné na globální úrovni. Všechny stránky v projektu mají přístup k těmto proměnným a funkcím, čímž se vyhnete požadavku na jejich přepisování. Jedním takovým příkladem je stránka Global.asa, která je uložena v kořenovém adresáři, aby byla přístupná pro jiné webové stránky ASP. Soubory Global.asa jsou volitelné, ale pokud jsou použity, každá aplikace může mít pouze jeden soubor Global.asa.

## Formát souboru ASA – Další informace

Soubory ASA jsou soubory ve formátu prostého textu s následujícími informacemi.

* Události aplikace
* Události relace
* \<object> prohlášení
* Deklarace TypeLibrary
* direktivu #include

## Příklad souboru ASA

Soubor Global.asa by mohl vypadat nějak takto.

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

## Reference

* [Soubor ASP Global.asa – w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

