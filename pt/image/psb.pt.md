{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo psb", "formato de arquivo psb", "o que é um arquivo psb", "arquivo", "exemplo psb", "extensão de arquivo psb", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Formato de arquivo de imagem grande do Photoshop",
  "description":"Saiba mais sobre o formato de arquivo PSB e APIs que podem criar e abrir arquivos PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PSB?
Adobe photoshop salva arquivos em dois formatos. Arquivos com tamanho de 30.000 por 30.000 pixels são salvos com extensão PSD e arquivos maiores que PSD até 300.000 por 300.000 pixels são salvos com extensão PSB conhecida como “Photoshop Big”. Mais especificamente, os arquivos PSB podem ter até 4 EB (mais de 4,2 bilhões de GB) com imagens com altura e largura de até 300.000 pixels. Os PSDs, por outro lado, podem ter no máximo até 2 GB e dimensões de imagem de 30.000 pixels.

PSB também é conhecido como tamanho de grande formato para photoshop e suporta todos os recursos do photoshop como camadas, efeitos e filtros.Photoshop pode converter arquivos PSB para [PSD](/pt/image/psd/), [JPG](/pt/image/jpeg/) , [PNG](/pt/image/png/), [EPS](/pt/page-description-language/eps/), [GIF](/pt/image/gif/) e outros formatos também. O formato de documento grande do Photoshop está disponível quando o recurso do painel de manipulação de arquivos da caixa de diálogo de preferências do Photoshop é ativado.

## Informações de formato de arquivo ##

O formato de arquivo do Photoshop é dividido em cinco partes principais com muitos marcadores de comprimento para mover entre as seções.

|Formato de arquivo
---|
|Cabeçalho do arquivo
|Dados do modo de cor
| Recursos de imagem
|Informações sobre Camadas e Máscaras
|((((
Dados de imagem
)))

### Cabeçalho do arquivo ###

O cabeçalho do arquivo tem comprimento fixo de 26 bytes e contém as propriedades básicas da imagem.

Assinatura BYTE [4] – Igual a '8BPS'.

Versão WORD [2] – Número da versão, PSD # 1, PSB # 2.

BYTE Reservado [6] – Reservado e sempre zero.

Canais WORD [2] – Número de canais de cores na imagem, incluindo canais alfa. Seu valor varia de 1 a 56.

LONG Rows [4] – Altura da imagem em pixels, PSD 1-30.000, PSB 1-300.000.

Colunas LONG [4] – Largura da imagem em pixels, PSD 1-30.000, PSB 1-300.000.

WORD Depth [2] – Número de bits por canal. Os valores suportados são 1,8,16 e 32.

Modo WORD [2] – Modo de cor do arquivo.

#### Descrição do modo ####


|Modo|Descrição
---|---|
|0|Bitmap (monocromático)
|1|Escala de cinza
|2|Indexado
|3|RGB
|4|CMYK
|7|Multicanal
|8|Duotônico (meio-tom)
|9|Laboratório

### Dados do modo de cor ###

Após a seção do cabeçalho do arquivo, segue a seção de dados do modo de cor. O bloco começa com um número LONG que fornece o comprimento do bloco em bytes. A estrutura dos dados do modo de cor é a seguinte:

4 bytes – O comprimento dos seguintes dados de cor.

Variável - Dados de cor

Se o valor do campo de modo na seção de cabeçalho não for Indexed Color ou duotone, o comprimento do bloco será 0 e não haverá dados após o campo de comprimento.

Para imagens coloridas indexadas, o comprimento será de 768 bytes, que conterá uma paleta de 256 cores. Para duotone, os dados conterão parâmetros de tela e outras informações relacionadas.

### Recursos de imagem ###

Seguindo a seção de dados do modo de cor, o terceiro bloco é a seção de recursos de imagem. Os primeiros quatro bytes são um número LONG que especifica o comprimento do bloco seguido por uma série de blocos de recursos. A estrutura do bloco de recursos de imagem é a seguinte:

Tipo BYTE [4] - Assinatura '8BIM'

WORD ID [2] – ID do recurso de imagem. Há uma lista de IDs de recursos que pode ser vista no link de referência.

BYTE Name [Variável] – Nome: Pascal String com comprimento par. ** **

LONG Size [4] – Tamanho real dos dados de recursos que se seguem.

Dados BYTE [Variável} – Dados do recurso. É acolchoado para fazer o mesmo tamanho.

Alguns dos formatos de recursos são explicados brevemente abaixo:

**Formato de recurso de grade e guias:** informações de grade e guias são armazenadas no bloco de recursos. Esses blocos de recursos contêm uma grade de 16 bytes e um cabeçalho de guia seguido por blocos de 5 bytes de informações de guia.

**Thumbnail Resource Format:** as informações de miniatura são armazenadas no bloco de recursos de imagem para exibição de visualização, que consiste em um cabeçalho de 28 bytes e uma miniatura JFIF em RGB.

**Formato de recurso de amostradores de cores:** informações de amostradores de cores são armazenadas no bloco de recursos de imagem com um cabeçalho de 8 bytes seguido por um bloco de comprimento variável de informações de amostradores de cores.

### Informações sobre Camadas e Máscaras ###

O quarto bloco é o bloco de informações de camada e máscara e contém informações sobre as camadas e máscaras. As informações de camada são armazenadas primeiro e, em seguida, as informações de máscara.

**Informações da camada:** as informações da camada começam com um valor LONG que mostra o comprimento das informações da camada. Depois disso, há a contagem do valor WORD que mostra o número de registros de camada a seguir.

[8] – comprimento das camadas

[2] – Contagem de Camadas

[Variável] – Informações sobre cada camada.

[Variável] – Dados de imagem do canal.** **

**Informações da máscara:** A estrutura da máscara tem o seguinte formato:


|Estrutura de dados|Nome do campo| Descrição
---|---|---|
|PALAVRA| Espaço de cores de sobreposição| (Não documentado)
|BYTE[8]| Componentes de cor| Componentes de cor de 4x2 bytes
|PALAVRA| Opacidade| 0#transparente, 1#opaco
|BYTE| Tipo| 0#invertido, 1#protegido, 128#usar valor armazenado
|BYTE| preenchimento | definido como zero

### Dados de imagem ###

A última seção contém os dados de pixel da imagem. Os dados da imagem são armazenados como uma série de sequências em planos, ou seja, primeiro todos os dados vermelhos, depois todos os dados verdes, etc. WORD no início de cada linha mostra o tamanho em bytes relacionado a cada linha de varredura.

[2] – Método de compressão:

[Variável] – Dados de imagem em ordem planar, ou seja, RRRR, GGGG, BBBB etc.

Métodos de compressão:

0 – Raw Dados de imagem

1 – RLE Comprimido

2 – Zip sem previsão

3 – Zip com previsão

## Referência ##

* [Formato de arquivo PSB - Por Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

