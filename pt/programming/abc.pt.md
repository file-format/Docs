
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - Arquivo de código de byte ActionScript",
  "description":"Aprenda sobre o que é o formato de arquivo ABC com exemplos e APIs que podem criar e abrir arquivos ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## O que é um arquivo ABC?

Um arquivo com extensão .abc é um arquivo de código de byte ActionScript criado pelo compilador Flash como resultado da compilação dos arquivos de script ActionScript. O byte code contido no arquivo ABC é executado pela ActionScript Virtual Machine (AVM e AVM2). O código de byte é composto por dados constantes, instruções do conjunto de instruções AVM2 e vários tipos de metadados. Quando um arquivo ABC é carregado no AVM ou AVM2, ele passa por verificação. Se não estiver em conformidade com a Visão geral do AVM2, será rejeitado. Os arquivos ABC podem ser abertos no Adobe Flash Player que foi descontinuado há muito tempo.

## Formato de arquivo ABC - Mais informações

Os arquivos ABC são salvos em disco em formato de arquivo binário que pode ser lido por máquinas virtuais AVM ou AVM2. Sua estrutura de arquivo interna representa o bloco de código executável com todos os seus dados constantes, descritores de tipo, código e metadados.

## Estrutura do arquivo ABC

A estrutura do arquivo ABC é mostrada abaixo.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Campos do arquivo ABC

|Nome do Campo|Descrição|
---|---|
|minor_version, major_version|Os valores de major_version e minor_version são os números de versão principal e secundária do formato abcFile.|
|constant_pool|O constant_pool é uma estrutura de comprimento variável composta de inteiros, doubles, strings, namespaces, namespace sets e multinames.|
|method_count, method|O valor demethod_count é o número de entradas na matriz de métodos. Cada entrada na matriz de métodos é uma estrutura method_info de comprimento variável.|
|metadata_count, metadata|O valor de metadata_count é o número de entradas na matriz de metadados. Cada entrada de metadados é uma metadata_infostructure que mapeia um nome para um conjunto de valores de string. |
|class_count, instance, class|O valor de class_count é o número de entradas nas matrizes de instância e classe. |
|script_count, script|O valor de script_count é o número de entradas na matriz de scripts. Cada entrada de script é uma estrutura script_info que define as características de um único script neste arquivo. |
|method_body_count, method_body|O valor de method_body_count é o número de entradas na matriz method_body. Cada method_bodyentry consiste em uma estrutura method_body_info de comprimento variável que contém as instruções para um método ou função individual.|

## Referências

* [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

