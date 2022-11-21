{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo emf", "formato de arquivo emf", "o que é um arquivo emf", "arquivo", "exemplo emf", "extensão de arquivo emf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Formato de Metafile Aprimorado",
  "description":"Saiba mais sobre o formato de arquivo EMF e APIs que podem criar e abrir arquivos EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo EMF?

**Formato de metarquivo aprimorado (EMF)** armazena imagens gráficas independentemente do dispositivo. Os metarquivos de EMF são compostos por registros de comprimento variável em ordem cronológica que podem renderizar a imagem armazenada após a análise em qualquer dispositivo de saída. Esses registros de comprimento variável podem ser definições de objetos incluídos, comandos para desenho e propriedades gráficas essenciais para renderizar a imagem com precisão. Quando um dispositivo abre um metarquivo EMF usando seu próprio ambiente gráfico, as proporções, dimensões, cores e outras propriedades gráficas da imagem original permanecem as mesmas, independentemente da plataforma do dispositivo de abertura.

## Breve história ##

Em 1990, a Microsoft projetou um formato de arquivo de imagem Windows Metafile ([WMF](/pt/image/wmf/)) para o Microsoft Windows. Os Meta-arquivos do Windows são formatos de 16 bits que podem conter alguns componentes de bitmap. O WMF pode consistir em gráficos vetoriais e destina-se a manter a portabilidade entre diferentes aplicativos. Em 1993, o Win32/GDI anunciou o Enhanced Metafile (EMF), uma versão mais recente com maior flexibilidade e escalabilidade. O EMF também é usado como comandos de linguagem gráfica para executar os drivers da impressora. A Microsoft agora recomenda o formato de metarquivo avançado (EMF) sobre o formato Windows (WMF). Quando o Windows XP foi introduzido, a versão Enhanced Metafile Format Plus (EMF+) foi lançada. Esta versão mais recente encontra seu caminho ao serializar chamadas de API GDI+, da mesma forma que WMF/EMF grava chamadas para GDI. Existe uma versão compactada com gzip do EMF conhecida como EMZ.

## Formato de metarquivo EMF ##

A seguir estão os elementos essenciais do formato de metarquivo aprimorado:

* Um EMR_HEADER (versão, tamanho, resolução da imagem na criação)
* Uma tabela para objetos GDI
* Uma paleta reservada (opcional)
* Registros de metarquivo organizados em estrutura de matriz (configurações de propriedades, objetos definidos, comandos de desenho)
* Registro EMR_EOF (último registro no metarquivo EMF)

## Versões EMF ##
* **Original**: A versão original especifica o registro necessário para manter a imagem original e manter seu dispositivo independente. Além disso suporta o registro contendo objetos gráficos e comandos para desenho.
* **Versão 1**: A segunda versão do EMF melhorou a flexibilidade e a independência do dispositivo adicionando o registro para o formato de pixel e a provisão para usar o comando OpenGL.
* **Versão 2**: A terceira versão aprimorou a precisão adicionando o sistema Metric para medir as distâncias da superfície do dispositivo, deixando o registro mais escalável.

## Registros de metarquivo aprimorados ##

Os registros de metarquivo são organizados na forma de matriz. Esses registros possuem estrutura ENHMETARECORD e comprimento variável. ENHMETARECORD especifica dados que definem funções GDI para criar uma imagem usando o formato de metarquivo aprimorado. A estrutura **ENHMETHEADER** é sempre o primeiro registro neste formato. Este cabeçalho EMF contém as seguintes informações.

Cada registro de metarquivo aprimorado tem dois membros do EMR (fornece a estrutura base) no início. O primeiro membro reconhece a função GDI (os parâmetros são usados no registro) que determina o tipo de registro e é conhecido como iType. O outro membro nSize define o tamanho de cada registro. Parâmetros restantes (se houver) e dados adicionais organizados imediatamente abaixo de nSize. Imediatamente após o cabeçalho, uma descrição de texto opcional pode apresentar. O nome da foto e do autor é registrado nessa descrição do texto. A paleta cuja presença é uma opção especifica as cores usadas na criação aprimorada de metarquivo. Os outros registros usados para especificar a função GDI que é essencial na criação de imagens.

Pelo menos um registro EMF deve estar presente em cada metarquivo. As informações de passagem de um registro para outro dependem dos registros EMF, portanto, esses registros devem ser organizados de forma adjacente. Em qualquer registro no metarquivo, exceto EOF_record, o comprimento desse registro específico define para mover para o próximo registro.

## Criação aprimorada de metarquivo ##

A função **CreateEnhMetaFile** é usada para criar um metarquivo aprimorado. Os argumentos desta função são usados para dimensões e armazenamento de imagem em disco/memória. Além disso, esta função requer a dimensão do dispositivo em que a imagem apareceu primeiro (dispositivo referenciado) e o contexto do dispositivo de referência (DC). Portanto, os argumentos para lidar com esse DC devem fornecer ao chamar a função **CreateEnhMetaFile**. A sintaxe da função é a seguinte:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** identificador para um dispositivo de referência.

**lptoFilename:** um ponteiro para o nome do arquivo.

**lprc:** O ponteiro para a estrutura oval especifica as dimensões da imagem em mm.

**lpDesc:** um ponteiro para uma string para o título da imagem e o nome do aplicativo que criou a imagem.

## Operações de metarquivo aprimoradas ##

A seguir estão os trabalhos que podem ser realizados usando o identificador para um metarquivo aprimorado.

* Exiba e edite a imagem armazenada.
* Produza cópias de metarquivo aprimoradas.
* Recupere a cópia de um cabeçalho EMF, descrição opcional e versão binária de um metarquivo aprimorado
* Recapitule as cores na paleta.

## Objetos gráficos ##

Nas operações de desenho e pintura, os objetos gráficos podem ser criados por registros de criação de objetos e podem ser salvos para uso posterior. Um registro `EMR_SELECTOBJECT` pode recuperar esses objetos gráficos usando o contexto do dispositivo de reprodução. Canetas, paletas, pincéis, espaços de cores, fontes e objetos de estoque são alguns tipos de objetos reutilizáveis.

## Ordenação de bytes ##

O formato Little-endian é usado para armazenar dados em registros de metarquivo.

## Versão ##

O formato de arquivo EMF foi revisado duas vezes. As versões alteradas são originais, extensão 1 e extensão 2. As versões estendidas têm provisão para registros OpenGL e um descritor opcional para formato de pixel interno. Uma facilidade de medição em mililitros é adicionada para as dimensões exibidas.

## Referências ##

* [Metarquivos de formato aprimorado | Documentos da Microsoft](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Formato e especificação de metarquivo aprimorados](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

