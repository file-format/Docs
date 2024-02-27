{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"apkg fil",
"apkg filformat",
"apkg filtype",
"fil",
"type",
"Hvad er en APKG-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG - Anki Flashcard Deck File Format",
  "description": "Lær om, hvad en APKG-fil og API'er er, der kan oprette og åbne dem.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-dag"
}
},
  "lastmod": "2021-06-16"
}

## Hvad er en APKG fil?

En fil med filtypenavnet .apkg er et sæt flashcards, der er genereret til brug i [Anki](https://ankiweb.net/about)-softwareapplikationen, som er et flashcard-baseret læringsprogram. Den indeholder [HTML](/web/html/) tekst, der skal indlæses og vises i Anki-applikationen og kan desuden have billeder og lyde til visuel og hørbar læring. Anki giver brugerne mulighed for at oprette deres egne Anki flashcard-dæk samt importere andre brugeres flashcard-dæk.

## APKG filformat

Anki kortspil er skabt ud fra skabeloner, der er skrevet i HTML, et berømt og almindeligt sprog til at skabe websider. Styling af kortspil udføres ved hjælp af CSS, som er det sprog, der bruges til styling af websider. Stylingen inkluderer modifikationer til:

 * font-family - Navnet på den skrifttype, der skal bruges på kortet.
 * font-size - Størrelsen af skrifttypen i pixels.
 * tekstjustering - Definerer, om teksten skal justeres i midten, venstre eller højre.
 * farve - Definerer farven på teksten, som kan være simple farvenavne såsom blå, rød osv. eller HTML-farvekoder.
 * baggrundsfarve - Definerer kortets baggrundsfarve

Stilinformationen deles mellem alle kort, hvilket påvirker alle kort, når der foretages en ændring. Følgende eksempel vil bruge en gul baggrund på alle kort undtagen det første:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Billedstørrelser på et Anki-kort kan styres som følger.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Indlejring af Javascript i Anki-kort

Det er muligt at indlejre [Javascript](/web/js/) i et Anki-kort ved hjælp af kortskabelonerne. Men på grund af det avancerede niveau af Javascript ydes dets support ikke. Desuden kan gengivelsesenheder vise implementeringspåvirkningerne af Javascript på kortet anderledes, hvilket resulterer i behovet for at teste implementeringen på alle enheder. Visse Javascript-funktioner såsom window.alert, hvilket gør det vanskeligt at fejlsøge den Javascript-kode, du har skrevet.

## Referencer ##

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

