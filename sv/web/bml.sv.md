{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML-filformat - Bean Markup Language File",
  "description":"Läs mer om BML-filformat och API:er som kan skapa och öppna BML-filer.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Vad är en BML fil?

En fil med tillägget .bml är en Bean Markup Language-fil som lagrar Java-klasser för att stödja Java-appar. Detta ger tillgång till Java-objekt och -metoder och behöver inte skapa ny funktionalitet med hjälp av Java-klasser. Den anger hur komponenterna är kopplade till varandra för att utföra användbara uppgifter. BML utvecklades av IBM alphaWorks för att beskriva strukturer och komponenters relationer. BML-filer kan öppnas och visas med vilken textredigerare som helst som webbläsare, Microsoft Notepad och Notepad++.

## BML filformat

IBM alphaworks webbplats har tillhandahållit två implementeringar av BML. Den första implementeringen är en tolk som "spelar" ett BML-skript för att generera den önskade bönhierarkin. Den andra implementeringen är en kompilator som kompilerar alla BML-skript till reflektionsfri Java-kod. Detta är fördelaktigt i den meningen att det gör det möjligt att fånga applikationens interkomponentstruktur med hjälp av ett språk som är designat för detta specifika ändamål med den extra möjligheten att kompilera den till "vanlig" Java-kod.

## BML-taggar

Följande är en förklaring av några av taggarna som används i BML-språket:

### Den<bean> märka:

De<bean> element används för att skapa nya bönor eller för att slå upp bönor efter namn. De<bean> taggen har formatet:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
"ID" i taggen är associerat med objektregistret för JavaBean.

### Den<string> märka

Det finns två sätt att använda strängtaggen:

1. Så här skapar du en icke-tom sträng:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Så här skapar du en tom sträng:

```
<string/>
```
## Referenser

* [Objektorienterad meddelandehantering med XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)


