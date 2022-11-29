{
  "date" : "2019-10-11",
  "keywords" :[ "pptm-fil", "pptm-filformat", "vad är en pptm-fil", "fil", "pptm-exempel", "pptm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPTM - Macro-Enabled PowerPoint Presentation File Format",
  "description":"Läs mer om PPTM-filformat och API:er som kan skapa och öppna PPTM-filer.",
  "linktitle" : "PPTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

Filer med PPTM-tillägg är makroaktiverade presentationsfiler som skapas med Microsoft PowerPoint 2007 eller högre versioner. De liknar [PPTX](/sv/presentation/pptx/)-filer med skillnaden att den laterala inte kan köra makron även om de kan innehålla makron. PPTM-filer kan redigeras genom att öppna dem i Microsoft PowerPoint och uppdatera innehållet. Ett annat liknande format är PPSM men det är skrivskyddat som standard och startar bildspelet när det öppnas. PPTM, liksom PPTX, innehåller bilder för olika presentationselement som text, bilder, videor, grafer och annat relaterat material.

## Kortfattad bakgrund ##

PPTM-filformatet introducerades 2007 och använder Open XML-standarden anpassad av Microsoft redan 2000. Den nya filtypen har lagt till fördelarna med små filstorlekar, mindre förändringar av korruption och välformaterad bildrepresentation. Det var i början av 2000 när Microsoft bestämde sig för att gå för förändringen för att passa standarden för **Office Open XML**. År 2007 blev detta nya filformat en del av Office 2007 och används även i de nya versionerna av Microsoft Office.

## Filformatspecifikationer ##

Filer genererade med Office Open XML-filformat är en samling XML-filer tillsammans med andra filer som ger länkar mellan alla ingående filer. Denna samling är faktiskt ett komprimerat arkiv som kan extraheras för att se dess innehåll. För att göra det, byt bara namn på PPTM-filtillägget med zip och extrahera det för att observera dess innehåll.

Följande avsnitt kastar lite ljus över var och en av dessa.

### [Content_Types].xml ###

Detta är den enda filen som finns på basnivån när zip-filen extraheras. Den listar innehållstyperna för delar i paketet. Alla referenser till XML-filerna som ingår i paketet hänvisas till i denna XML-fil. Följande är en innehållstyp för en bilddel:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Om nya delar behöver läggas till i paketet kan det göras genom att lägga till den nya delen och uppdatera eventuella relationer i .rels-filerna. Man måste komma ihåg att för en sådan förändring måste Content_Types.xml också uppdateras.

### \_rels (mapp) ###

Relationer mellan de andra delarna och resurser utanför paketet upprätthålls av relationsdelen. Mappen Relationer innehåller en enda XML-fil som lagrar relationerna på paketnivå. Länkar till nyckeldelarna i presentationsfilerna finns i den här filen som URI:er. Dessa URI:er identifierar typen av relation mellan varje nyckeldel och paketet. Detta inkluderar relationen till primära kontorsdokument som finns som ppt/presentation.xml och andra delar inom docProps som kärnegenskaper och utökade egenskaper.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Varje del av dokumentet som är källan till en eller flera relationer kommer att ha sin egen relationsdel där varje sådan relationsdel finns i en \_rels undermapp till delen och namnges genom att lägga till '.rels' till namnet på del. Huvudinnehållsdelen (presentation.xml) har sin egen relationsdel (presentation.xml.rels). Den innehåller relationer till andra delar av innehållet såsom slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, samt URI:erna för externa länkar.

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

