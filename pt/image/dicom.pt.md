{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo dicom", "formato de arquivo dicom", "o que é um arquivo dicom", "arquivo", "exemplo dicom", "extensão de arquivo dicom", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Digital Imaging and Communications File Format",
  "description":"Saiba mais sobre o formato de arquivo DICOM e APIs que podem criar e abrir arquivos DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DICOM?

DICOM é a sigla para Digital Imaging and Communications in Medicine e pertence ao campo da Informática Médica. DICOM é usado para a integração de dispositivos de imagens médicas como impressoras, servidores, scanners etc de vários fornecedores e também contém dados de identificação de cada paciente para exclusividade. Os arquivos DICOM podem ser compartilhados entre duas partes se forem capazes de receber dados de imagem no formato DICOM. A parte de comunicação do DICOM é um protocolo de camada de aplicação e usa TCP/IP para comunicação entre entidades. As versões suportadas pelos serviços da Web são 1.0, 1.1, 2 ou posterior.

## História ##

O DICOM foi desenvolvido em conjunto pelo American College of Radiology (ACR) e pela National Electrical Manufacturers Association (NEMA) para a troca e visualização de imagens médicas como ressonâncias magnéticas, tomografias computadorizadas e imagens de ultrassom. Inicialmente, era difícil decodificar as imagens que as máquinas produziam. Portanto, ACR e NEMA juntos formaram uma equipe em 1983 que lançou seu primeiro padrão, ACR/NEMA 300 em 1985. A segunda versão foi lançada em 1988, que era mais popular entre os fornecedores, mas logo percebeu-se que a segunda versão também precisa ser aprimorada. A 3ª versão do padrão foi lançada em 1993 como "DICOM". 3.0 ainda é a versão mais recente, mas tem sido continuamente atualizada desde 1993.

## Formato de arquivo DICOM ##

DICOM é a combinação de definição de formato de arquivo e um protocolo de comunicação de rede. O DICOM usa a extensão .DCM. .DCM existem em dois formatos diferentes, ou seja, formato 1.xe formato 2.x. O formato DCM 1.x também está disponível em duas versões normal e estendida. Os protocolos HTTP e HTTPS são usados para os serviços web do DICOM.

### Cabeçalho do arquivo ###

O cabeçalho do arquivo contém Preâmbulo de Arquivo de 128 bytes e prefixo DICOM de 4 bytes.

**Preâmbulo # 128 Bytes**|**Prefixo # 4 Bytes “D, I, C, M**

**Preâmbulo** é usado para acessar as imagens e outros dados no arquivo DICOM, oferecendo compatibilidade com os formatos de arquivo de imagem comumente usados.

**Prefixo** contém a string "DICM" como caracteres maiúsculos.

### Conjunto de dados ###

Cada arquivo deve conter um único conjunto de dados representando a instância SOP e a Classe SOP com IOD relacionado. Conjunto de dados é a representação de informações do mundo real. O conjunto de dados contém elementos de dados e os elementos de dados contêm valores dos atributos desse objeto. A estrutura dos atributos é especificada em IODs. Um objeto de dados DICOM consiste em vários atributos, incluindo itens como nome, ID, etc., e também um atributo especial contendo os dados de pixel da imagem.

### Elementos de dados ###

O elemento de dados consiste em Tag do elemento de dados, Comprimento do valor e valor para o Elemento de dados. Existem 5 tipos de elementos de dados, ou seja, elementos de dados obrigatórios tipo 1, elementos de dados condicionais tipo 1C, elementos de dados obrigatórios tipo 2, elementos de dados condicionais tipo 2C e elementos de dados opcionais tipo 3. Básico Três tipos de estruturas de elementos de dados são os seguintes.

**Elemento de dados com VR explícito**

|Número do grupo|Número do elemento|Representação do valor|Reservado|Tamanho do valor|Campo do valor
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|"Value Length Bytes"

**Elemento de dados com VR explícito**

|Número do grupo|Número do elemento|Representação do valor|Comprimento do valor|Campo do valor
---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes|"Value Length Bytes"

**Elemento de dados com RV implícita**


|Número do grupo|Número do elemento|Comprimento do valor|Campo de valor
---|---|---|---|
|2 Bytes|2 Bytes|4 Bytes|"Value Length Bytes"

1. **Etiqueta de elemento de dados**: um número inteiro ordenado que representa o número do grupo e o número do elemento
1. **Representação de Valor VR**: VR é uma cadeia de caracteres que representa o VR do Elemento de dados.
1. **Value Length**: o inteiro sem sinal representa o comprimento explícito do campo de valor.
1. **Value Field**: Descreve os valores dos elementos de dados.

## Sintaxe de transferência ##

A sintaxe de transferência é um conjunto de regras para codificação para representar sem ambiguidade sintaxes mais abstratas. Com a ajuda da sintaxe de transferência, as entidades de comunicação negociam as técnicas de codificação comuns que elas suportam.

## POPs ##

A união de IOD e DIMSE define uma classe SOP. A definição de Classe SOP contém as regras e semânticas que podem restringir o uso dos serviços no Grupo de Serviços DIMSE ou os Atributos do IOD. Exemplos de elementos de serviço são armazenar, obter, localizar, mover, etc. Exemplos de objetos são imagens de TC, imagens de RM, mas também incluem listas de agendamento, filas de impressão, etc.

## Serviços ##

A DICOM fornece vários serviços, principalmente relacionados à comunicação de dados. Cada um deles é brevemente descrito a seguir:


**Store:** o serviço DICOM Store envia imagens ou outros objetos para um sistema de arquivamento e comunicação de imagens (PACS) ou servidor.


**Compromisso de armazenamento:** o serviço de compromisso de armazenamento é usado para confirmar que uma imagem foi armazenada permanentemente no dispositivo em qualquer tipo de mídia.


**Consulta/recuperação:** esse serviço permite que uma estação de trabalho encontre as listas de imagens ou outros objetos e, em seguida, recupere-os do PACS.


**Lista de trabalho de modalidade:** o serviço de lista de trabalho de modalidade fornece uma lista de procedimentos de imagem que foram programados para execução por um dispositivo de aquisição de imagem.


**Imprimir:** Este serviço envia imagens para a impressora.

## Números de porta sobre IP ##

O DICOM usa as seguintes portas TCP e UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Referências ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

