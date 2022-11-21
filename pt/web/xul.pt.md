{
  "date" : "2021-05-24",
  "keywords" :["xul", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "Linguagem de interface de usuário XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Arquivo de linguagem de interface de usuário XML",
  "description":"Saiba mais sobre o formato de arquivo XUL e APIs que podem criar e abrir arquivos XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## O que é um arquivo XUL?

Um arquivo com extensão .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) significa XML User Interface Language) é um arquivo de linguagem de marcação baseado em [XML](/pt/web/xml/) para criação de interfaces de usuário. Ele foi desenvolvido pela Mozilla para desenvolvedores criarem elementos de interface gráfica do usuário semelhantes a outras linguagens de marcação usadas para criar páginas da web. O XUL tem sido amplamente utilizado pela Mozilla em seu navegador Firefox, onde usou a base de código Mozilla. A renderização XUL é realizada usando o
[Motor Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). Forks do Firefox, como Pale Moon, Basilisk e Waterfox, mantêm o suporte para complementos XUL. Os arquivos XUL são identificados com o tipo MIME: application/vnd.mozilla.xul+xml.

## Formato de arquivo XUL

Os arquivos XUL são escritos em texto simples com base no formato de arquivo XML e são renderizados usando o mecanismo Gecko. As três partes principais de uma estrutura XUL são:

* `Conteúdo` - Isso inclui as declarações da janela e os elementos da interface do usuário contidos nelas.
* `Skin` - Inclui quaisquer folhas de estilo, imagens e outros arquivos relacionados ao tema. A aparência de uma janela é descrita nas folhas de estilo.
* `Locale` - O texto exibido em uma janela é armazenado separadamente e vários conjuntos de arquivos de idioma podem ser usados pelos usuários.

### Exemplo de XUL

O exemplo a seguir cria três botões empilhados uns sobre os outros na direção vertical.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referências

* [XUL - Por Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Documentação arquivada XUL - Por Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

