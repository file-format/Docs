{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу RST - файл reStructuredText",
  "description":"Дізнайтеся про формат файлу RST та API, які можуть створювати та відкривати файли RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Що таке файл RST?

Файл RST — це формат файлу технічної документації, який використовується в основному в спільноті програмістів Python. Це текстовий файл, написаний мовою розмітки reStructuredText, який застосовує стилі та форматування до простих текстових документів для створення документації. Файли RST використовують коментарі та іншу інформацію в програмному коді Python для створення технічної документації програми. Однак вони також можуть містити текст, який можна перетворити на прості веб-сторінки та [електронні книги](/uk/ebook/). Для відкриття файлів RST можна використовувати такі текстові редактори, як Github Atom, GNU Emacs (кросплатформний), Microsoft Notepad (Windows), Apple TextEdit (Mac) і Vim (Linux).

## Формат файлу RST

Файли RST містять код, написаний мовою розмітки reStructuredText. Це частина проекту Docutils Python Doc-SIG (Documentation Special Interest Group), який надає набір інструментів для Python, подібний до Javadoc для Java. Синтаксичний аналізатор формату файлів RST вбудовано в Docutils і може отримувати інформацію з програм Python для форматування їх у програмну документацію.

### Приклад RST reStructuredText

Розглянемо приклад тексту, написаного у форматі файлу RST, як показано нижче.

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

Коли цей текст вводиться в процесор rST, наприклад Docutils, виводиться наступний вигляд.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Посилання ##

* [reStructuredText - Вікіпедія](https://en.wikipedia.org/wiki/ReStructuredText)

