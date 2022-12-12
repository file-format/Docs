{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru WSDL - soubor jazyka popisu webových služeb",
  "description":"Zjistěte, co je soubor WSDL a rozhraní API, která mohou vytvářet a otevírat soubory WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Co je soubor WSDL?

Soubor WSDL je soubor jazyka popisu webových služeb, který je napsán v jazyce XML pro popis webových služeb. Obsahuje informace o koncových bodech nebo rozhraních pro připojení k vnějšímu světu v všeobecně přijímaném formátu. [Specifikace formátu souboru WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (spravuje W3C.org) definují podmínky pro publikování datových zdrojů pro výměnu dat za účelem vzdálený přístup aplikací přes porty a koncové body.

## Formát souboru WSDL – Další informace

Soubory WSDL se ukládají jako soubory XML, které jsou čitelné pro člověka a lze je otevřít v libovolném textovém editoru a zobrazit obsah.

## Popis služby WSDL

Specifikace formátu souboru WSDL 2.0 popisuje službu WSDL jako službu sestávající ze dvou fází:

- Abstraktní fáze
- Konkrétní jeviště

Opakovaná použitelnost popisu a nezávislých návrhů se řídí webovou službou. Toho je dosaženo pomocí několika různých typů prvků, včetně typů (definice datových typů), zpráv (komunikovaná data), operací (akcí) a protokolů používaných službou. Všechny jsou spravovány na abstraktní úrovni. Vazba podrobností o formátu přenosu a přenosu je specifikována vazbou, která seskupuje koncové body a implementuje společné rozhraní.

### Jaké technologie lze použít pro propojení se službami WSDL?

Pro propojení se službami WSDL lze použít několik různých technologií, včetně aplikací ASP.NET, C/C++ a Java.

## Příklad WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

V tomto příkladu portType "glossaryTerms" definuje jednosměrnou operaci nazvanou "setTerm".

## Reference

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Specifikace formátu souboru WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

