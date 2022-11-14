{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML-bestandsindeling - Bean Markup Language-bestand",
  "description":"Meer informatie over BML-bestandsindeling en API's die BML-bestanden kunnen maken en openen.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Wat is een BML-bestand?

Een bestand met de extensie .bml is een Bean Markup Language-bestand dat Java-klassen opslaat ter ondersteuning van Java-apps. Dit geeft toegang tot Java-objecten en -methoden en hoeft geen nieuwe functionaliteit te creëren met behulp van Java-klassen. Het specificeert hoe de componenten met elkaar zijn verbonden voor het uitvoeren van nuttige taken. BML is ontwikkeld door IBM alphaWorks om de relaties tussen structuren en componenten te beschrijven. BML-bestanden kunnen worden geopend en bekeken met elke teksteditor, zoals webbrowsers, Microsoft Notepad en Notepad++.

## BML-bestandsindeling

De IBM alphaworks-website heeft twee implementaties van BML opgeleverd. De eerste implementatie is een interpreter die een BML-script 'afspeelt' om de gewenste bonenhiërarchie te genereren. De tweede implementatie is een compiler die elk BML-script compileert tot reflectievrije Java-code. Dit is voordelig in die zin dat het de mogelijkheid biedt om de structuur tussen componenten van de applicatie vast te leggen met behulp van een taal die voor dit specifieke doel is ontworpen, met de toegevoegde mogelijkheid om deze in 'gewone' Java-code te compileren.

## BML-tags

Hieronder volgt een uitleg van enkele van de tags die in de BML-taal worden gebruikt:

### De<bean> label:

De<bean> element wordt gebruikt om nieuwe bonen te maken of om bonen op naam op te zoeken. De<bean> tag heeft het formaat:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
De "id" in de tag is gekoppeld aan het objectregister voor de JavaBean.

### De<string> label

Er zijn twee manieren waarop de string-tag kan worden gebruikt:

1. Een niet-lege tekenreeks maken:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Om een lege string aan te maken:

```
<string/>
```
## Referenties

* [Object-Oriented Messaging met XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [De fysieke opmaaktaal](http://web.mit.edu/mecheng/pml/standards.htm)
* [The Bean Markup Language](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

