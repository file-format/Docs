{
  "date" : "2021-05-24",
  "keywords" :["zul", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "abrir"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK User Interface File",
  "description":"Saiba mais sobre o formato de arquivo ZUL e APIs que podem criar e abrir arquivos ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## O que é um arquivo ZUL?

Um arquivo com extensão .zul é um arquivo da Web criado com o User Interface Markup Language (ZUML) e contém definições para elementos da interface do usuário. As classes Ajax e Java suportam o uso do ZUML baseado em [XML](/pt/web/xml/) para desenvolver arquivos do lado do servidor. O formato de arquivo ZUL foi desenvolvido pela ZK, uma estrutura de interface do usuário que permite criar aplicativos da Web e móveis sem o conhecimento de JavaScript ou AJAX.

## Formato de arquivo ZUL

Os arquivos ZUL são baseados em XML, consistindo em diferentes elementos para construir a interface do usuário. O carregador ZK usa cada elemento XML para criar um componente. O processamento geral dos elementos da página, como título da página, descrição, etc., são descritos por cada instrução de processamento XML do ZUML.

### Exemplo ZUL

No exemplo a seguir de código ZUML, a primeira linha especifica o título da página, a segunda linha cria um componente raiz com título e borda e a terceira linha cria um botão com rótulo e um ouvinte de evento.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
O esquema ZUL pode ser baixado em http://www.zkoss.org/2005/zul/zul.xsd.
## Referências

* [ZUL - Por ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Esquema ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

