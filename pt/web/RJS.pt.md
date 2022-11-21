{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "RJS", "Arquivo Javascript Ruby"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Arquivo Javascript Ruby",
  "description":"Saiba mais sobre o que é formato de arquivo RJS e APIs que podem criar e abrir arquivos RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## O que é um arquivo RJS?

Um arquivo com extensão .rjs é uma combinação de código Ruby e JavsScript que permite que desenvolvedores Rails usem Ruby para produzir código JavaScript dinâmico. O código Ruby está embutido em funções Java e é compilado no servidor web que requer que o mecanismo Ruby esteja rodando no servidor. RJS é semelhante a [RHTML](/pt/web/rhtml/); a única diferença é que a lateral contém código Ruby em [HTML](/pt/web/html/) enquanto contém código Ruby em funções Javascript.

## Formato de arquivo RJS

Os arquivos RJS são codificados em texto simples como qualquer outra linguagem de script ou programação. Quando tal página é solicitada pelo cliente, o código Ruby é executado no servidor, e apenas o código HTML e Javascript são retornados ao navegador do cliente. A sintaxe do arquivo RJS é semelhante à da combinação da sintaxe Ruby e JavaScript, de modo que apenas o código Ruby é incorporado nas funções JavaScript.

### Exemplo de RJS

O exemplo a seguir mostra um código Ruby simples de forma independente e, em seguida, incorporado em uma função JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
e segue o RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referências

* [RJS](https://github.com/makevoid/rjs)

