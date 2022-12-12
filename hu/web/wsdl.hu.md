{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL fájlformátum – webszolgáltatást leíró nyelvi fájl",
  "description":"További információ arról, hogy mi az a WSDL-fájl és az API-k, amelyek WSDL-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Mi az a WSDL fájl?

A WSDL-fájl a webszolgáltatások leírására szolgáló nyelvi fájl, amely XML nyelven íródott a webszolgáltatások leírására. Általánosan elfogadott formátumban tartalmaz információkat a külvilággal való kapcsolódás végpontjairól vagy interfészeiről. [WSDL-fájlformátum-specifikációk](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (a W3C.org által karbantartott) meghatározza az adatfolyamok közzétételének feltételeit az adatcseréhez. távoli alkalmazás-hozzáférés portokon és végpontokon keresztül.

## WSDL fájlformátum - További információ

A WSDL-fájlok XML-fájlokként kerülnek mentésre, amelyek ember által olvashatók, és bármely szövegszerkesztőben megnyithatók a tartalom megtekintéséhez.

## WSDL szolgáltatás leírása

A WSDL 2.0 fájlformátum specifikációi szerint a WSDL szolgáltatás két szakaszból áll:

- Absztrakt színpad
- Konkrét színpad

A leírás és a független konszerntervek újrafelhasználhatóságát egy webszolgáltatás szabályozza. Ez több különböző típusú elem használatával érhető el, beleértve a típusokat (adattípus-definíciók), az üzeneteket (a közölt adatok), a műveleteket (műveleteket) és a szolgáltatás által használt protokollokat. Ezeket mind absztrakt szinten kezelik. A szállítási és vezetékes formátum részleteinek összerendelését az összerendelés határozza meg, amely a végpontokat csoportosítja egy közös interfész megvalósításához.

### Milyen technológiák használhatók a WSDL szolgáltatásokkal való interfészhez?

Számos különböző technológia használható a WSDL szolgáltatásokkal való interfészhez, beleértve az ASP.NET, C/C++ és Java alkalmazásokat.

## WSDL példa

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

Ebben a példában a portType "glossaryTerms" egy "setTerm" nevű egyirányú műveletet határoz meg.

## Hivatkozások

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL fájlformátum specifikációi](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

