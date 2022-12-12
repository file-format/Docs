{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "soubor", "rozšíření", "formát souboru", "implementace mrc", "Průvodce programováním", "příklad mrc", "mIRC", "skriptovací jazyk mIRC", "soubory INI", " skriptovací jazyk mSL", "jazyk mIRC", "skripty mIRC", "skriptovací jazyk" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - soubor skriptovacího jazyka mIRC",
  "description":"Další informace o formátu souboru MRC a rozhraních API, která mohou vytvářet a otevírat soubory MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Co je soubor MRC?

mIRC je skriptovací jazyk, který je zabudován jako IRC klient (Internet Relay Chat) v operačním systému Windows. Poskytuje ochranu před spamem pro osobní a kanálové použití. Pro zajištění lepší uživatelské kompatibility umožňuje tento skriptovací jazyk mIRC vytváření dialogových oken. Soubory, které obsahují skripty, většinou ve formátu prostého textu, jsou uloženy s příponou MRC nebo jako soubory [INI](/cs/system/ini/). Funkce tohoto jazyka jsou známé jako příkazy a identifikátory (když vracejí hodnotu).

Jazyk mIRC poskytuje načítání více souborů skriptů najednou. Na druhou stranu, jeden soubor může způsobit, že druhý již nebude používán při současném načítání. Příkazy se ukládají a mohou v IRC existovat automaticky. Příkazy a aliasy používané v tomto jazyce nezahrnují přednost žádného ze znaků.

mIRC se široce používá k tomu, aby roboti spravovali kanál automaticky, ale lze jej upravit také skriptovacím jazykem mSL. Může zavést mnoho nových funkcí, jako jsou makra, schopnost přehrávání hudby, malá makra a funkce, základní hry nebo ovládání malých aplikací.


## Stručná historie ##

Tento skriptovací jazyk byl poprvé vyvinut v roce 1995 Khaledem Adamem Beyem. Také design skriptovacího jazyka vytvořil Khalid. Cílem tohoto jazyka bylo programování řízené událostmi. Zpočátku byla přípona souborů používaná pro soubory tohoto programovacího jazyka .mrc a .ini. Navíc byl vyvinut pod licencí proprietárního softwaru.

## Technická specifikace ##

Některé funkce jsou vlastní skripty prostřednictvím tohoto jazyka mIRC a jsou známé jako aliasy. Když tyto aliasy vracejí hodnoty, jsou známé jako vlastní identifikátory. Všechny proměnné obsažené v tomto jazyce mIRC jsou dynamicky typovány. Sigils jsou používány skripty mIRC. Další funkcí tohoto skriptovacího jazyka jsou vyskakovací okna. Uživatelé mohou volat vyskakovací okna pouhým výběrem. Dálkové ovladače jsou určeny pro určité události. Dálkové ovladače jsou volány, když dojde k relativní události.

Tokeny oddělené mezerou se používají k přerušení každého řádku kódu tohoto jazyka. Existují některá další populární rozšíření používaná pro soubory mIRC, jako je MDX (mIRC Dialog Extension) a DCX (Dialog Control Extension). Obě jsou rozšířením dialogu a jsou poměrně populárnější. Na jazykové konstrukce se odkazuje nomenklatura tohoto skriptovacího jazyka. Jazyk mIRC zahrnuje různé aspekty skriptovacího jazyka, jako jsou lokální a globální proměnné, binární proměnné, hashovací tabulky a práce se soubory.


## Příklad formátu souboru MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/cs/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## reference ##

* [MIRC – z Wikipedie](https://en.wikipedia.org/wiki/MIRC_scripting_language)



