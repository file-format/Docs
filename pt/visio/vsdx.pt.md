{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo vsdx", "formato de arquivo vsdx", "o que é um arquivo vsdx", "arquivo", "exemplo vsdx", "extensão de arquivo vsdx","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Saiba mais sobre o formato de arquivo VSDX e APIs que podem criar e abrir arquivos VSDX.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VSDX?

Arquivos com extensão .vsdx representam o formato de arquivo do Microsoft Visio introduzido a partir do Microsoft Office 2013. Ele foi desenvolvido para substituir o formato de arquivo binário, [.VSD](/pt/image/vsd/), que é suportado por versões anteriores do Microsoft Visio. Ele também é compatível com os Serviços do Visio no Microsoft SharePoint Server 2013 e não requer um formato de arquivo intermediário para publicação no SharePoint Server. Os arquivos do Visio são usados para criar desenhos que contêm objetos visuais, fluxogramas, diagrama UML, fluxo de informações, organogramas, diagramas de software, layout de rede, modelos de banco de dados, mapeamento de objetos e outras informações semelhantes. Os arquivos gerados usando o Visio também podem ser exportados para diferentes formatos de arquivo, como [PNG](/pt/image/png/), [BMP](/pt/image/bmp/), [PDF](/pt/pdf/) e outros.

## Formato de arquivo ##

Os arquivos VSDX são baseados nas Convenções de Empacotamento Aberto e XML e os desenvolvedores podem se beneficiar desse formato aprendendo como trabalhar com esses arquivos programaticamente. O formato herda muitas das mesmas estruturas XML que suas partes do formato de arquivo de desenho XML do Visio (.vdx). A interoperabilidade com arquivos do Visio é bastante aumentada, pois softwares de terceiros podem manipular arquivos do Visio em um nível de formato de arquivo.

Alguns outros tipos de arquivo que compõem o formato de arquivo do Visio 2013 incluem:

* .vsdm (desenho habilitado para macro do Visio)
* .vssx (estêncil do Visio)
* .vssm (estêncil habilitado para macro do Visio)
* .vstx (modelo do Visio)
* .vstm (modelo habilitado para macro do Visio)

Nos bastidores, o formato de arquivo do Visio 2013 usa um meio estruturado para armazenar dados do aplicativo junto com recursos relacionados em um arquivo como [ZIP](/pt/compression/zip/). O arquivo ZIP pode ser extraído usando qualquer utilitário de extração padrão onde também contenha outros tipos de arquivos. Você pode simplesmente substituir a extensão de arquivo .vsdx por .zip no Windows explore para ver o conteúdo dentro do arquivo VSDX.

Cada arquivo do Visio é denominado como pacote que contém outros arquivos ou partes. Uma parte do pacote pode ser um arquivo XML, uma imagem ou até mesmo uma solução VBA. As partes dentro do pacote podem ser divididas em partes "documento" e "relacionamento".

### Documento ###

As partes do documento contêm o conteúdo real e os metadados do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém e até mesmo as conexões de dados das formas. Imagens e arquivos de texto dentro do pacote são considerados partes do documento.

### Relacionamentos ###

As partes de relacionamento de um arquivo do Visio são armazenadas na pasta "\_rels" e descrevem como as partes do pacote estão relacionadas a cada uma. Ele também fornece a estrutura do arquivo. Um documento XML autônomo usa o relacionamento pai/filho dos elementos para determinar o relacionamento das entidades entre si. Um formato de arquivo válido do Visio 2013 contém o conjunto correto de partes e o pacote contém as relações entre as partes.

Partes de relacionamento são documentos XML que descrevem os relacionamentos entre diferentes partes do documento dentro do pacote. Eles definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificada. Por exemplo, as partes de relacionamento são usadas para descrever quais mestres de forma estão associados ao arquivo, como as páginas se relacionam com o arquivo e entre si ou como imagens e objetos se relacionam com uma página específica.

## Referências ##

* [Introdução ao formato de arquivo do Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

