{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "soubor DML", "formát souboru DML", "typ souboru DML", "soubor", "typ", "co je soubor DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - soubor HTML DynaScript",
  "description":"Další informace o formátu souborů DML a rozhraních API, která mohou vytvářet a otevírat soubory DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Co je soubor DML?

Soubor s příponou .dml je soubor kódu stránky webového skriptu vytvořený pomocí jazyka DyanScript. DynaScript je dynamický [HTML](/cs/web/html/) skriptovací jazyk, který je kompatibilní s ECMAScriptem a poskytuje většinu stejných funkcí jako ostatní skriptovací jazyk. Je podobný kódu ColdFusion a kódu Microsoft Active Server Pages (ASP). Soubory DML lze otevírat a prohlížet ve standardních webových prohlížečích podobně jako jiné stránky HTML.

## Formát souboru DML

Soubory DML jsou vytvářeny ve formátu prostého textu a lze je otevřít pomocí textového editoru a zobrazit kód. Psaní kódu pomocí skriptovacího jazyka DML lze použít k dynamickému generování HTML na stránkách DML hostovaných na straně serveru. DynaScripty jsou sestaveny z následujících jazykových prvků:


* Tag SCRIPT – Jsou vkládány do dokumentů jako HTML komentáře. Komentář HTML je označen znakem \ <!-- tag.
* Literály – Toto jsou pevné hodnoty v souborech DynaScript. Příklady zahrnují celá čísla, jako je s 123 , 0x3F , 0123, čísla s plovoucí desetinnou čárkou, jako je 456,789 , 3,2e-8, logická hodnota, jako je pravda nebo nepravda, a řetězec jako „Déšť ve Španělsku“
* Proměnné - Proměnné DynaScriptu nemusí být definovány ani je přiřazovat k pevnému datovému typu. Proměnná musí mít hodnotu, než ji použijete ve výrazu; jinak se vygeneruje varování za běhu.
* Výrazy – Jedná se o kombinace proměnných, doslovných hodnot, operátorů a dalších výrazů. Pravá strana příkazu přiřazení je výraz.
* Operátory – pracují s jedním nebo více výrazy nazývanými operandy. Ty mohou být buď ternární, binární nebo unární: ternární operátory působí na tři výrazy, binární operátory působí na dva výrazy a unární operátory působí na jeden.
* Příkazy – řídí tok skriptů, manipulují s objekty a obecné programování. Obecně platí, že tato prohlášení se řídí standardní syntaxí C a Java. Příklady jsou if-else, smyčky do-while, přepínání, přerušení, pokračování atd. jako jakýkoli jiný skriptovací jazyk.
* Funkce – Funkce, stejně jako jakýkoli jiný skriptovací jazyk, vám umožňují zapouzdřit sadu instrukcí jednou v dokumentu jako funkci a poté ji použít několikrát v celém dokumentu (voláním funkce). DynaScript také podporuje funkce.
* Objekty – DynaScript je objektově orientovaný a podporuje „objekty“ a základní objektově orientované koncepty zapouzdření, polymorfismu a dědičnosti.

