{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml", "arquivo dhtml", "formato de arquivo dhtml", "tipo de arquivo dhtml", "arquivo", "tipo", "o que é um arquivo dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Formato de arquivo HTML dinâmico",
  "description":"Saiba mais sobre o formato de arquivo DHTML e APIs que podem criar e abrir arquivos DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DHTML?

Um arquivo com extensão .dhtml é um arquivo dinâmico [HTML](/pt/web/html/) usado para criar conteúdo dinâmico de uma página da web. Um elemento da web criado em DHTML é orientado a eventos e não requer recarregar a página. Na maioria dos casos, um arquivo DHTML é usado para criar o conteúdo dinâmico de uma página da Web, como menus suspensos, camadas flutuantes, botões de rolagem e outros conteúdos dinâmicos. Você encontra elementos html dinâmicos quase diariamente em sua vida quando passa o mouse em um item de menu e abre mais opções de submenu. DHTML faz uso de tecnologias da web como [HTML](/pt/web/html/), [Javascript](/pt/web/js/), HTML DOM, HTML Events e [CSS](/pt/web/css/) para alcançar a dinâmica comportamento dos elementos.

## Formato de arquivo DHTML

Os arquivos DHTML são arquivos de texto simples que contêm código DHTML para implementar o comportamento dinâmico dos elementos da web.


### DHTML DOM

O DHTML Document object Model (DOM) é baseado no HTML DOM que é uma estrutura em árvore com elementos, atributos e texto conforme mostrado na imagem a seguir.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

O nó `Document` pode ser usado para chamar várias funções para implementar diferentes funcionalidades. O exemplo a seguir simplesmente usa o método document.write() de JavaScript no DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Este código escreve o texto "Hello World" para saída no navegador.

### Eventos DHTML

|S.N.|Evento|Ocorrência|
---|---|---|
|1|onabort|Ocorre quando o usuário aborta o carregamento da página ou arquivo de mídia.|
|2|onblur|Ocorre quando o usuário deixa um objeto HTML.|
|3|onchange|Ocorre quando o usuário altera ou atualiza o valor de um objeto.|
|4|onclick|Ocorre ou é acionado quando qualquer usuário clica em um elemento HTML.|
|5|ondblclick|Ocorre quando o usuário clica duas vezes em um elemento HTML.|
|6|onfocus|Ocorre quando o usuário foca em um elemento HTML. Este manipulador de eventos funciona de forma oposta ao onblur.|
|7|onkeydown|Ele é acionado quando um usuário pressiona uma tecla em um dispositivo de teclado. Este manipulador de eventos funciona para todas as chaves.|
|8|onkeypress|É acionado quando os usuários pressionam uma tecla em um teclado. Este manipulador de eventos não é acionado para todas as chaves.|
|9|onkeyup|Ocorre quando um usuário libera uma tecla de um teclado após pressionar um objeto ou elemento.|
|10|onload|Ocorre quando um objeto é completamente carregado.|
|11|onmousedown|Ocorre quando um usuário pressiona o botão do mouse sobre um elemento HTML.|
|12|onmousemove|Ocorre quando um usuário move o cursor sobre um objeto HTML.|
|13|onmouseover|Ocorre quando um usuário move o cursor sobre um objeto HTML.|
|14|onmouseout|Ocorre ou dispara quando o ponteiro do mouse é movido para fora de um elemento HTML.|
|15|onmouseup|Ocorre ou dispara quando o botão do mouse é liberado sobre um elemento HTML.|
|16|onreset|É utilizado pelo usuário para redefinir o formulário.|
|17|onselect|Ocorre após selecionar o conteúdo ou texto em uma página da web.|
|18|onsubmit|É acionado quando o usuário clica em um botão após o envio de um formulário.|
|19|onunload|É acionado quando o usuário fecha uma página da web.|

## Referências

* [HTML dinâmico - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

