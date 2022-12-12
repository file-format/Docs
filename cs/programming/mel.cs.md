{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language", "soubor", "rozšíření", "formát souboru", "Maya 3D", "Průvodce programováním" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded Language File Format",
  "description":"Další informace o formátu souborů MEL a rozhraních API, která mohou vytvářet a otevírat soubory MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Co je soubor MEL?

Soubor s příponou .mel (Maya Embedded Language) je skriptovací jazyk, který používá Autodesk Maya k vytváření grafických rozhraní. Kromě grafického rozhraní Maya vám umožňuje automatizovat vytváření grafických prvků pomocí spustitelných skriptů. MEL vám umožňuje vytvářet grafická rozhraní, aniž byste se museli učit programovat. Toho je dosaženo vytvářením maker a vlastních akcí, které urychlují opakující se úkoly. Tyto procedury a skripty umožňují vytvářet vlastní modelování, animace, dynamiku a vykreslování úloh. Autodesk Maya 2020 lze použít k otevření a zobrazení obsahu souboru EML.

## Formát souboru MEL - Další informace

Programátorská [referenční příručka](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) je pro vývojáře k dispozici v sekci dokumentace Maya. MEL je založen na skriptovacích příkazech shellu, podobně jako UINX, k dosažení věcí. Příkazy založené na skriptování je činí irelevantními pro konvenční a objektově orientované programování (OOP), což má za následek žádné použití datových struktur, volání funkcí nebo používání OOP jako v jiných jazycích.

Některé klíčové body o MEL jsou následující.

`Komentáře` - Každý příkaz v MEL musí končit středníkem (;), a to i na konci bloku.

`Vracející se hodnoty` - Uvedení výrazu, který vrací hodnotu, automaticky nevytiskne hodnotu v MEL. Místo toho způsobí chybu.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Příkazy pro Create, Edit and Delete` – Stejný příkaz se používá k vytváření věcí, upravování věcí nebo dotazování na informace o existujících věcech. Příznak však řídí, co (vytváření, úpravy nebo dotazování) příkaz dělá.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Vrátit hodnotu z funkce` - Syntaxe funkce automaticky vrátí hodnotu. Chcete-li získat návratovou hodnotu pomocí syntaxe příkazu, musíte příkaz uzavřít do zpětných uvozovek.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Reference

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

