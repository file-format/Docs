{
"datum": "2023-06-08",
  "keywords": [
"soubor hpp",
"co je soubor hpp",
"co obsahuje soubor hpp",
"příklad souboru hpp",
"jaký je formát souboru hpp",
"soubor",
"přípona souboru hpp",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru HPP - soubor záhlaví C++",
  "description":"Další informace o formátu HPP a rozhraních API, která mohou vytvářet a otevírat soubory HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Co je soubor HPP?

Formát souboru ".hpp" se běžně používá pro hlavičkové soubory v programovacím jazyce C++. Soubory záhlaví obvykle obsahují deklarace a definice funkcí, tříd, proměnných a konstant, které jsou používány jinými soubory zdrojového kódu v projektu C++.

Účelem použití hlavičkových souborů je poskytnout způsob, jak sdílet společný kód mezi více soubory zdrojového kódu bez duplikace samotného kódu. Když zdrojový soubor C++ potřebuje získat přístup k deklaracím nebo definicím ze souboru záhlaví, obsahuje soubor záhlaví pomocí direktivy preprocesoru `#include`.

Přípona souboru ".hpp" se často používá k označení, že soubor je soubor záhlaví C++. Použití této specifické přípony pro hlavičkové soubory není podmínkou a můžete narazit i na hlavičkové soubory s příponami „.h“ nebo jinými. Volba rozšíření je do značné míry věcí konvence a osobních preferencí.

Když zdrojový soubor C++ obsahuje soubor záhlaví pomocí `#include`, kompilátor efektivně zkombinuje obsah souboru záhlaví se zdrojovým souborem, než jej zkompiluje jako celek. To umožňuje zdrojovému souboru přístup k deklaracím a definicím v hlavičkovém souboru a poskytuje kompilátoru potřebné informace k provedení kontroly typu a generování kódu.

## Co obsahuje soubor HPP?

Zde jsou některé běžné obsahy, které můžete najít v souboru „.hpp“:

- **Deklarace funkcí:** Soubory záhlaví často obsahují deklarace funkcí bez jejich skutečné implementace. Tyto deklarace poskytují informace o názvu funkce, návratovém typu a parametrech, což umožňuje jiným souborům zdrojového kódu používat funkci, aniž by bylo nutné znát podrobnosti implementace.
- **Deklarace tříd:** Soubory záhlaví mohou obsahovat deklarace tříd, včetně názvu třídy, členských proměnných, členských funkcí a specifikátorů přístupu. Zahrnutím deklarace třídy do souboru záhlaví mohou jiné soubory zdrojového kódu vytvářet objekty této třídy a přistupovat k jejím členům.
- **Deklarace konstant:** Soubory záhlaví mohou definovat konstanty, jako jsou globální proměnné nebo hodnoty enum, které mají být sdíleny mezi více soubory zdrojového kódu. K těmto konstantám lze přistupovat zahrnutím hlavičkového souboru do jiných zdrojových souborů, což jim umožňuje používat definované konstanty.
- **Definice typů:** Soubory záhlaví mohou obsahovat definice typů pomocí klíčového slova "typedef" nebo aliasy typu pomocí klíčového slova "using". Tyto definice vytvářejí nové názvy pro existující typy, díky čemuž je kód čitelnější a lépe udržovatelný.
- **Inline definice funkcí:** V některých případech mohou hlavičkové soubory obsahovat vložené definice funkcí. Inline funkce jsou malé funkce, které jsou rozbaleny na místě volání, spíše než aby byly volány jako samostatná funkce. Zahrnutí inline definice funkce do hlavičkového souboru umožňuje kompilátoru nahradit volání funkce přímo tělem funkce, což potenciálně zvyšuje výkon.

## Příklad souboru HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Jaký je formát souboru HPP?

HPP je prostý textový soubor, ale řídí se obecnými pravidly a syntaxí programovacího jazyka C++. Zde je rozpis obecného formátu a struktury souboru ".hpp":

- **Ochrany záhlaví:** Soubor ".hpp" obvykle začíná ochrannými prvky záhlaví, aby se zabránilo vícenásobnému zahrnutí stejného souboru. Toho je dosaženo pomocí direktiv preprocesoru jako `#ifndef`, `#define` a `#endif`. Ochrana záhlaví zajišťuje, že obsah souboru je zahrnut pouze jednou během procesu kompilace.
- **Include statement:** Po hlavičkových ochranách můžete zahrnout další potřebné hlavičkové soubory pomocí direktivy `#include`. Ty mohou zahrnovat standardní záhlaví knihovny nebo jiná vlastní záhlaví vyžadovaná vaším kódem.
- **Deklarace a definice:** Primárním obsahem souboru ".hpp" jsou deklarace a v některých případech definice tříd, funkcí, konstant, typových aliasů a dalších prvků. Můžete například deklarovat třídy pomocí klíčového slova `class`, funkce pomocí jejich návratového typu, názvu a seznamu parametrů a konstanty pomocí klíčového slova `const` následovaného jejich typem a názvem.
- **Inline definice funkcí:** V určitých případech můžete zahrnout definice inline funkcí přímo do souboru ".hpp". Inline funkce jsou obvykle definovány uvnitř těla třídy, což znamená, že definice funkce je zahrnuta spolu s její deklarací. To lze provést přidáním předdefinování funkce klíčovým slovem `inline`.
- **Deklarace jmenného prostoru:** Pokud ve svém kódu používáte jmenné prostory, můžete je deklarovat v souboru ".hpp". To se provádí pomocí klíčového slova `namespace` následovaného názvem jmenného prostoru a uzavřením příslušného kódu do bloku jmenného prostoru.

## Reference
* [Soubory záhlaví (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

