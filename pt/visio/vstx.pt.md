{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo vstx", "formato de arquivo vstx", "o que é um arquivo vstx", "arquivo", "exemplo vstx", "extensão de arquivo vstx","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Formato de arquivo do Microsoft Visio",
  "description":"Saiba mais sobre o formato de arquivo VSTX e APIs que podem criar e abrir arquivos VSTX.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VSTX?

Arquivos com extensões .vstx são arquivos de modelo de desenho criados com o Microsoft Visio 2013 e superior. Esses arquivos VSTX fornecem o ponto de partida para a criação de desenhos do Visio, salvos como arquivos [.VSDX](/pt/image/vsdx/), com layout e configurações padrão. Em geral, os arquivos do Visio são usados para criar desenhos que contêm objetos visuais, fluxogramas, diagrama UML, fluxo de informações, organogramas, diagramas de software, layout de rede, modelos de banco de dados, mapeamento de objetos e outras informações semelhantes. Os arquivos gerados usando o Visio também podem ser exportados para diferentes formatos de arquivo, como [PNG](/pt/Image/PNG/), [BMP](/pt/Image/BMP/), [PDF](/pt/pdf/) e outros. Os programas que abrem arquivos VSTX incluem o Microsoft Visio para Windows e Mac que permitem abrir esses arquivos para visualização e edição. Também permite converter formatos de arquivo do Visio para vários outros formatos.

# Formato de arquivo VSTX #

O "X" na extensão do arquivo refere-se ao formato de arquivo OpenOffice que foi introduzido pela Microsoft como um formato de arquivo [ZIP](/pt/compression/zip/) para substituição de formatos de arquivo binários suportados anteriormente. Os arquivos VSTX, portanto, são baseados no formato de arquivo XML das especificações do OpenOffice, diferentemente do formato de arquivo [.VST](/pt/image/vst/) que está no formato binário.

Os arquivos VSDX são baseados nas Convenções de Empacotamento Aberto e XML e os desenvolvedores podem se beneficiar desse formato aprendendo como trabalhar com esses arquivos programaticamente. O formato herda muitas das mesmas estruturas XML que suas partes do formato de arquivo de desenho XML do Visio (.vdx). A interoperabilidade com os arquivos do Visio aumentou bastante, pois softwares de terceiros podem manipular arquivos do Visio em um nível de formato de arquivo.

Alguns outros tipos de arquivo que compõem o formato de arquivo do Visio 2013 incluem:

* .vsdm (desenho habilitado para macro do Visio)
* .vssx (estêncil do Visio)
* .vssm (estêncil habilitado para macro do Visio)
* .vstx (modelo do Visio)
* .vstm (modelo habilitado para macro do Visio)

Nos bastidores, o formato de arquivo do Visio 2013 usa um meio estruturado para armazenar dados do aplicativo junto com recursos relacionados em um arquivo como [ZIP](/pt/Compression/ZIP/). O arquivo ZIP pode ser extraído usando qualquer utilitário de extração padrão onde também contenha outros tipos de arquivos. Você pode simplesmente substituir a extensão do arquivo .VSTX por .ZIP no Windows explore para ver o conteúdo dentro do arquivo VSTX.

Cada arquivo do Visio é denominado como pacote que contém outros arquivos ou partes. Uma parte do pacote pode ser um arquivo XML, uma imagem ou até mesmo uma solução VBA. As partes dentro do pacote podem ser divididas em partes "documento" e "relacionamento".

### Documento ###

As partes do documento contêm o conteúdo real e os metadados do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém e até mesmo as conexões de dados das formas. Imagens e arquivos de texto dentro do pacote são considerados partes do documento.

### Relacionamentos ###

As partes de relacionamento de um arquivo do Visio são armazenadas na pasta "_rels" e descrevem como as partes do pacote estão relacionadas a cada uma. Ele também fornece a estrutura do arquivo. Um documento XML autônomo usa o relacionamento pai/filho dos elementos para determinar o relacionamento das entidades entre si. Um formato de arquivo válido do Visio 2013 contém o conjunto correto de partes e o pacote contém as relações entre as partes.

Partes de relacionamento são documentos XML que descrevem os relacionamentos entre diferentes partes do documento dentro do pacote. Eles definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificada. Por exemplo, as partes de relacionamento são usadas para descrever quais mestres de forma estão associados ao arquivo, como as páginas se relacionam com o arquivo e entre si ou como imagens e objetos se relacionam com uma página específica.

## Referências ##

* [Introdução ao formato de arquivo do Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

