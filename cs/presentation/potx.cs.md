{
  "date" : "2019-10-11",
  "keywords" :[ "soubor potx", "formát souboru potx", "co je soubor potx", "soubor", "příklad potx", "přípona souboru potx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Šablona prezentace Microsoft PowerPoint",
  "description":"Další informace o formátu souborů POTX a rozhraních API, která mohou vytvářet a otevírat soubory POTX.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor POTX?

Soubory s příponou .POTX představují prezentace šablon Microsoft PowerPoint, které jsou vytvořeny pomocí Microsoft PowerPoint 2007 a vyšší. Tento formát byl vytvořen, aby nahradil formát souboru [POT](/cs/presentation/pot/), který je založen na binárním formátu souboru a je podporován aplikací PowerPoint 97-2003. Vygenerované soubory lze použít k vytvoření prezentací, které mají stejné rozvržení a další nastavení potřebná pro použití na nové soubory. Tato nastavení mohou zahrnovat styly, pozadí, paletu barev, písma a výchozí hodnoty. Tyto soubory jsou generovány za účelem vytvoření souborů šablon připravených k použití pro oficiální použití.

## Stručná historie ##

Bylo to počátkem roku 2000, kdy se Microsoft rozhodl přistoupit ke změně, aby vyhovoval standardu pro **Office Open XML**. Dokumenty různých typů podle tohoto nového standardu byly identifikovány připojením "X" v jejich rozšíření, kde "X" je pro XML. V roce 2007 se tento nový formát souborů stal součástí sady Office 2007 a je používán i v nových verzích sady Microsoft Office. Nový typ souboru přidal výhody malých velikostí souborů, méně změn poškození a dobře formátované reprezentace obrázků.

## Specifikace formátu souboru ##

Soubory generované pomocí Office Open XML file format je kolekce souborů XML spolu s dalšími soubory, které poskytují propojení mezi všemi základními soubory. Tato kolekce je ve skutečnosti komprimovaný archiv, který lze rozbalit a zobrazit jeho obsah. Chcete-li tak učinit, přejmenujte příponu souboru POTX na zip a extrahujte ji, abyste mohli sledovat její obsah.

Následující části osvětlují každý z nich.

### [Content_Types].xml ###

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML. Následuje typ obsahu pro část snímku:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Pokud je třeba do balíčku přidat nové součásti, lze to provést přidáním nové součásti a aktualizací všech vztahů v souborech .rels. Je třeba mít na paměti, že pro takovou změnu je nutné aktualizovat také Content_Types.xml.

### \_rels (složka) ###

Vztahy mezi ostatními částmi a zdroji mimo balíček jsou udržovány částí vztahů. Složka Relationships obsahuje jeden soubor XML, ve kterém jsou uloženy vztahy na úrovni balíčku. Odkazy na klíčové části souborů PPTX jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu kancelářskému dokumentu umístěnému jako ppt/presentation.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.
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

* [[MS-PPTX] – Formát souboru PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)
