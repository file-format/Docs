{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "arquivo mhtml", "formato de arquivo mhtml", "tipo de arquivo mhtml", "arquivo", "tipo", "o que é um arquivo mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Arquivo HTML MIME",
  "description":"Saiba mais sobre o formato de arquivo MHTML e APIs que podem criar e abrir arquivos MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo MHTML?

Arquivos com extensão MHTML representam um formato de arquivo de página da web que pode ser criado por vários aplicativos diferentes. O formato é conhecido como formato de arquivo porque salva o código da Web **[HTML](/pt/web/html/)** e os recursos associados em um único arquivo. Esses recursos incluem qualquer coisa vinculada à página da Web, como imagens, applets, animações, arquivos de áudio e assim por diante. Os arquivos MHTML podem ser abertos em vários aplicativos, como Internet Explorer e Microsoft Word. O Microsoft Windows usa o formato de arquivo MHTML para registrar cenários de problemas observados durante o uso de qualquer aplicativo no Windows que levante problemas. O formato de arquivo MHTML codifica o conteúdo da página de forma semelhante às especificações definidas em message/rfc822, que são especificações relacionadas a e-mail de texto simples. As especificações reais do formato são detalhadas por [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Formato de arquivo MHTML

O MHTML também é conhecido como MIME Encapsulation of Aggregate HTML documents por sua capacidade de codificar páginas da Web HTML juntamente com seus recursos em um único arquivo da Web. De acordo com as especificações RFC 2557, um documento agregado é uma mensagem codificada em MIME que contém um recurso raiz (objeto), bem como outros recursos vinculados a ele por meio de URIs. Esses outros recursos podem ser a representação de imagens em linha, folhas de estilo, applets, etc. Além disso, podem ser a raiz de outros documentos multimídia. As especificações completas do documento para o formato de arquivo MHTML estão detalhadas na [RFC 2557](https://tools.ietf.org/html/rfc2557) e devem ser consultadas para qualquer tipo de desenvolvimento de aplicativo para leitura/gravação deste formato de arquivo. A norma especifica que as partes do corpo a serem referenciadas podem ser identificadas por um Content-ID ou por um Content-Location.

### Cabeçalhos de conteúdo MIME

Um cabeçalho de conteúdo MIME, Content-Location, é definido para resolver referências de URI a recursos em outras partes do corpo. Esse cabeçalho pode ocorrer em qualquer cabeçalho de mensagem ou conteúdo.

### Cabeçalho de localização do conteúdo

Um Content-Location é uma representação de um URI que rotula o conteúdo de uma parte do corpo onde ele é colocado. Seu valor pode ser um URI absoluto ou relativo. Ele pode ser usado para rotular um recurso que não pode ser recuperado por alguns ou por todos os destinatários de uma mensagem. Uma única mensagem pode ter apenas um único cabeçalho Content-Location. Exemplo de uma estrutura multiparte/relacionada contendo partes do corpo com rótulos Content-Location e Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URIs de Agregados MHTML

O URI do agregado MHTML é diferente do URI raiz. O campo de cabeçalho Content-Location deve ser aplicado a todo o agregado se for usado no cabeçalho de um cabeçalho de várias partes/relacionado. Da mesma forma, o conjunto de recursos recuperados pode ser diferente do conjunto de recursos recuperados usando os Content-Locations de suas partes quando o URI referente ao agregado MHTML é usado para recuperar esse agregado. Por exemplo, recuperar um agregado MHTML pode retornar uma versão antiga, enquanto recuperar o URI raiz e seus objetos vinculados em linha podem retornar uma versão mais recente.

## Referências

* [encapsulamento MIME de documentos agregados - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Formato de arquivo MHTML - pela Wikipedia](https://en.wikipedia.org/wiki/MHTML)

