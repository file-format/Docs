{
  "date" : "2020-01-11",
  "keywords" :[ "arquivo x", "formato de arquivo x", "o que é um arquivo x", "arquivo", "exemplo x", "extensão de arquivo x", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Formato de arquivo DirectX 2.0",
  "description":"Saiba mais sobre o formato de arquivo DirectX X e APIs que podem abrir e criar arquivos DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## O que é um arquivo X?

Um arquivo com extensão .x refere-se ao formato de arquivo legado [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics que foi introduzido com o Microsoft DirectX 2.0. Ele foi usado para renderização de gráficos 3D em jogos e especifica as estruturas para malhas, texturas, animações e objetos definidos pelo usuário. Ele foi preterido desde 2014, pois o formato de arquivo Autodesk FBX funciona melhor como um formato mais moderno. O X é orientado a modelos e está livre de qualquer conhecimento de uso.

Você pode abrir arquivos DirectX X usando o Microsoft DirectX e editores de texto comuns.

## Formato de arquivo X

A [referência do arquivo X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) contém informações de referência para os elementos da API que são usados para trabalhar com arquivos DirectX .x. O formato fornece primitivas de dados de baixo nível que são usadas por outros aplicativos para definir primitivas de nível superior por meio de modelos de dados. O DirectX 6.0 introduziu interfaces e métodos que permitem ler e gravar em arquivos .x. O DirectX 3.0 introduziu uma versão binária desse formato de arquivo.

A [referência de formato de arquivo X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) definida pelo DirectX 9 contém informações de referência para .x arquivos em binário, bem como codificações de texto.

### Codificação Binária

O [formato binário](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) define o formato DirectX X como uma representação tokenizada do formato de texto. Esses tokens podem ser autônomos para fornecer estrutura gramatical ou podem ser tokens de registro que fornecem os dados necessários.

#### Cabeçalho

O cabeçalho binário pode ser lido e escrito usando as seguintes definições.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Codificação de Texto

Os arquivos DirectX .x não dependem da forma como o arquivo é usado e não são específicos de nenhum aplicativo. Essa abordagem orientada a modelos permite que o formato de arquivo .x seja usado por qualquer aplicativo cliente.


#### Cabeçalho

O cabeçalho de comprimento variável é obrigatório e deve estar no início do fluxo de dados. O cabeçalho contém os seguintes dados.

|Tipo |Subtipo |Tamanho |Conteúdo |Significado do conteúdo|
---|---|---|---|---|
|Número Mágico (obrigatório)| | 4 bytes |xof |
|Número da versão (obrigatório) |Número principal |2 bytes |03 |Versão principal 3|
| |Número secundário |2 bytes |02 |Versão secundária 2|
|Tipo de formato (obrigatório)| |4 bytes |"txt" |Arquivo de texto|
| | | |"compartimento"| Arquivo Binário|
| | | |"tzip"| Arquivo de texto compactado MSZip|
| | | |"bzip"| Arquivo binário compactado MSZip|
|Tamanho do flutuador (obrigatório)| |4 bytes| 0064| flutuadores de 64 bits|
| | | |0032 |Floats de 32 bits|


## Referências

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Referência de formato de arquivo do DirectX 9](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

