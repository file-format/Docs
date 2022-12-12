{
  "date" : "2019-10-11",
  "keywords" :[ "soubor ppsm", "formát souboru ppsm", "co je soubor ppsm", "soubor", "příklad ppsm", "přípona souboru ppsm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - PowerPoint Presentation File s podporou maker",
  "description":"Další informace o formátu souboru PPSM a rozhraních API, která mohou vytvářet a otevírat soubory PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PPSM?

Soubory s příponou PPSM představují formát souboru prezentace s podporou maker vytvořený pomocí aplikace Microsoft PowerPoint 2007 nebo vyšší. Dalším podobným formátem souboru je [PPTM](/cs/presentation/pptm/), který se liší otevřením v aplikaci Microsoft PowerPoint v upravitelném formátu namísto spuštění jako prezentace. Při spuštění jako prezentace soubor PPSM zobrazuje snímky prezentace s nedotčeným obsahem v prezentaci a ve výchozím nastavení je v režimu pouze pro čtení. Soubory PPSM lze stále upravovat v aplikaci Microsoft PowerPoint otevřením v aplikaci PowerPoint.

## Formát souboru ##

Formát souboru PPSM byl zaveden s aplikací PowerPoint 2007 a je založen na formátu souboru OpenXML, který k ukládání obsahu používá kombinaci XML a [ZIP](/cs/compression/zip/). Soubory generované pomocí Office Open XML file format je kolekce souborů XML spolu s dalšími soubory, které poskytují propojení mezi všemi základními soubory. Tato kolekce je ve skutečnosti komprimovaný archiv, který lze rozbalit a zobrazit jeho obsah. Chcete-li tak učinit, přejmenujte příponu souboru PPSM na zip a extrahujte ji, abyste mohli sledovat její obsah.

Následující části osvětlují každý z nich.

### [Content_Types].xml ###

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML. Následuje typ obsahu pro část snímku:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Pokud je třeba do balíčku přidat nové součásti, lze to provést přidáním nové součásti a aktualizací všech vztahů v souborech .rels. Je třeba mít na paměti, že pro takovou změnu je nutné aktualizovat také Content_Types.xml.

### \_rels (složka) ###

Vztahy mezi ostatními částmi a zdroji mimo balíček jsou udržovány částí vztahů. Složka Relationships obsahuje jeden soubor XML, ve kterém jsou uloženy vztahy na úrovni balíčku. Odkazy na klíčové části souborů prezentace jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu kancelářskému dokumentu umístěnému jako ppt/presentation.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Každá část dokumentu, která je zdrojem jednoho nebo více vztahů, bude mít svou vlastní část vztahů, kde se každá taková část vztahu nachází v podsložce \_rels části a je pojmenována připojením '.rels' k názvu části část. Hlavní obsahová část (presentation.xml) má svou vlastní část týkající se vztahů (presentation.xml.rels). Obsahuje vztahy s jinými částmi obsahu, jako jsou slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, a také identifikátory URI pro externí odkazy.

#### Explicitní vztah ####

Pro explicitní vztah je zdroj odkazován pomocí atributu Id z a<Relationship> živel. To znamená, že ID ve zdroji se mapuje přímo na ID položky vztahu s explicitním odkazem na cíl.

Snímek může například obsahovat hypertextový odkaz, jako je tento:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" odkazuje na následující vztah v části vztahů pro snímek (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implicitní vztah ####

Pro implicitní vztah neexistuje žádný takový přímý odkaz na `<Relationship> Id'. Místo toho je odkaz chápán.

### Složka ppt ###

Toto je hlavní složka, která obsahuje všechny podrobnosti o obsahu prezentace. Ve výchozím nastavení má následující složky:

* \_rels
* téma
* diapozitivy
* rozvržení snímků
* slideMasters

a následující xml soubory:

* prezentace.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Reference ##

* [Formát souboru prezentace OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

