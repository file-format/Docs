{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo vsdm", "formato de arquivo vsdm", "o que é um arquivo vsdm", "arquivo", "exemplo vsdm", "extensão de arquivo vsdm","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Formato de arquivo de desenho do Microsoft Visio",
  "description":"Saiba mais sobre o formato de arquivo VSDM e APIs que podem criar e abrir arquivos VSDM.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VSDM?

Arquivos com extensão .vsdm são arquivos de desenho criados com o aplicativo Microsoft Visio que oferece suporte a macros. Os arquivos VSDM são desenhos OPC/XML semelhantes ao VSDX, mas também fornecem a capacidade de executar macros quando o arquivo é aberto. Macros são ações/etapas definidas pelo usuário que são desenvolvidas no Visual Basic for Applications (VBA) e podem ser usadas para executar tarefas repetitivas. O formato de arquivo VSDM foi introduzido com o lançamento do Microsoft Visio 2013. Os arquivos do Visio são usados para criar desenhos que contêm objetos visuais, fluxogramas, diagrama UML, fluxo de informações, organogramas, diagramas de software, layout de rede, modelos de banco de dados, mapeamento de objetos e outros informações semelhantes. Os arquivos gerados usando o Visio também podem ser exportados para diferentes formatos de arquivo, como [PNG](/pt/image/png/), [BMP](/pt/image/bmp/), [PDF](/pt/pdf/) e outros.

## Formato de arquivo VSDM

Os arquivos VSDM são baseados nas Convenções de Empacotamento Aberto e XML e os desenvolvedores podem se beneficiar desse formato aprendendo a trabalhar com esses arquivos programaticamente. O formato herda muitas das mesmas estruturas XML que suas partes do formato de arquivo de desenho XML do Visio (.vdx). A interoperabilidade com os arquivos do Visio aumentou bastante, pois softwares de terceiros podem manipular arquivos do Visio em um nível de formato de arquivo.

Cada arquivo do Visio é denominado como pacote que contém outros arquivos ou partes. Uma parte do pacote pode ser um arquivo XML, uma imagem ou até mesmo uma solução VBA. As partes dentro do pacote podem ser divididas em partes "documento" e "relacionamento".

### Documento ###

As partes do documento contêm o conteúdo real e os metadados do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém e até mesmo as conexões de dados das formas. Imagens e arquivos de texto dentro do pacote são considerados partes do documento.

### Relacionamentos ###

As partes de relacionamento de um arquivo do Visio são armazenadas na pasta "\_rels" e descrevem como as partes do pacote estão relacionadas a cada uma. Ele também fornece a estrutura do arquivo. Um documento XML autônomo usa o relacionamento pai/filho dos elementos para determinar o relacionamento das entidades entre si. Um formato de arquivo válido do Visio 2013 contém o conjunto correto de partes e o pacote contém as relações entre as partes.

Partes de relacionamento são documentos XML que descrevem os relacionamentos entre diferentes partes do documento dentro do pacote. Eles definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificada. Por exemplo, as partes de relacionamento são usadas para descrever quais mestres de forma estão associados ao arquivo, como as páginas se relacionam com o arquivo e entre si ou como imagens e objetos se relacionam com uma página específica.

## Referências ##

* [Introdução ao formato de arquivo do Visio](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

