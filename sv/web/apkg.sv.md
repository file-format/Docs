{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg-fil", "apkg-filformat", "apkg-filtyp", "fil", "typ", "Vad är en APKG-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck File Format",
  "description" :"Läs mer om vad som är en APKG-fil och API:er som kan skapa och öppna dem.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Vad är en APKG fil?

En fil med filtillägget .apkg är en kortlek som genereras för att användas i programvaran [Anki](https://ankiweb.net/about), som är ett flashkortbaserat lärandeprogram. Den innehåller [HTML](/sv/web/html/) text som ska laddas och visas i Anki-applikationen och kan dessutom ha bilder och ljud för visuell och hörbar inlärning. Anki tillåter användare att skapa sina egna Anki flashcard kortlekar samt importera andra användares flashcard kortlekar.

## APKG-filformat

Anki-kortlekar skapas av mallar som är skrivna i HTML, ett känt och vanligt språk för att skapa webbsidor. Styling av kortlek görs med CSS som är språket som används för styling av webbsidor. Stylingen inkluderar modifieringar av:

* font-family - Namnet på teckensnittet som ska användas på kortet.
* font-size - Teckensnittets storlek i pixlar.
* text-align - Definierar om texten ska justeras i mitten, vänster eller höger.
* färg - Definierar färgen på texten som kan vara enkla färgnamn som "blå", "röd" etc. eller HTML-färgkoder.
* bakgrundsfärg - Definierar bakgrundsfärgen på kortet

Stylinginformationen delas mellan alla kort, vilket påverkar alla kort när en ändring görs. Följande exempel kommer att använda en gul bakgrund på alla kort utom det första:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Bildstorleksändring i ett Anki-kort kan styras enligt följande.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Inbädda Javascript i Anki-kort

Det är möjligt att bädda in [Javascript](/sv/web/js/) i ett Anki-kort med hjälp av kortmallarna. Men på grund av den avancerade nivån av Javascript tillhandahålls inte dess stöd. Dessutom kan renderingsenheter visa implementeringseffekterna av Javascript på kortet på olika sätt, vilket resulterar i ett behov av att testa implementeringen på alla enheter. Vissa Javascript-funktioner som window.alert, vilket gör det svårt att felsöka Javascript-koden som du har skrivit.

## Referenser ##

* [Anki-dokumentation](https://docs.ankiweb.net/intro.html)

