{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI File - Asterisk Gateway Interface File Format",
  "description":"Saiba mais sobre o que é o formato de arquivo AGI com exemplos e APIs que podem criar e abrir arquivos AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## O que é um arquivo AGI?

Um arquivo AGI é um arquivo de script usado pelo sistema de telefonia de código aberto, Asterisk. Ele contém informações que podem ser usadas para automatizar processos e o plano de discagem do Asterisk. Usando arquivos de script AGI, as conexões podem ser estabelecidas com bancos de dados relacionais como PostgreSQL ou MySQL. Além disso, os scripts AGI também podem ser usados para acessar outros recursos externos. Os scripts AGI podem transferir o controle do dialplan para um script AGI externo, permitindo que o Asterisk execute tarefas complexas.

## Formato de arquivo AGI - Mais informações

Os arquivos de script AGI são salvos como arquivos de texto e podem ser abertos em qualquer editor de texto para fazer alterações.

### Padrão Padrão de Comunicação AGI

O script AGI carrega as variáveis e seus valores enviados pelo Asterisk. Uma aparência comum dessas variáveis é a seguinte.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Essas variáveis são seguidas por uma linha em branco enviada pelo Asterisk, mostrando que o script AGI pode assumir o controle do dialplan agora.

### Linguagem de programação para arquivos de script AGI

Os scripts AGI geralmente podem ser escritos em Perl, [PHP](/pt/programming/php/), [C](/pt/programming/c/), Pascal ou Bourne Shell.

## Referências

* [Script AGI Asterisk](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

