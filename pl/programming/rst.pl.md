{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku RST — plik reStructuredText",
  "description":"Poznaj format pliku RST i interfejsy API, które mogą tworzyć i otwierać pliki RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Czym jest plik RST?

Plik RST to format pliku dokumentacji technicznej, używany głównie w społeczności programistów Pythona. Jest to plik tekstowy napisany w języku znaczników reStructuredText, który stosuje style i formatowanie do zwykłych dokumentów tekstowych w celu generowania dokumentacji. Pliki RST wykorzystują komentarze i inne informacje w kodzie programów Pythona do tworzenia dokumentacji technicznej aplikacji. Mogą one jednak zawierać również tekst, który można przekonwertować na proste strony internetowe i [eBooki](/pl/ebook/). Edytory tekstu, takie jak Github Atom, GNU Emacs (wieloplatformowy), Microsoft Notepad (Windows), Apple TextEdit (Mac) i Vim (Linux) mogą być używane do otwierania plików RST.

## Format pliku RST

Pliki RST zawierają kod napisany w języku znaczników reStructuredText. Jest częścią projektu Docutils firmy Python Doc-SIG (Documentation Special Interest Group), który zapewnia zestaw narzędzi dla Pythona podobnych do Javadoc dla Javy. Parser dla formatu plików RST jest wbudowany w Docutils i może wydobywać informacje z programów Pythona w celu sformatowania ich w dokumentacji programu.

### reStructuredText RST Przykład

Weźmy przykładowy tekst zapisany w formacie pliku RST w następujący sposób.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Gdy ten tekst jest wprowadzany do procesora rST, takiego jak Docutils, dane wyjściowe są następujące.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Odniesienie ##

* [reStructuredText – z Wikipedii](https://en.wikipedia.org/wiki/ReStructuredText)

