{
  "date" : "2021-06-30",
  "keywords" :[ "arquivo mst", "formato de arquivo mst", "o que é um arquivo mst", "arquivo", "exemplo mst", "extensão de arquivo mst", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo MST e APIs que podem criar e abrir arquivos MST.",
  "title" :"MST - Arquivo de pacote do Windows Installer",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## O que é um arquivo MST?
Os arquivos com extensão .mst são usados para transformar o conteúdo de um pacote MSI. Eles são comumente usados por administradores de sistema para aplicar as configurações personalizadas a um arquivo MSI existente. Os arquivos MST são usados junto com o pacote MSI original em seus sistemas de distribuição de software, como políticas de grupo. Os arquivos MST geralmente são usados no desenvolvimento e teste de software para configurar suas versões em desenvolvimento do software.

## Formato de arquivo MST
Um arquivo MST ou Transform é usado para coletar as opções de instalação para programas que usam o Microsoft Windows Installer em um arquivo. Esses arquivos são comumente usados na linha de comando do Instalador (MSIEXEC.EXE) ou em uma Diretiva de Grupo de instalação de software; em um domínio do Microsoft Active Directory. Os arquivos MST também podem ser usados com instaladores executáveis agrupados. Um caso geral é que alguém deseja passar parâmetros de linha de comando para o instalador encapsulado. Para fazer isso, você precisa de um arquivo MST que adicione a propriedade WRAPPED_ARGUMENTS à tabela de propriedades. Esses arquivos não podem ser criados ou editados usando editores gerais. Ferramentas específicas estão disponíveis para este fim.

### Como usar arquivos MST?
Os arquivos MST podem ser gerados usando várias ferramentas e o Ocra geralmente é usado para gerar arquivos MST. Em seguida, as configurações podem ser personalizadas de acordo com a necessidade e salvá-las em um local específico. Depois disso, os arquivos MST podem ser usados em conjunto com os arquivos MSI. Se você quiser testar esses arquivos; use a seguinte sintaxe na linha de comando

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Propriedade TRANSFORMS

Você também pode usar a propriedade **TRANSFORMS** do instalador do Windows, que na verdade é uma lista das transformações que o instalador aplica ao instalar o pacote. O instalador executa as transformações na mesma ordem em que estão listadas na propriedade TRANSFORM. As transformações podem ser especificadas por nome de arquivo com extensão .mst ou caminho completo. Para especificar mais de uma transformação, separe cada nome de arquivo ou um ponto e vírgula como no exemplo a seguir.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referências

* [Arquivos de transformação do MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [propriedade TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


