{
  "date" : "2019-10-11",
  "keywords" :[ "potx fil", "potx filformat", "vad är en potx fil", "fil", "potx exempel", "potx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Microsoft PowerPoint-presentationsmall",
  "description":"Lär dig om POTX-filformat och API:er som kan skapa och öppna POTX-filer.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en POTX fil?

Filer med tillägget .POTX representerar Microsoft PowerPoint-mallpresentationer som skapas med Microsoft PowerPoint 2007 och senare. Det här formatet skapades för att ersätta filformatet [POT](/sv/presentation/pot/) som är baserat på det binära filformatet och som stöds av PowerPoint 97-2003. Filerna som genereras kan användas för att skapa presentationer som har samma layout och andra inställningar som krävs för att tillämpas på nya filer. Dessa inställningar kan inkludera stilar, bakgrunder, färgpalett, typsnitt och standardinställningar. Sådana filer genereras för att skapa färdiga mallfiler för officiellt bruk.

## Kortfattad bakgrund ##

Det var i början av 2000 när Microsoft bestämde sig för att gå för förändringen för att passa standarden för **Office Open XML**. Dokument, av olika typer, under denna nya standard identifierades genom att lägga till "X" i deras tillägg, där "X" är för XML. År 2007 blev detta nya filformat en del av Office 2007 och används även i de nya versionerna av Microsoft Office. Den nya filtypen har lagt till fördelarna med små filstorlekar, mindre förändringar av korruption och välformaterad bildrepresentation.

## Filformatspecifikationer ##

Filer genererade med Office Open XML-filformat är en samling XML-filer tillsammans med andra filer som ger länkar mellan alla ingående filer. Denna samling är faktiskt ett komprimerat arkiv som kan extraheras för att se dess innehåll. För att göra det, byt bara namn på POTX-filtillägget med zip och extrahera det för att observera dess innehåll.

Följande avsnitt kastar lite ljus över var och en av dessa.

### [Content_Types].xml ###

Detta är den enda filen som finns på basnivån när zip-filen extraheras. Den listar innehållstyperna för delar i paketet. Alla referenser till XML-filerna som ingår i paketet hänvisas till i denna XML-fil. Följande är en innehållstyp för en bilddel:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Om nya delar behöver läggas till i paketet kan det göras genom att lägga till den nya delen och uppdatera eventuella relationer i .rels-filerna. Man måste komma ihåg att för en sådan förändring måste Content_Types.xml också uppdateras.

### \_rels (mapp) ###

Relationer mellan de andra delarna och resurser utanför paketet upprätthålls av relationsdelen. Mappen Relationer innehåller en enda XML-fil som lagrar relationerna på paketnivå. Länkar till nyckeldelarna av PPTX-filerna finns i den här filen som URI:er. Dessa URI:er identifierar typen av relation mellan varje nyckeldel och paketet. Detta inkluderar relationen till primära kontorsdokument som finns som ppt/presentation.xml och andra delar inom docProps som kärnegenskaper och utökade egenskaper.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Varje del av dokumentet som är källan till en eller flera relationer kommer att ha sin egen relationsdel där varje sådan relationsdel finns i en \_rels undermapp till delen och namnges genom att lägga till '.rels' till namnet på del. Huvudinnehållsdelen (presentation.xml) har sin egen relationsdel (presentation.xml.rels). Den innehåller relationer till andra andra delar av innehållet såsom slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, samt URI:erna för externa länkar.

#### Explicit förhållande ####

För en explicit relation refereras en resurs med Id-attributet för a<Relationship> element. Det vill säga, ID:t i källan mappas direkt till ett ID för ett relationsobjekt, med en explicit referens till målet.

Till exempel kan en bild innehålla en hyperlänk som denna:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" refererar till följande relation inom relationsdelen för bilden (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implicit relation ####

För ett implicit förhållande finns det ingen sådan direkt hänvisning till en `<Relationship> Id`. Istället förstås referensen.

### ppt-mapp ###

Detta är huvudmappen som innehåller all information om innehållet i presentationen. Som standard har den följande mappar:

* \_rels
*tema
* diabilder
* slideLayouts
* slideMasters

och följande xml-filer:

* presentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referenser ##

* [[MS-PPTX] - PPTX-filformat](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

