{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Especificações de papel XML", "Arquivo", "Extensão", "Formato de arquivo", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Formato de arquivo de layout de página",
  "description":"Saiba mais sobre o formato de arquivo XPS e APIs que podem criar e abrir arquivos XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo XPS? ##

Um arquivo XPS representa arquivos de layout de página baseados em XML Paper Specifications criados pela Microsoft. Ele foi desenvolvido como uma substituição do formato de arquivo EMF e é semelhante ao formato de arquivo [PDF](/pt/pdf/), mas usa XML no layout, aparência e informações de impressão de um documento. É, de fato, mais justificado dizer que o XPS é uma tentativa de PDF, mas não conseguiu popularidade suficiente como propriedade do PDF por muitas razões. A Microsoft fornece o XPS Document Writer por padrão a partir do Windows 7 para a criação de arquivos XPS. Os arquivos XPS podem ser gerados selecionando o "Microsoft XPS Document Writer" como impressora durante a impressão do documento.

Os visualizadores XPS vêm integrados como parte do Windows Vista, Windows 7, Windows 8 e Internet Explorer 6 ou posterior. Os arquivos XPS tornam-se somente leitura assim que são gerados. Isso aumenta a confiança do usuário nos documentos recebidos enviados como XPS para a autenticidade do documento. Um documento XPS pode conter uma ou mais páginas convertidas do documento original.

## Breve história ##

A Microsoft submeteu a especificação XPS à Ecma International. Em junho de 2007, o Comitê Técnico Ecma 46 (TC46) foi criado para desenvolver um padrão baseado nas Especificações de Papel OpenXPS. A Ecma International aprovou o Padrão Ecma (ECMA-388) [especificações XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) em junho de 2009 na 97ª Assembléia Geral.

## Formato de arquivo XPS ##

O formato XPS consiste em marcação XML que define a composição de um documento e a aparência visual de cada página juntamente com regras de renderização para exibição ou impressão do documento. Ele retém todas as informações para recriar um documento em qualquer sistema, o que o torna independente dos recursos disponíveis nesse sistema. O formato é essencialmente um arquivo ZIP e se você renomear a extensão do arquivo para ZIP, verá os arquivos constituintes que contêm os dados do documento. Esses documentos incluem:

* arquivos de página de documento (.fpage) - Contém o conteúdo do documento e as configurações de formato do documento. Cada página no documento XPS tem um arquivo FPAGE.
* arquivo de configurações do documento (.fdoc) - Armazena as configurações incluídas no arquivo XPS.
* arquivos de fragmento de documento (.frag) - define as configurações para o arquivo XPS real e cada página do documento tem seu próprio arquivo .frag.

{{< figure src="../XPS-1.png" alt="Formato de arquivo XPS" >}}

Esses arquivos retêm o conteúdo do documento de forma que, se, por exemplo, alguém não tiver as mesmas fontes instaladas em sua máquina, o visualizador XPS ainda renderizará essas fontes originais. Isso implica a inclusão do arquivo de marcação XML para cada:

* Página
* Texto
* Fontes incorporadas
* Imagens raster
* Gráficos vetoriais 2D
* Gerenciamento de direitos digitais

O formato Documento XPS inclui um conjunto bem definido de partes e relacionamentos, cada um cumprindo uma finalidade específica no documento. O formato também estende os recursos do pacote, incluindo assinaturas digitais, miniaturas e intercalação.

Um documento XPS típico tem a seguinte aparência e pode ser analisado à luz do formato de arquivo XPS especificações.

{{< figure src="../XPS-2.png" alt="Formato de arquivo XPS" >}}


## Referências ##

* [Especificações de formato de arquivo XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Por Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

