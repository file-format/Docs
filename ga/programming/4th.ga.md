
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4ú Comhad - Forth Language File Formáid",
  "description":"Foghlaim faoi cad é formáid comhaid .4th le sampla agus APIs ar féidir leo 4ú comhad a chruthú agus a oscailt.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Cad is 4ú comhad ann?

Is comhad ríomhchláraithe é comhad a bhfuil .4ú síneadh comhad aige a cruthaíodh don **Forth Programming Language**. Tá cód foinse ann do chláir atá scríofa i dteanga ríomhchlárúcháin Forth agus gineann sé an t-aschur nuair a chuirtear an clár i gcrích. Níl ann ach comhad teanga ríomhchlárúcháin eile atá cosúil le comhad foinse [C](/programming/c/) agus [C++](/programming/cpp/).

## 4ú Formáid Chomhaid - Tuilleadh Eolais


### 4ú Sampla Cód Teanga Ríomhchlárúcháin

Seo sampla de chlár simplí scríofa in Forth a ríomhann fachtóiruimhir uimhir tugtha:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * iolraíonn sé an dá luach ar bharr an chruach. rialaíonn an má agus tús/go dtí go dtógtar sreabhadh an chláir.

Chun an clár seo a úsáid, chuirfeá an sainmhíniú isteach san ateangaire Forth, agus ansin cuirfá an focal fachtóir leis an uimhir a dteastaíonn uait an fachtóir a aimsiú:

```
10 factorial .
```
Mar thoradh air seo bheadh an t-aschur 3628800, arb é 10 fachtóir é.

## Tagairtí

 * [Forth Teanga Ríomhchlárúcháin](https://en.wikipedia.org/wiki/Forth_(programming_language))

