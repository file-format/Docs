{
  "date" : "2019-12-13",
  "keywords" :[ "soubor pptx", "formát souboru pptx", "co je soubor pptx", "soubor", "příklad pptx", "přípona souboru pptx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru PPTX a rozhraních API, která mohou vytvářet a otevírat soubory PPTX.",
  "title" :"PPTX - formát souboru prezentace PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PPTX?

Soubory s příponou PPTX jsou prezentační soubory vytvořené pomocí oblíbené aplikace Microsoft PowerPoint. Na rozdíl od předchozí verze formátu prezentačních souborů PPT, která byla binární, je formát PPTX založen na formátu otevřeného prezentačního souboru Microsoft PowerPoint XML. Soubor prezentace je kolekce snímků, kde každý snímek může obsahovat text, obrázky, formátování, animace a další média. Tyto snímky jsou publiku prezentovány ve formě prezentací s vlastním nastavením prezentace.

## Stručná historie

Formát souboru PPTX byl představen v roce 2007 a používá standard Open XML upravený společností Microsoft již v roce 2000. Před PPTX byl běžným formátem souborů PPT, což byl čistě binární formát souboru. Nový typ souboru přidal výhody malých velikostí souborů, méně změn poškození a dobře formátované reprezentace obrázků. Bylo to počátkem roku 2000, kdy se Microsoft rozhodl přistoupit ke změně, aby vyhovoval standardu pro **Office Open XML**. V roce 2007 se tento nový formát souborů stal součástí sady Office 2007 a je používán i v nových verzích sady Microsoft Office.

## Specifikace formátu souboru PPTX

Soubory generované pomocí Office Open XML file format je kolekce souborů XML spolu s dalšími soubory, které poskytují propojení mezi všemi základními soubory. Tato kolekce je ve skutečnosti komprimovaný archiv, který lze rozbalit a zobrazit jeho obsah. Chcete-li tak učinit, přejmenujte příponu souboru PPTX na zip a rozbalte ji, abyste si mohli prohlédnout její obsah (viz [Specifikace formátu souboru PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) od společnosti Microsoft).

Následující části osvětlují každý z nich.

### [Content_Types].xml

Toto je jediný soubor, který je po extrahování zipu nalezen na základní úrovni. Uvádí typy obsahu součástí v balíčku. Všechny odkazy na soubory XML obsažené v balíčku jsou uvedeny v tomto souboru XML. Následuje typ obsahu pro část snímku:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Pokud je třeba do balíčku přidat nové součásti, lze to provést přidáním nové součásti a aktualizací všech vztahů v souborech .rels. Je třeba mít na paměti, že pro takovou změnu je nutné aktualizovat také Content_Types.xml.

### \_rels (složka) ###

Vztahy mezi ostatními částmi a zdroji mimo balíček jsou udržovány částí vztahů. Složka Relationships obsahuje jeden soubor XML, který ukládá vztahy na úrovni balíčku. Odkazy na klíčové části souborů PPTX jsou obsaženy v tomto souboru jako URI. Tyto URI identifikují typ vztahu každé klíčové části k balíčku. To zahrnuje vztah k primárnímu kancelářskému dokumentu umístěnému jako ppt/presentation.xml a dalším částem v rámci docProps jako základním a rozšířeným vlastnostem.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Implicitní vztah ####

Pro implicitní vztah neexistuje žádný takový přímý odkaz na `<Relationship> Id'. Místo toho je odkaz chápán.

### ppt Folder ###


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

* [[MS-PPTX] – Formát souboru PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

