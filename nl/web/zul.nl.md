{
  "date" : "2021-05-24",
  "keywords" :["zul", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "open"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK gebruikersinterfacebestand",
  "description":"Meer informatie over ZUL-bestandsindeling en API's die ZUL-bestanden kunnen maken en openen.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Wat is een ZUL-bestand?

Een bestand met de extensie .zul is een webbestand gemaakt met de User Interface Markup Language (ZUML) en bevat definities voor elementen van de gebruikersinterface. Ajax- en Java-klassen ondersteunen het gebruik van de op [XML](/nl/web/xml/) gebaseerde ZUML voor het ontwikkelen van server-side-bestanden. Het ZUL-bestandsformaat is ontwikkeld door ZK, een UI-framework waarmee u web- en mobiele applicaties kunt bouwen zonder kennis van JavaScript of AJAX.

## ZUL-bestandsindeling

ZUL-bestanden zijn gebaseerd op XML en bestaan uit verschillende elementen om de gebruikersinterface te construeren. De ZK-lader gebruikt elk XML-element om een component te maken. De algehele verwerking van de pagina-elementen zoals paginatitel, beschrijving, enz. wordt beschreven door elke XML-verwerkingsinstructie van ZUML.

### ZUL Voorbeeld

In het volgende voorbeeld van ZUML-code specificeert de eerste regel de paginatitel, de tweede regel maakt een hoofdcomponent met titel en rand en de derde regel maakt een knop met label en een gebeurtenislistener.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Het ZUL-schema kan worden gedownload van https://www.zkoss.org/2005/zul/zul.xsd.
## Referenties

* [ZUL - Door ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL-schema](https://www.zkoss.org/2005/zul/zul.xsd)

