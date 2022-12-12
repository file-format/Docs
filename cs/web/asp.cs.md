{
  "date" : "2019-10-11",
  "keywords" :[ "asp","soubor ASP", "formát souboru ASP", "typ souboru ASP", "soubor", "typ", "co je soubor asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - formát souboru Active Server Pages",
  "description" :"Zjistěte, co je soubor ASP a rozhraní API, která je mohou vytvářet a otevírat.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ASP?

ASP je zkratka pro Active Server Pages, což je vývojový rámec pro vytváření webových stránek. Umožňuje spouštění počítačového kódu interním serverem pro obsluhu webových požadavků. Když je webovým prohlížečem vygenerován požadavek na soubor ASP, server soubor přečte a spustí jakýkoli kód/skript v něm, aby vygeneroval výsledek **[HTML](/cs/web/html/)**, který se vrátí prohlížeč pro zobrazení.

Na rozdíl od stránek HTML, které jsou statickými stránkami obsluhovanými serverem, generují soubory ASP za běhu dynamický obsah, který může zahrnovat požadavky na data z databáze. Stránky ASP obvykle používají příponu ASP spíše než .html. Vzhledem k tomu, že kód/skript v souboru ASP se spouští na straně serveru, žádající prohlížeč nevidí kód použitý k vytvoření obsluhované stránky. Všechny moderní prohlížeče jsou schopny zobrazit stránky, které jsou výsledkem toho. Stránky vytvořené pomocí technologie ASP jsou postaveny na technologii společnosti Microsoft a jsou hostovány na serverech Internetové informační služby (IIS) společnosti Microsoft.

## Stručná historie formátu souborů ASP
ASP prošlo jen několika revizemi, ale bylo nahrazeno ASP.NET, což je modernější a efektivnější způsob vývoje a správy stránek na straně serveru. Podpora pro ASP je standardně zahrnuta spolu s Internetovou informační službou (IIS). ASP bylo publikováno ve třech různých verzích s vylepšeními v každé z nich.

* ASP 1.0 byla vydána v prosinci 1996 jako součást IIS 3.0
* ASP 2.0 bylo vydáno v září 1997 jako součást IIS 4.0
* ASP 3.0 bylo vydáno v listopadu 2000 jako součást IIS 5.0

## Funkční objekty ASP

Soubory ASP používají objekty na straně serveru ke zpracování požadavků uživatelů a generování výstupních stránek, které mají být poskytovány uživatelům. Každý objekt má sadu kolekcí, vlastností a metod pro zpracování požadavků a odpovědí. Mezi tyto objekty patří:

### Objekt požadavku

Když prohlížeč požádá o stránku ze serveru, nazývá se to požadavek. Objekt Request slouží k získání informací od návštěvníka.

### Objekt odpovědi

Objekt ASP Response se používá k odeslání výstupu uživateli ze serveru.

### Objekt serveru

Objekt ASP Server se používá pro přístup k vlastnostem a metodám na serveru. Umožňuje připojení k databázím (ADO), souborovému systému a použití komponent nainstalovaných na serveru.

### Objekt relace

Objekt relace je jako spojení mezi prohlížečem uživatele požadujícím stránku ze serveru a serverem samotným. Toho je dosaženo pomocí cookie vytvořené ASP a zaslané do počítače uživatele. Objekt Session ukládá informace o uživatelské relaci nebo mění nastavení pro ni. Informace uložené v objektu Session jsou sdíleny na všech stránkách aplikace. Běžné informace uložené v proměnných relace jsou název, id a preference. Server vytvoří nový objekt Session pro každého nového uživatele a zničí objekt Session, když relace vyprší.

### Objekt aplikace

Objekt Application obsahuje informace, které budou použity mnoha stránkami v aplikaci (jako jsou informace o připojení k databázi). Informace jsou přístupné z jakékoli stránky. Informace lze také změnit na jednom místě a změny se automaticky projeví na všech stránkách. Objekt Application se používá k ukládání a přístupu k proměnným z libovolné stránky, stejně jako objekt Session.

### Objekt ASPERror

Objekt ASPError byl implementován v ASP 3.0 a je dostupný v IIS5 a novějších. Objekt ASPError se používá k zobrazení podrobných informací o jakékoli chybě, která se vyskytuje ve skriptech na stránce ASP.

**Poznámka:** Objekt ASPError je vytvořen při volání Server.GetLastError, takže k informacím o chybě lze přistupovat pouze pomocí metody Server.GetLastError.

## Reference

* [ASP – od W3C](https://www.w3schools.com/asp/default.asp)
* [Vytváření jednoduchých stránek ASP](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

