{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion Markup Language File",
  "description" :"Zjistěte, co je soubor CFML a rozhraní API, která mohou vytvářet a otevírat soubory CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Co je soubor CFML?

Soubor s příponou .cfml je soubor ColdFusion Markup Language, který se používá k vytvoření webové stránky. Odkazuje na sadu pravidel používaných k definování toho, jak bude programátor vyvíjet aplikaci ColdFusion. ColdFusion je programovací jazyk, který se používá k vytváření serverových webových aplikací rychle as méně než jinými technologiemi, jako je [ASP](/cs/web/asp/), [PHP](/cs/programming/php/) atd. Mezi aplikace, které mohou otevírat soubory CML, patří Adobe ColdFusion 2018, Adobe ColdFusion Builder a Adobe Dreamweaver.

## Formát souboru CFML – Další informace

Soubory CFML jsou soubory značek a obsahují webové prvky ve formě značek. Jedná se o textové soubory, které lze otevřít a upravit v libovolném textovém editoru. Soubory CFML se skládají z několika značek, které jsou podobné [HTML](/cs/web/html/) a obvykle se skládají z úvodní a závěrečné značky. Tyto značky mohou také obsahovat jeden nebo více atributů.

### Syntaxe značek

Následuje zobecněná syntaxe značek CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Většina značek přijímá atributy a jsou definovány následovně.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Některé z těchto značek také přijímají více atributů s následující syntaxí.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Příklad kódu CFML

Zde je příklad, který používá skutečnou značku CFML – značku `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Reference

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

