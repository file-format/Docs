{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RST Fayl Format - Yenidən Strukturlaşdırılmış Mətn Faylı",
  "description": "RST faylları yarada və aça bilən RST fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-azt"
}
},
  "lastmod": "2022-04-11"
}

## RST faylı nədir?

RST faylı əsasən Python proqramlaşdırma cəmiyyətində istifadə olunan texniki sənəd fayl formatıdır. Bu, sənədlərin yaradılması üçün düz mətn sənədlərinə üslub və format tətbiq edən reStructuredText işarələmə dilində yazılmış mətn faylıdır. RST faylları tətbiqin texniki sənədlərini yaratmaq üçün Python proqram kodundakı şərhlərdən və digər məlumatlardan istifadə edir. Bununla belə, bunlar sadə veb səhifələrə və [eBooks](/ebook/) çevrilə bilən mətni də ehtiva edə bilər. Github Atom, GNU Emacs (cross-platform), Microsoft Notepad (Windows), Apple TextEdit (Mac) və Vim (Linux) kimi mətn redaktorları RST fayllarını açmaq üçün istifadə edilə bilər.

## RST fayl formatı

RST fayllarında reStructuredText işarələmə dilində yazılmış kod var. O, Python üçün Java üçün Javadoc-a bənzər alətlər dəsti təqdim edən Python Doc-SIG (Sənədləşdirmə Xüsusi Maraq Qrupu) Docutils layihəsinin bir hissəsidir. RST fayl foramt üçün analizator Docutils-ə daxil edilmişdir və onları proqram sənədlərinə formatlaşdırmaq üçün Python proqramlarından məlumat çıxara bilər.

### restructuredText RST Nümunəsi

Aşağıdakı kimi RST fayl formatında yazılmış nümunə mətni götürək.

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

Bu mətn Docutils kimi rST prosessoruna daxil edildikdə, çıxış aşağıdakı kimi olur.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## İstinad ##

* [reStructuredText - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/ReStructuredText)


