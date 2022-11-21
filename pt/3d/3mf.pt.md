{
  "date" : "2019-12-09",
  "keywords" :[ "arquivo 3mf", "formato de arquivo 3mf", "o que é um arquivo 3mf", "arquivo", "exemplo 3mf", "extensão de arquivo 3mf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Saiba mais sobre o formato de arquivo 3MF e APIs que podem abrir e criar arquivos 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## O que é um arquivo 3MF?

3MF, 3D Manufacturing Format, é usado por aplicativos para renderizar modelos de objetos 3D para uma variedade de outros aplicativos, plataformas, serviços e impressoras. Ele foi construído para evitar as limitações e problemas em outros formatos de arquivo 3D, como [STL](/pt/cad/stl/), para trabalhar com as versões mais recentes de impressoras 3D. 3MF é um formato de arquivo relativamente novo que foi desenvolvido e publicado pelo consórcio 3MF. É rico o suficiente para descrever completamente um modelo, retendo informações internas, cores e outras características que o tornam extensível para suportar novas inovações em impressão 3D. O formato é extensível, capaz de ser amplamente adotado e livre de problemas que afetam outros formatos de arquivo amplamente utilizados.

## Breve História do Formato de Arquivo 3MF

As limitações existentes nos formatos de arquivos descritivos de modelos disponíveis, como STL e outros, levam as marcas líderes a se reunirem e formularem um formato de arquivo mais extensível para impressão 3D. Uma consideração importante foi como os aplicativos devem passar os dados do modelo para as impressoras 3D. O consórcio 3MF, portanto, surgiu para apoiar um novo formato de arquivo 3D chamado 3MF com o objetivo de torná-lo extensível o suficiente para atender às necessidades de impressão 3D. Várias empresas fizeram parte deste consórcio, incluindo Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP e outras. A Microsoft doou seu trabalho em andamento no formato de arquivo 3D como ponto de partida para o desenvolvimento colaborativo da especificação pelo 3MF Consortium.

## Formato de arquivo 3MF - Mais informações

3MF é um formato de dados baseado em XML – XML compactado legível por humanos – que inclui definições para dados relacionados à fabricação 3D, incluindo extensibilidade de terceiros para dados personalizados. O formato de arquivo 3MF foi projetado tendo em mente as limitações e problemas enfrentados por outros formatos de arquivo 3D. Isso levou à formulação do formato de arquivo 3MF que é:

* **Completo:** contendo todas as informações necessárias de modelo, material e propriedade em um único arquivo
* **Legível por humanos:** usando estruturas comuns como OPC, [ZIP](/pt/compression/zip/) e XML para facilitar o desenvolvimento
* **Simples:** uma especificação curta e clara, facilitando o desenvolvimento e a validação rápida
* **Extensível:** o aproveitamento de namespaces XML permite extensões públicas e privadas, mantendo a compatibilidade
* **Sem ambiguidade:** testes de linguagem e conformidade claros garantem que um arquivo seja sempre consistente do digital ao físico
* **Gratuito:** O acesso e implementação da especificação 3MF é e sempre será livre de royalties, patentes e licenciamento

As especificações para o formato de arquivo 3MF são hospedadas no [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) para acesso público e atualizações contínuas. A versão atual publicada é a 1.2.3 que descreve o conjunto de convenções para o uso de XML e outras tecnologias amplamente disponíveis para descrever o conteúdo e a aparência de um ou mais modelos 3D. Os desenvolvedores que desejam construir sistemas para processamento de formatos de arquivo 3MF podem consultar essas especificações para fins de implementação.

## Especificações de formato de arquivo 3MF

O formato de arquivo 3MF usa as especificações Open Packaging na forma de arquivo ZIP para seu modelo físico. Inclui um conjunto bem definido de partes e relacionamentos que atendem a um propósito específico no documento. Isso também faz com que o formato siga o recurso do pacote, incluindo assinaturas digitais e miniaturas.

### O Documento 3MF - Uma Visão Geral

Um documento 3MF típico tem a seguinte aparência:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

A carga útil inclui o conjunto completo de peças necessárias para processar a peça do Modelo 3D. Todo o conteúdo a ser usado para fabricar um objeto descrito na carga útil 3D DEVE estar contido no Documento 3MF. A descrição de cada parte do documento, juntamente com seu status conforme necessário ou opção, é fornecida na tabela a seguir.


|**Nome**|**Descrição**|**Fonte do relacionamento**|**Obrigatório/Opcional**
--- | --- | --- | ---
|Modelo 3D|Contém a descrição de um ou mais objetos 3D para fabricação.|Pacote|NECESSÁRIO
|Propriedades do núcleo|A parte OPC que contém várias propriedades do documento.|Pacote|OPCIONAL
|Origem da Assinatura Digital|A parte OPC que é a raiz das assinaturas digitais no pacote.|Pacote|OPCIONAL
|Assinatura Digital|Partes OPC que contêm uma assinatura digital.|Origem da Assinatura Digital|OPCIONAL
|Certificado de Assinatura Digital|Peças OPC que contêm um certificado de assinatura digital.|Assinatura Digital|OPCIONAL
|PrintTicket|Fornece configurações a serem usadas na saída do(s) objeto(s) 3D na parte do modelo 3D.|Modelo 3D|OPCIONAL
|Miniatura|Contém uma pequena imagem JPEG ou PNG que representa os objetos 3D no pacote ou o pacote como um todo.|Pacote|OPCIONAL
|Textura 3D|Contém uma textura usada para aplicar cor a um objeto 3D na parte do Modelo 3D (disponível para extensões)|Modelo 3D|OPCIONAL
|Peças Personalizadas|Peças OPC que estão associadas a metadados|Pacote|OPCIONAL

As [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Recursos de objetos](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Recursos Materiais](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) e [Recursos do pacote](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) seções de especificações documento fornecem informações detalhadas sobre o documento 3MF.

## Referências ##

* [Especificações de formato de arquivo 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Por Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

