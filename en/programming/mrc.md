{
  "date" : "2021-09-14", 
  "keywords" : [ "mrc", "file", "extension", "file format", "mrc implementation", "Programming Guide", "mrc example", "mIRC", "mIRC scripting language", "files of INI", "mSL scripting language", "mIRC language", "mIRC scripts", "scripting language" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MRC - mIRC Script Language File",
  "description":"Learn about MRC file format and APIs that can create and open MRC files.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-09-14"
}

## What is an MRC file?

mIRC is a scripting language that is embedded as an IRC client (Internet Relay Chat) in the Windows operating system. It provides a facility of protection from spamming for personal and channel use. To provide a better experience of user compatibility, this mIRC scripting language allows the creation of dialogue windows. The files that contain scripts, mostly in a plain text format are stored with the extension of MRC or as the files of [INI](/system/ini/). Functions of this language are known as commands and identifiers (when they return value).

mIRC language provides the loading of multiple script files at one time. On the other hand, one file can cause the other to be no longer used when loaded simultaneously. Commands are saved and they can exist in IRC automatically. The commands and aliases used in this language do not comprise precedence of any of the characters.

mIRC is used widely for making the bots manage a channel automatically but it can be modified too by the mSL scripting language. It can introduce many new features like macros, music playing ability, small macros and functions, basic games, or operating small applications. 


## Brief History ##

This scripting language was first developed in 1995 by Khaled Adam Bey. The design of the scripting language was also created by Khalid. The target of this language was event-driven programming. Initially, the file extension used for the files of this programming language was .mrc and .ini. Moreover, it was developed under the license of proprietary software.

## Technichal Specification ##

Some functions are custom scripted through this mIRC language and are known as aliases. When these aliases return values they are known as custom identifiers. All of the variables contained in this mIRC language are dynamically typed. Sigils are used by the mIRC scripts. Another feature of this scripting language is pop-ups. The users can call pop-ups by simply selecting them. Remotes are specified to certain events. The remotes are called when the relative event occurs.

Space delimited tokens are used to break each line of code of this language. There are some other popular extensions used for mIRC files such as MDX (mIRC Dialog Extension) and DCX (Dialog Control Extension). Both of these are dialogue extensions and are comparatively more popular. The language constructs are referred to by the nomenclature of this scripting language. The mIRC language involves different aspects of a scripting language such as local and global variables, binary variables, hash tables, and file handling.


## MRC File Format Example ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
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

## Reference ##

* [MIRC - by Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)


