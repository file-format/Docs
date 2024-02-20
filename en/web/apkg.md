{
  "date": "2019-10-11",
  "keywords": [
    "apkg",
    "apkg file",
    "apkg file format",
    "apkg file type",
    "file",
    "type",
    "What is an APKG file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "APKG - Anki Flashcard Deck File Format",
  "description": "Learn about what is an APKG file and APIs that can create and open them.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apkg"
    }
  },
  "lastmod": "2021-06-16"
}

## What is an APKG file?

A file with .apkg extension is a deck of flashcards generated to be used in [Anki](https://ankiweb.net/about) software application which is a flashcard-based learning program. It contains [HTML](/web/html/) text to be loaded and displayed in Anki application and can additionally have images and sounds for visual and audible learning. Anki allows users to create their own Anki flashcard decks as well as import other user's flashcard decks.

## APKG File Format

Anki card decks are created from templates that are written in HTML, a famous and common language for creating web pages. The styling of deck cards is done using CSS which is the language used for styling web pages. The styling includes modifications to:

 * font-family - The name of the font to be used on the card.
 * font-size - The size of the font in pixels.
 * text-align - Defines whether the text should be aligned in the centre, left, or right.
 * color - Defines the colour of the text which can be simple colour names such as "blue", "red", etc. or HTML colour codes.
 * background-color - Defines the background colour of the card

The styling information is shared among all cards, affecting all cards when a change is made. The following example will use a yellow background on all cards except the first one:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Images resizing in an Anki card can be controlled as follow.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Embedding Javascript in Anki cards

It is possible to embed [Javascript](/web/js/) in an Anki card using the card templates. However, due to the advanced level of Javascript, its support is not provided. Moreover, rendering devices may show the implementation affects of Javascript in the card differently, resulting in the need of testing the implementation on all devices. Certain Javascript features such as window.alert, making it difficult to debug the Javascript code that you have written.

## References ##

* [Anki Documentation](https://docs.ankiweb.net/intro.html)
