{
  "date" : "2020-03-16",
  "keywords" :[ "DXF-fil", "Filformat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DXF-filformat och API:er som kan skapa och öppna DXF-filer.",
  "title" :"DXF-filformat",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DXF fil?

DXF, Drawing Interchange Format eller Drawing Exchange Format, är en märkt datarepresentation av AutoCAD-ritningsfil. Varje element i filen har ett prefix heltal som kallas en gruppkod. Denna gruppkod representerar faktiskt elementet som följer och indikerar betydelsen av ett dataelement för en given objekttyp. DXF gör det möjligt att representera nästan all användarspecificerad information i en ritningsfil.

DXF-filformatet utvecklades av Autodesk som CAD-datafilformat för datakompatibilitet mellan AutoCAD och andra applikationer. Således kan data importeras från andra format till DXF till AutoCAD enligt DXF-filformatets interoperabilitetsspecifikationer.

## Kortfattad bakgrund ##


Historien om DXF-filformat går tillbaka till 1982 när det introducerades som en del av AutoCAD 1.0. De ursprungliga versionerna av AutoCAD stöder endast ASCII-filformatet DXF. Med release 10 av AutoCAD (och uppåt) 1988 introducerades stöd för både ASCII och binära DXF-filformat i AutoCAD. I de tidigare stadierna delade Autodesk inga filformatspecifikationer och på grund av detta var korrekt import av DXF-filer inte lätt. Men Autodesk publicerar nu DXF-specifikationerna och är tillgängliga för allmänheten.

## Filformatspecifikationer ##

DXF-filformatet använder gruppkoden och värdeparen för att ordna innehållet i sektioner. Varje sektion är sammansatt av poster där varje post består av en gruppkod och datapost. Varje gruppkod och värde finns på sin egen rad i DXF-filen. Varje avsnitt börjar med en gruppkod 0 följt av strängen, SECTION. Detta följs av en gruppkod 2 och en sträng som anger sektionens namn (till exempel SECTION1). Varje sektion är sammansatt av gruppkoder och värden som definierar dess element. Ett avsnitt slutar med en 0 följt av strängen ENDSEC.

DXF-filformat betraktar objekt som skiljer sig från entiteter. Objekt har ingen grafisk representation här men entiteter har det. Således hänvisas till poster i DXF som grafiska objekt medan objektobjekt hänvisas till som icke-grafiska objekt. Sektionerna BLOCK och ENTITIES i DXF-filen innehåller Entiteter och användningen av gruppkoder i dessa två sektioner är identisk. Slutet på en enhet indikeras av nästa 0-grupp, som börjar nästa enhet eller indikerar slutet på avsnittet.

### Filstruktur ###

Avsnitt i en DXF-fil är ordnade i följande ordning:

|Avsnitt|Grundläggande beskrivning
---|---|
|Header|Det här avsnittet innehåller allmän information om ritningen. Det är som funktionen Inställningar i din telefon, som innehåller de olika variablerna som är kopplade till ritningen och dess tillhörande värden. Till exempel kommer Header-sektionen att definiera vilken AutoCAD-version som DXF-filen använder (variabeln $ACADVER) eller enheten som används för att mäta vinklar i filen (variabeln $AUNITS)
|Klasser|Sektionen KLASSER innehåller informationen för applikationsdefinierade klasser vars instanser visas i sektionerna BLOCKS, ENTITIES och OBJECTS i databasen.
|Tabell|Det här avsnittet innehåller definitioner för flera olika tabeller, som var och en innehåller ett antal olika symbolposter. Till exempel [radtyp](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) definierar mönstret av streck, punkter, text och symboler i DXF-filen och hur de skalas. Här är en komplett lista över tabeller som finns i det här avsnittet:<ul><li> Tabell för applikations-ID (APPID).</li><li> Block Record (BLOCK_RECORD) tabell</li><li> Tabell för dimensionsstil (DIMSTYPE).</li><li> Layer (LAYER) tabell</li><li> Linjetyp (LTYPE) tabell</li><li> Tabell för textstil (STYLE).</li><li> Tabell för användarkoordinatsystem (UCS).</li><li> Visa (VISA) tabell</li><li> Viewport-konfigurationstabell (VPORT).</li></ul>
|Block|Det här avsnittet innehåller de grafiska objekten och ritenheterna som utgör varje blockreferens i ritningen.
|Entiteter|Detta avsnitt innehåller de faktiska objektdata och grafiska enheter i ritningen. Detta kan inkludera rådata – till exempel definieras en cirkelenhet av dess tjocklek, mittpunkt, dess radie och extruderingsriktning.
|Objekt|Här hittar du de icke-grafiska delarna av ritningen. Till exempel lagras AutoCAD-ordböcker här.

## Referenser ##

* [DXF-filspecifikationer](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF av Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

