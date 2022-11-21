{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "Linguagem de folha de estilo extensível"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo XSLT",
  "description":"Saiba mais sobre o formato de arquivo XSLT e APIs que podem criar e abrir arquivos XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## O que é um arquivo XSLT?

Um arquivo com extensão .xslt é um arquivo Extensible Stylesheet Language Transformation usado para transformar e estilizar um arquivo XML usando instruções XSL. O formato é usado para transformar documentos XML em formatos de saída padrão, como um documento de texto ou uma página da Web .html. Essa transformação cria um novo documento com base no conteúdo do documento XML existente. O XSLT está tornando-o teoricamente capaz de cálculos arbitrários.

## Formato de arquivo XSLT

O formato de arquivo XLST contém instruções de transformação em formato de texto simples que podem ser visualizados em qualquer editor de texto. Houve três revisões para a linguagem.

* `XSLT 1.0` - XSLT 1.0 foi publicado como uma recomendação do W3C em novembro de 1999.
* `XSLT 2.0` - Inclui modificações como manipulação de String usando expressões regulares, funções e operadores para manipular datas, horas e durações, vários documentos de saída, agrupamento e um sistema de tipos mais rico e forte verificação de tipos.
* `XSLT 3.0` - Tornou-se parte da Recomendação do W3C em 8 de junho de 2017 e os principais novos recursos incluem transformação de streaming, pacotes para melhorar a modularidade de folhas de estilo grandes, tratamento aprimorado de erros dinâmicos com, por exemplo, uma instrução xsl:try, e suporte para mapas e matrizes, permitindo que o XSLT manipule JSON e XML.

### Exemplo de XSLT

O exemplo a seguir foi extraído de [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Referências ##

* [XSLT - Por Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [Elementos XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

