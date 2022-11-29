{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Fil", "Extension", "Filformat", "Filtillägg", "extensible html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Extensible Hypertext Markup Language File Format",
  "description":"Läs mer om vad som är XHTML-filformat och API:er som kan skapa och öppna XHTML-filer.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en XHTML-fil?

XHTML är ett textbaserat filformat med markering i XML, med en omformulering av HTML 4.0. Dessa filer är väl lämpade att öppna eller visa i en webbläsare. XHTML designades för att vara mer strukturerad, mindre skript, generisk; använder alla befintliga möjligheter för XML och mer enhetsoberoende. XHTML tillhandahåller en allmänt värdefull uppsättning element och attribut, med tilläggsalternativ i kombination med stilmallar. Attributen används från insamlingen av metadataattribut. XHTML ger flexibilitet och tillgänglighet genom att underordna alla **[HTML](/sv/web/html/)** presentationselement till stilmallar. Stilmallar är mer mångsidiga än dessa presentationselement. Specifikationer för HTML 4.01, HTML5 och XHTML utvecklas dynamiskt av World Wide Web Consortium (W3C).

## Kort historia av XHTML-filformat

Historien om XHTML börjar med ett utkast till dokument som släpptes i december 1998 av World Wide Web Consortium. Detta dokument hänvisar till "Omformulera HTML i XML", en specifikation som kallas XHTML 1.0. Denna nya specifikation omformulerade HTML i XML med hjälp av befintliga element eller attribut. I maj 1999 deklarerade W3 Consortium att HTML 4.0 hade omformats som en XML-applikation. dvs XHTML. Den 26 januari 2000 släpptes den första specifikationen som definierar XHTML 1.0 av W3C. Den 31 maj 2001 tillkännagav W3C XHTML som ett oberoende språk och började arbeta med utveckling av HTML 5.0. Men 2005 bildades en arbetsgrupp (WHATWG) som syftade till att förbättra vanlig HTML oberoende av XHTML. WHATWG började så småningom arbeta med HTML5 parallellt med XHTML 2.

## XHTML filformat

XHTML är ett format, som är en samling av olika dokumenttyper och moduler som efterliknar, kategoriserar och utökar HTML 4. Filerna i XHTML är XML-baserade och syftar till att arbeta med användaragenterna baserade på XML. XHTML-filer är XML-kompatibla. Standard XML-verktyg används för att visa, redigera och validera XHTML-filer. HTML Document Object Model eller XML Document Object Model [DOM] beroende applikationer kan fungera genom XHTML-dokument. Genom att välja XHTML idag kan innehållsutvecklare njuta av alla associerade fördelar med XML utan att behöva oroa sig för deras innehålls framåt- eller bakåtkompatibilitet.

En uppsättning relaterade element bygger en modul i XHTML. En formulär- eller tabellmodul kan innehålla olika formulär- eller tabellelement som kan visas på en webbsida. Modulariseringen syftade till att isolera HTML-element till uppsättningar av många länkade element. Så att innehållsutvecklare kan dra fördel av modulval för olika typer av enheter. Dessutom tillåter moduler användaragenter att välja element utan att förlora överensstämmelse med XHTML-standarden. Parsningskraven för XHTML är samma som XML medan HTML praktiserar sina egna.

### Dokumentöverensstämmelse

XHTML2 erbjuder specifikationer som överensstämmer med XHTML 1.0-dokument, som använder namnutrymmeselement och attribut från XML och XHTML 1.0. Dokumentöverensstämmelse är av två typer.

Ett strikt överensstämmande dokument är XML-baserat som endast behöver obligatoriska tjänster definierade i denna specifikation. Följande kriterier måste uppfyllas för XHTML-filer:

* En fil måste överensstämma med de begränsningar som definieras i DTD:er och i bilaga B.
* Filens baselement måste vara html.
* Filens baselement måste innehålla deklaration för XHTML-namnutrymmet och bör definieras som:

```
http://www.w3.org/1999/xhtml.
```

* Baselementet kan skrivas som:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Tidigare än baselementet måste en DOCTYPE deklareras, vars offentliga identifierare måste referera till en av de tre dokumenttypsdefinitionerna (DTD). Systemidentifieraren kan modifieras för att följa de nuvarande systemkonventionerna.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

I XML-dokument är det onödigt att ange XML-deklarationer i alla dokument; innehållsutvecklare lockas dock att använda XML-deklarationer i alla sina XHTML-dokument. Dessa deklarationer är obligatoriska antingen när teckenkodningen för dokumentet skiljer sig från UTF-8 /16 eller när ingen kodning specificerades av ett styrande protokoll. Följande exempel på ett XHTML-dokument definierar XML-deklarationerna

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

En överensstämmande användaragent måste uppfylla följande regler:

* Parsning och utvärdering av XHTML-dokument görs av en användaragent som säkerställer dess överensstämmelse med XML 1.0-rekommendationen.
* Vid validering av användaragent måste den kontrollera dokumentens giltighet för deras refererade DTD:er enligt XML. När XHTML-filen behandlas av användaragenten som generisk XML, kommer funktionerna i typ-ID att erkännas som fragmentidentifierare.

Om en användaragent stöter på ett okänt element, följer följande de obligatoriska kriterierna som den måste uppfylla

* bearbeta innehållet i det okända elementet
* ignorera attributet och dess värde
* Använd värdet på det angivna attributet som standard.

När användaragenten stöter på att en enhetsreferensdeklaration inte har behandlats tidigare bör den behandlas som tecknen (börjar med "&"-tecknet och slutar med semikolon). Under innehållsbehandling kan tecken eller teckenenhetsreferenser som är förutsägbara av användaragenten men inte renderbara använda valfri alternativ rendering som ger liknande betydelse. I sådana fall måste dokumentet visas på ett sätt som gör användaren uppenbar om att återgivningsprocessen inte har varit normal. För bearbetning av blanksteg måste användaragenten se definitionen från CSS-tecken [CSS2].

## XHTML bakåtkompatibilitet

Den bakåtriktade kompatibiliteten för XHTML 1.-dokument är väl bevandrad med HTML 4-användaragenter, om de rätta reglerna följs. XHTML 1.1 är helt kompatibel förutom ruby-anteckningar, även om de i allmänhet ignoreras av HTML 4-webbläsarna. XHTML 2.0 är jämförelsevis mindre kompatibel, men problemet har till viss del åtgärdats genom användning av skript.

## Referenser

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

