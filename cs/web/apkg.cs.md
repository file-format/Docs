{
  "date" : "2019-10-11",
   "keywords" :[ "apkg", "soubor apkg", "formát souboru apkg", "typ souboru apkg", "soubor", "typ", "Co je soubor APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Formát souboru Anki Flashcard Deck",
  "description" :"Zjistěte, co je soubor APKG a rozhraní API, která je mohou vytvářet a otevírat.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Co je soubor APKG?

Soubor s příponou .apkg je balíček karet vygenerovaných pro použití v softwarové aplikaci [Anki](https://ankiweb.net/about), která je výukovým programem založeným na kartách. Obsahuje [HTML](/cs/web/html/) text k načtení a zobrazení v aplikaci Anki a může mít navíc obrázky a zvuky pro vizuální a zvukové učení. Anki umožňuje uživatelům vytvářet vlastní balíčky karet Anki a také importovat balíčky karet jiných uživatelů.

## Formát souboru APKG

Balíčky karet Anki jsou vytvořeny ze šablon, které jsou napsány v HTML, což je známý a běžný jazyk pro vytváření webových stránek. Stylování karet se provádí pomocí CSS, což je jazyk používaný pro stylování webových stránek. Styling zahrnuje úpravy:

* font-family - Název fontu, který má být použit na kartě.
* font-size - Velikost písma v pixelech.
* text-align - Definuje, zda má být text zarovnán na střed, doleva nebo doprava.
* barva - Definuje barvu textu, což mohou být jednoduché názvy barev jako "modrá", "červená" atd. nebo kódy barev HTML.
* background-color - Definuje barvu pozadí karty

Informace o stylu jsou sdíleny mezi všemi kartami a při provedení změny ovlivní všechny karty. Následující příklad použije žluté pozadí na všech kartách kromě první:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Změna velikosti obrázků na kartě Anki lze ovládat následovně.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Vložení Javascriptu do karet Anki

Je možné vložit [Javascript](/cs/web/js/) do karty Anki pomocí šablon karet. Vzhledem k pokročilé úrovni Javascriptu však není poskytována jeho podpora. Navíc vykreslovací zařízení mohou vykazovat dopady implementace Javascriptu na kartě odlišně, což má za následek nutnost otestovat implementaci na všech zařízeních. Některé funkce Javascriptu, jako je window.alert, ztěžují ladění kódu Javascript, který jste napsali.

## Reference ##

* [Dokumentace Anki](https://docs.ankiweb.net/intro.html)

