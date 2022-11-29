{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "fil", "tillägg", "filformat", "mrc implementering", "Programmeringsguide", "mrc exempel", "mIRC", "mIRC skriptspråk", "filer av INI", " mSL-skriptspråk", "mIRC-språk", "mIRC-skript", "skriptspråk" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC Script Language File",
  "description":"Läs mer om MRC-filformat och API:er som kan skapa och öppna MRC-filer.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Vad är en MRC fil?

mIRC är ett skriptspråk som är inbäddat som en IRC-klient (Internet Relay Chat) i Windows operativsystem. Det ger en möjlighet att skydda mot skräppost för personlig användning och kanalanvändning. För att ge en bättre upplevelse av användarkompatibilitet tillåter detta mIRC-skriptspråk att skapa dialogfönster. Filerna som innehåller skript, mestadels i oformaterad text, lagras med MRC-tillägget eller som filerna till [INI](/sv/system/ini/). Funktioner i detta språk är kända som kommandon och identifierare (när de returnerar värde).

mIRC-språket ger laddning av flera skriptfiler på en gång. Å andra sidan kan en fil göra att den andra inte längre används när den laddas samtidigt. Kommandon sparas och de kan existera i IRC automatiskt. Kommandon och alias som används på detta språk har inte företräde för något av tecknen.

mIRC används flitigt för att få bots att hantera en kanal automatiskt, men det kan också modifieras av mSL-skriptspråket. Det kan introducera många nya funktioner som makron, musikuppspelningsförmåga, små makron och funktioner, grundläggande spel eller drift av små applikationer.


## Kortfattad bakgrund ##

Detta skriptspråk utvecklades först 1995 av Khaled Adam Bey. Utformningen av skriptspråket skapades också av Khalid. Målet för detta språk var händelsestyrd programmering. Från början var filtillägget som användes för filerna i detta programmeringsspråk .mrc och .ini. Dessutom utvecklades den under licens av proprietär programvara.

## Teknisk specifikation ##

Vissa funktioner är anpassade skriptade genom detta mIRC-språk och är kända som alias. När dessa alias returnerar värden kallas de anpassade identifierare. Alla variabler som finns i detta mIRC-språk är dynamiskt skrivna. Sigils används av mIRC-skripten. En annan funktion i detta skriptspråk är popup-fönster. Användarna kan ringa upp popup-fönster genom att helt enkelt välja dem. Fjärrkontroller är specificerade för vissa händelser. Fjärrkontrollerna anropas när den relativa händelsen inträffar.

Mellanslagsavgränsade tokens används för att bryta varje kodrad på detta språk. Det finns några andra populära tillägg som används för mIRC-filer som MDX (mIRC Dialog Extension) och DCX (Dialog Control Extension). Båda dessa är dialogtillägg och är jämförelsevis mer populära. Språkkonstruktionerna refereras till av nomenklaturen för detta skriptspråk. mIRC-språket involverar olika aspekter av ett skriptspråk som lokala och globala variabler, binära variabler, hashtabeller och filhantering.


## Exempel på MRC-filformat ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/sv/echo) 'Hello World!' into the active window(-a)
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

## Referens ##

* [MIRC - av Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



