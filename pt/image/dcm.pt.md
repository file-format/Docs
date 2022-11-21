{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo dcm", "formato de arquivo dcm", "o que é um arquivo dcm", "arquivo", "exemplo dcm", "extensão de arquivo dcm", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo DCM - Arquivo de informações médicas digitais",
  "description":"Saiba mais sobre o formato de arquivo do DCM e as APIs que podem criar e abrir arquivos do DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## O que é um arquivo DCM?

Arquivos com extensão .dcm representam imagens digitais que armazenam informações médicas de pacientes, como ressonâncias magnéticas, tomografias computadorizadas e imagens de ultrassom. Os arquivos DCM usam o formato de arquivo de imagem [DICOM](/pt/image/dicom) (Digital Imaging and Communications in Medicine) e podem incluir informações do paciente para referência. Foi desenvolvido pela [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) e teve como objetivo padronizar o formato de arquivo de imagem para distribuição e visualização de imagens médicas.

## Formato de arquivo DCM

Os arquivos DCM armazenam informações no formato de imagem DICOM. Esses arquivos armazenam o Data Set, que é uma informação do mundo real, que representa uma instância SOP relacionada a um DICOM IOD. As informações de meta do arquivo DICOM são armazenadas no arquivo seguidas pelo fluxo de bytes do conjunto de dados real.

### Informações de Meta do Arquivo DICOM ##

Cada arquivo DICOM inclui um cabeçalho de informações de identificação para o conjunto de dados encapsulado que consiste em:
* Um preâmbulo de arquivo de 128 bytes
* Prefixo DICOM de 4 bytes
* Elementos Meta do Arquivo

Este cabeçalho é obrigatório para todos os arquivos DICOM.

### Elementos de Meta do Arquivo ###
|Nome do atributo|Tag|Tipo| Descrição do atributo
---|---|---|---|
|Arquivo Preâmbulo|Sem Tag ou Campos de Comprimento|1|Um campo fixo de 128 bytes disponível para Perfil de Aplicação ou uso especificado de implementação. Se não for usado por um Perfil de Aplicativo ou uma implementação específica, todos os bytes devem ser definidos como 00H. Leitores ou Atualizadores de Conjunto de Arquivos não devem confiar no conteúdo deste Preâmbulo para determinar se este Arquivo é ou não um Arquivo DICOM.
|DICOM Prefix|Sem Tag ou Campos de Comprimento|1|Quatro bytes contendo a cadeia de caracteres "DICM". Este prefixo destina-se a ser usado para reconhecer que este arquivo é ou não um arquivo DICOM.
|File Meta Information Group Length|(0002,0000)|1|Número de bytes após este File MetaElement (final do campo Value) até e incluindo o último File MetaElement do Grupo 2 File Meta Information
|File Meta Information Version|(0002,0001)|1|Este é um campo de dois bytes onde cada bit identifica uma versão deste cabeçalho de File Meta Information. Na versão 1, o valor do primeiro byte é 00H e o valor do segundo valor do byte é 01H. As implementações de leitura de Arquivos com Meta Informação onde este atributo tem o bit 0 (lsb) do segundo byte definido como 1 podem interpretar a Meta Informação do Arquivo conforme especificado neste versão do PS3.10. Todos os outros bits não devem ser verificados.
|UID da classe SOP de armazenamento de mídia|(0002,0002)|1|Identifica exclusivamente a classe SOP associada ao conjunto de dados. Os UIDs de classe SOP permitidos para armazenamento de mídia são especificados em PS3.4 - Perfis de aplicativo de armazenamento de mídia.
|UID da instância SOP de armazenamento de mídia|(0002,0003)|1|Identifica exclusivamente a instância SOP associada ao conjunto de dados colocado no arquivo e seguindo as Metainformações do arquivo.
|Transfer Syntax UID|(0002,0010)|1|Identifica exclusivamente a sintaxe de transferência usada para codificar o conjunto de dados a seguir. Esta Sintaxe de Transferência não se aplica às Metainformações do Arquivo.
|Classe de Implementação UID|(0002,0012)|1|Identifica exclusivamente a implementação que gravou este arquivo e seu conteúdo. Ele fornece uma identificação inequívoca do tipo de implementação que gravou o arquivo por último no caso de problemas de intercâmbio.
|Nome da Versão de Implementação|(0002,0013)|3|Identifica uma versão para um UID de Classe de Implementação (0002,0012) usando até 16 caracteres do repertório.
|Título da Entidade do Aplicativo de Origem|(0002,0016)|3|O Título da Entidade do Aplicativo DICOM (AE) do EA que escreveu o conteúdo deste arquivo (ou o atualizou pela última vez). Se utilizado, permite rastrear a origem dos erros em caso de problemas de intercâmbio de mídia.
|UID do criador de informações privadas|(0002,0100)|3|O UID do criador das informações privadas (0002,0102).
|Informações Privadas|(0002,0102)|1C|Contém Informações Privadas colocadas nas Metainformações do Arquivo. O criador deve ser identificado em (0002,0100). Obrigatório se o UID do Criador de Informações Privadas (0002,0100) estiver presente.

### Encapsulamento do conjunto de dados ###

Um arquivo DICOM contém um único conjunto de dados que representa uma única instância SOP relacionada a uma única classe SOP. O UID da Sintaxe de Transferência das Metainformações do Arquivo DICOM deve definir a Sintaxe de Transferência usada para codificar o Conjunto de Dados.

### Suporte para informações de gerenciamento de arquivos ###

A camada de formato de mídia fornece as seguintes informações de gerenciamento de arquivos, se necessário, para um determinado perfil de aplicativo DICOM.

* Identificação do proprietário do conteúdo do arquivo

* Estatísticas de acesso a arquivos (por exemplo, data e hora de criação)

* Controle de acesso ao arquivo do aplicativo

* Controle de acesso de mídia física (por exemplo, proteção contra gravação)

## Referências ##
* [Padrão DICOM](https://www.dicomstandard.org/current/)
* [Formato de arquivo DICOM](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

