{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "arquivo", "extensão", "formato de arquivo", "implementação mrc", "Guia de programação", "exemplo mrc", "mIRC", "linguagem de script mIRC", "arquivos de INI", " linguagem de script mSL", "linguagem mIRC", "scripts mIRC", "linguagem de script" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - arquivo de linguagem de script mIRC",
  "description":"Saiba mais sobre o formato de arquivo MRC e APIs que podem criar e abrir arquivos MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## O que é um arquivo MRC?

mIRC é uma linguagem de script que é incorporada como um cliente IRC (Internet Relay Chat) no sistema operacional Windows. Ele fornece uma facilidade de proteção contra spam para uso pessoal e de canal. Para proporcionar uma melhor experiência de compatibilidade do usuário, esta linguagem de script mIRC permite a criação de janelas de diálogo. Os arquivos que contêm scripts, principalmente em formato de texto simples, são armazenados com a extensão de MRC ou como os arquivos de [INI](/pt/system/ini/). As funções desta linguagem são conhecidas como comandos e identificadores (quando retornam valor).

A linguagem mIRC fornece o carregamento de vários arquivos de script de uma só vez. Por outro lado, um arquivo pode fazer com que o outro não seja mais utilizado quando carregado simultaneamente. Os comandos são salvos e podem existir no IRC automaticamente. Os comandos e aliases usados neste idioma não incluem precedência de nenhum dos caracteres.

O mIRC é amplamente usado para fazer com que os bots gerenciem um canal automaticamente, mas também pode ser modificado pela linguagem de script mSL. Ele pode introduzir muitos novos recursos, como macros, capacidade de reprodução de música, pequenas macros e funções, jogos básicos ou operação de pequenos aplicativos.


## Breve história ##

Esta linguagem de script foi desenvolvida pela primeira vez em 1995 por Khaled Adam Bey. O design da linguagem de script também foi criado por Khalid. O alvo desta linguagem era a programação orientada a eventos. Inicialmente, a extensão de arquivo utilizada para os arquivos desta linguagem de programação era .mrc e .ini. Além disso, foi desenvolvido sob licença de software proprietário.

## Especificação Técnica ##

Algumas funções têm scripts personalizados por meio dessa linguagem mIRC e são conhecidas como aliases. Quando esses aliases retornam valores, eles são conhecidos como identificadores personalizados. Todas as variáveis contidas nesta linguagem mIRC são tipadas dinamicamente. Sigilos são usados pelos scripts mIRC. Outro recurso dessa linguagem de script são os pop-ups. Os usuários podem chamar pop-ups simplesmente selecionando-os. Remotes são especificados para determinados eventos. Os remotos são chamados quando ocorre o evento relativo.

Tokens delimitados por espaço são usados para quebrar cada linha de código desta linguagem. Existem algumas outras extensões populares usadas para arquivos mIRC, como MDX (mIRC Dialog Extension) e DCX (Dialog Control Extension). Ambos são extensões de diálogo e são comparativamente mais populares. As construções de linguagem são referidas pela nomenclatura desta linguagem de script. A linguagem mIRC envolve diferentes aspectos de uma linguagem de script, como variáveis locais e globais, variáveis binárias, tabelas de hash e manipulação de arquivos.


## Exemplo de formato de arquivo MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/pt/echo) 'Hello World!' into the active window(-a)
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

## Referência ##

* [MIRC - pela Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



