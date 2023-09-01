{
  "date" : "2020-01-10",
  "keywords" :[ "arquivo otg", "formato de arquivo otg", "o que é um arquivo otg", "arquivo", "exemplo otg", "extensão de arquivo otg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Formato de arquivo de modelo de desenho OpenDocument",
  "description":"Saiba mais sobre o formato de arquivo OTG e APIs que podem criar e abrir arquivos OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## O que é um arquivo OTG?

Um arquivo OTG é um modelo de desenho criado usando o padrão OpenDocument que segue o OASIS Office Applications [especificação 1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Ele representa a organização padrão dos elementos de desenho para uma imagem vetorial que pode ser usada para aprimorar ainda mais o conteúdo do arquivo. Os arquivos OTF são como qualquer outro arquivo baseado no formato OpenDocument que se baseia no formato XML para representar o conteúdo do documento. Os arquivos OTF podem ser visualizados abrindo-os em qualquer editor de texto ou XML padrão.

## Especificações de formato de arquivo OTG ##

O formato de arquivo OTG é baseado no formato XML OpenDocument que possui um esquema bem estabelecido. A estrutura de cada componente de um formato OpenDocument é representada por um elemento que possui atributos associados e é comum a todos os tipos de documentos, como documento de texto, planilha ou arquivo de desenho. O OTG, sendo um modelo de desenho, utiliza extensivamente as especificações de conteúdo gráfico que incluem:

* Recursos de página aprimorados para aplicativos gráficos
* Formas de desenho
* Quadros
* Formas 3D
* Forma personalizada
* Formas de apresentação
* Animações de apresentação
* Animações de apresentação SMIL
* Eventos de apresentação
* Apresentar campos de texto
* Conteúdo do Documento de Apresentação

### Recursos de página aprimorados para aplicativos gráficos ###
#### Mestre de Apostilas ####

O elemento Folheto Mestre é um modelo para gerar automaticamente as páginas de folheto para aplicativos que suportam a impressão de tais páginas.
Os atributos que podem estar associados ao `<style:handout-master>` elemento são:

|Layout|Atributo|Descrição
---|---|---|
|Layout da página de apresentação|apresentação:nome do layout da página de apresentação|Links para `<style:presentation-page-layout>`  atributo
|Layout da página|`style:page-layout-name` | Especifica um layout de página que contém os tamanhos, a borda e a orientação da página mestra do folheto.
|Estilo de página|`draw:style-name`|Atribui atributos de formatação adicionais a uma página-mestre de folheto atribuindo um estilo de página de desenho.|
|Declaração do cabeçalho| `apresentação:use-header-name`| Especifica o nome da declaração do campo de cabeçalho que é usado para todos os campos de cabeçalho exibidos na página mestra do folheto.
|Declaração de Rodapé| Presentation:use-footer-name|Especifica o nome da declaração do campo de rodapé que é usado para todos os campos de rodapé exibidos na página mestra do folheto.
|Declaração de data e hora|use-date-time-name|Especifica o nome da declaração de campo de data e hora que é usada para todos os campos de data e hora exibidos na página mestra do folheto.

### Formas de desenho ###
O formato OpenDocument suporta várias formas de desenho que podem ser usadas por qualquer tipo de documento.

|Forma|Atributos Associados| elementos
---|---|---|
Retângulo - `<draw:rect> `|Posição, tamanho, estilo, camada, índice Z, ID, ID da legenda, âncora de texto, fundo da tabela, posição final do desenho, cantos arredondados|Título, descrição longa, ouvintes de eventos, pontos de cola, texto
Linha `<draw:line> `|Estilo, Camada, Índice Z, ID, ID da legenda e Transformação, Âncora de texto, plano de fundo da tabela, posição final do desenho, Ponto inicial, Ponto final|Título, Descrição longa, Ouvintes de evento, Pontos de cola, Texto
Polilinha `<draw:polyline> `| Posição, Tamanho, Caixa de exibição, Estilo, Camada, Índice Z, ID, ID da legenda e Transformação, Âncora de texto, plano de fundo da tabela, posição final do desenho, Pontos| Título, descrição longa, ouvintes de eventos, pontos de cola, texto
Polígono `<draw:polygon> `|Posição, Tamanho, Caixa de visualização, Estilo, Camada, Índice Z, ID, ID da legenda e Transformação, Âncora de texto, plano de fundo da tabela, posição final do desenho, Pontos|Título, Descrição longa, Ouvintes de eventos, Pontos de cola, Texto
|Polígono Regular `<draw:regular-polygon> `|Posição, Tamanho, Estilo, Camada, Índice Z, ID, ID da legenda e Transformação, Âncora de texto, plano de fundo da tabela, posição final do desenho, Côncavo, Cantos, Nitidez|Título, Descrição longa, Ouvintes de evento, Pontos de cola, Texto
|Caminho `<draw:path> `|Posição, tamanho, caixa de exibição, estilo, camada, índice Z, ID, identificação da legenda e transformação, âncora de texto, plano de fundo da tabela, posição final do desenho, dados do caminho| Título, descrição longa, ouvintes de eventos, pontos de cola, texto

### Quadros ###
Um quadro, em um documento de desenho, é um recipiente retangular que contém caixas de texto, imagens ou objetos. Os quadros suportam recursos adicionais, como contornos, mapas de imagem e hiperlinks. Um quadro pode conter tanto um objeto quanto uma imagem, permitindo assim ter múltiplas interpretações de um objeto. Os aplicativos renderizam o respectivo elemento com base no melhor suporte.

Os quadros podem conter:
* Caixas de texto
* Objetos representados no formato OpenDocument ou em um formato binário específico do objeto
* Imagens
* Miniaplicativos
* Plugins
* Quadros flutuantes

Um quadro está contido em um documento conforme mostrado abaixo.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referências ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

