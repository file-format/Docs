{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST файлов формат - реструктуриран текстов файл",
  "description":"Научете за файловия формат RST и API, които могат да създават и отварят RST файлове.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Какво е RST файл?

RST файлът е файлов формат с техническа документация, използван предимно в общността за програмиране на Python. Това е текстов файл, написан на езика за маркиране reStructuredText, който прилага стилове и форматиране към документи с обикновен текст за генериране на документация. RST файловете използват коментарите и друга информация в програмния код на Python, за да създадат техническа документация на приложението. Те обаче могат да съдържат и текст, който може да се преобразува в прости уеб страници и [електронни книги](/bg/ebook/). Текстови редактори като Github Atom, GNU Emacs (между платформи), Microsoft Notepad (Windows), Apple TextEdit (Mac) и Vim (Linux) могат да се използват за отваряне на RST файлове.

## RST файлов формат

RST файловете съдържат код, който е написан на език за маркиране reStructuredText. Той е част от проекта Docutils на Python Doc-SIG (Група за специални интереси за документация), който предоставя набор от инструменти за Python, подобни на Javadoc за Java. Анализаторът за RST файлов формат е вграден в Docutils и може да извлича информация от програми на Python за форматирането им в програмна документация.

### RST пример за reStructuredText

Нека вземем примерен текст, написан във файлов формат RST, както следва.

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

Когато този текст се въведе в rST процесор като Docutils, изходът е както следва.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Референция ##

* [reStructuredText - от Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

