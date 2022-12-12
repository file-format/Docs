{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "soubor", "rozšíření", "formát souboru", "implementace hta", "Průvodce programováním", "příklad hta", "aplikace HTML", "aplikace jazyka hypertextových značek", "soubory HTA", "Aplikace Microsoft HTML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - HTML aplikační soubory",
  "description":"Další informace o formátu souboru HTA a rozhraních API, která mohou vytvářet a otevírat soubory HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Co je soubor HTA?

HTMLA je zkratka pro **Hypertext Markup Language Application** je program, který je kompatibilní s Microsoft Windows. Zdrojový kód tohoto programu obsahuje více než jeden skriptovací jazyk, jako je [HTML](/cs/web/html/) a [JavaScript](/cs/web/js/). Pro uživatelské rozhraní je preferována HTML aplikace, zatímco pro splnění požadavku programové logiky se používá jakýkoli jiný skriptovací jazyk.

Aplikace HTML je nezávislá na modelu zabezpečení internetového prohlížeče a běží jako plně důvěryhodná aplikace. Přípona použitá pro soubory týkající se těchto aplikací je HTA. Tyto aplikace obsahují vlastnosti HTML spolu s vlastnostmi jiných skriptovacích jazyků.


## Stručná historie ##

HTA byl poprvé představen v roce 1999 společností Microsoft spolu s vydáním Internet Exploreru 5. Byl kompatibilní s Internet Explorerem, a tak mohl být spuštěn pouze na operačním systému Windows. Tato technologie byla patentována v roce 2003. Soubory HTA se spouštějí podobně jako jakékoli jiné soubory .exe. Soubory HTA jsou kompatibilní i s dnešní aktualizovanou verzí Windows 11.


## Technická specifikace ##

HTA mají stejný formát jako jakákoli jiná stránka HTML, z nichž některé se používají pro ovládání stylů okrajů nebo ikon programů. Kromě toho jsou uvedeny argumenty pro spuštění HTA. Tyto aplikace lze spustit pomocí programu s názvem mshta.exe. Lze k němu přistupovat jednoduše dvojitým kliknutím na soubor. Tyto programy se automaticky spouštějí spolu s Internet Explorerem. Kromě jiných specifikací nejsou nezávislé na prohlížeči Trident engine, ale jsou nezávislé na Internet Exploreru. To znamená, že je lze spustit bez použití Internet Exploreru.

Značky se používají za účelem přizpůsobení vzhledu těchto aplikací. Převod z aplikace Microsoft HTML do formátu HTA je jednodušší, tj. stačí změnit příponu. Protože víme, že tyto aplikace jsou plně důvěryhodné, obsahují více funkcí a výhod ve srovnání s jednoduchými soubory HTML. K vytvoření HTA lze použít textové editory. Tyto editory může získat společnost Microsoft nebo jakýkoli jiný důvěryhodný zdroj.


## Příklad formátu souboru HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## reference ##

* [HTA – od Wikipedie](https://en.wikipedia.org/wiki/HTML_Application)



