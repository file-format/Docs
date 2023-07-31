{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Script de Recurso Compilado C++",
  "description":"Saiba mais sobre o formato de arquivo RES com exemplo de RES e APIs que podem criar e abrir arquivos RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo RES?
O arquivo com sufixo ou extensão .res pode pertencer a várias categorias de formato de arquivo. Aqui estamos discutindo o formato de arquivo RES que é um Script de Recurso Compilado em C++; um arquivo binário criado pelo Microsoft Resource Compiler (rc) que contém dados de recursos; com base no conteúdo do arquivo de definição de recurso; relevantes para seu projeto de software pai. O arquivo .res geralmente é reformatado em um arquivo de objeto de recurso para vinculá-lo ao arquivo executável de um aplicativo.

## Formato de arquivo RES
O formato de arquivo RES pertence ao Microsoft Resource Compiler (rc). O compilador de recursos é uma ferramenta que compila recursos como cursores, ícones, menus e caixas de diálogo que seu aplicativo usa. Os arquivos de recursos geralmente possuem uma extensão .res; contém recursos, como cursores, imagens e informações de versão. Um arquivo RES pode ser um arquivo de recurso de 16 ou 32 bits.
## Estrutura do arquivo de recurso
Um arquivo de recurso contém uma série de várias entradas de recursos. Cada entrada contém um cabeçalho de recurso e dados relevantes. Um cabeçalho de recurso geralmente é alinhado com DWORD no arquivo e contém o seguinte:

- Um **DWORD** para especificar o tamanho do cabeçalho do recurso
- Um **DWORD** para especificar o tamanho dos dados do recurso
- O tipo de recurso
- O nome do recurso
- Informações de recursos adicionais

A estrutura do cabeçalho do recurso define o formato do arquivo RES. Os dados do recurso seguem o cabeçalho do recurso. Alguns recursos também adicionam um padrão de cabeçalho de grupo específico do recurso para fornecer informações sobre um grupo de recursos. A seguir estão alguns dos tipos de entrada de recursos e sua descrição:

### Recursos da tabela do acelerador
Uma tabela aceleradora é uma entrada de recurso em um arquivo RES sem um cabeçalho de grupo. O padrão **ACCELTABLEENTRY** define cada entrada na tabela do acelerador. Um arquivo RES pode ter várias tabelas aceleradoras.

### Recursos de cursores e ícones
Embora, o sistema considere cada ícone e cursor como um único arquivo, mas estes são armazenados em arquivos RES como um grupo de recursos de ícone ou um grupo de recursos de cursor. Os formatos de arquivo dos recursos de ícone e cursor são os mesmos. Um cabeçalho de grupo de recursos segue todos os componentes individuais de ícone ou grupo de cursores no arquivo .res.

### Recursos da caixa de diálogo
Uma caixa de diálogo também é realizada como uma entrada de recurso no arquivo RES. Ele contém um padrão de cabeçalho de caixa de diálogo **DLGTEMPLATE** e um padrão **DLGITEMTEMPLATE** para cada controle específico na caixa de diálogo. Os padrões **DLGTEMPLATEEX** e **DLGITEMTEMPLATEEX** explicam o formato dos recursos da caixa de diálogo estendida.

### Recursos de fonte
Um recurso de menu contém um padrão **MENUHEADER** subsequentemente um ou mais padrões **NORMALMENUITEM** ou **POPUPMENUITEM**, um para cada item de menu no modelo de menu. Os padrões **MENUEX_TEMPLATE_HEADER** e **MENUEX_TEMPLATE_ITEM** explicam o formato dos recursos de menu estendidos.

### Recursos da tabela de mensagens
Uma tabela de mensagens consiste em texto formatado para exibição como uma mensagem de erro ou em uma caixa de mensagem. O padrão principal em um recurso de tabela de mensagens é a estrutura **MESSAGE_RESOURCE_DATA**.

### Recursos de versão
O padrão principal em um recurso de versão é o **VS_FIXEDFILEINFO**. Padrões adicionais incluem **VarFileInfo** para armazenar dados relacionados a informações de idioma e **StringFileInfo** para informações de string personalizadas.




## Referências

* [Formatos de arquivo de recurso](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



