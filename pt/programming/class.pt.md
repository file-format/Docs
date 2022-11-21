{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","o que é um arquivo de classe","como abrir um arquivo de classe", "extensão", "arquivo", "arquivo de classe","formato de arquivo de classe", "extensão .class ", "arquivo de classe em java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Classe - Formato de arquivo de classe Java",
  "description":"Saiba mais sobre o formato de arquivo de classe e APIs que podem criar e abrir arquivos de classe.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo de classe?

Um **arquivo de classe em Java** é a saída compilada da classe [.java](/pt/programming/java/) que é realmente executada por uma Java Virtual Machine (JVM). Arquivos de classe podem ser executados individualmente, bem como podem fazer parte de um arquivo [JAR](/pt/programming/jar/) como um pacote junto com outros arquivos de pacote. Eles podem ser criados usando o comando **`javac`** da interface de linha de comando. Alguns IDEs Java como [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) e NetBeans fornecem arquivos de saída create .class do Java do projeto arquivos.

## Formato de arquivo de classe

Um arquivo de classe Java é composto por bytecode que é um código intermediário a ser executado pela JVM. Um arquivo de classe consiste em um fluxo de bytes de 8 bits e os itens de dados multibyte são sempre armazenados em ordem big-endian.

### Estrutura ClassFile

A estrutura do arquivo de classe é mostrada abaixo.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
Onde:

* u1 = quantidade de um byte sem sinal
* u2 = quantidade de dois bytes sem sinal
* u4 = quantidade de quatro bytes sem sinal

Detalhes da estrutura do arquivo .class bem explicados no Oracle [formato de arquivo de classe](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) e podem ser consultados por desenvolvedores para referência. Um resumo desses campos é o seguinte.

* `magic` - O item mágico fornece o número mágico que identifica o formato do arquivo da classe; tem o valor 0xCAFEBABE.
* `minor_version`, `major_version` - Os valores dos itens minor_version e major_version são os números de versão secundária e principal deste arquivo de classe.
* `constant_pool_count` - O valor do item constant_pool_count é igual ao número de entradas na tabela constant_pool mais um. Um índice constant_pool é considerado válido se for maior que zero e menor que constant_pool_count, com exceção de constantes do tipo long e double.
* `constant_pool[]` - O constant_pool é uma tabela de estruturas (§4.4) representando várias constantes de string, nomes de classe e interface, nomes de campo e outras constantes que são referidas na estrutura ClassFile e suas subestruturas. O formato de cada entrada da tabela constant_pool é indicado por seu primeiro byte "tag".
* `access_flags` - O valor do item access_flags é uma máscara de sinalizadores usados para denotar permissões de acesso e propriedades desta classe ou interface.
* `this_class` - O valor do item this_class deve ser um índice válido na tabela constant_pool.
* `super_class` - Para uma classe, o valor do item super_class deve ser zero ou deve ser um índice válido na tabela constant_pool.
* `interfaces_count` - O valor do item interfaces_count fornece o número de superinterfaces diretas desta classe ou tipo de interface.
* `interfaces[]` - Cada valor no array interfaces deve ser um índice válido na tabela constant_pool.
* `fields_count` - O valor do item fields_count fornece o número de estruturas field_info na tabela de campos.
* `fields[]` - Cada valor na tabela de campos deve ser uma estrutura field_info fornecendo uma descrição completa de um campo nesta classe ou interface.
* `methods_count` - O valor do item method_count fornece o número de estruturas method_info na tabela de métodos.
* `methods[]` - Cada valor na tabela de métodos deve ser uma estrutura method_info fornecendo uma descrição completa de um método nesta classe ou interface. Se nenhum dos sinalizadores ACC_NATIVE e ACC_ABSTRACT estiver definido no item access_flags de uma estrutura method_info, as instruções da Java Virtual Machine que implementam o método também serão fornecidas.
* `attributes_count` - O valor do item attribute_count fornece o número de atributos (§4.7) na tabela de atributos desta classe.
* `attributes[]` - Cada valor da tabela de atributos deve ser uma estrutura attribute_info.




## Referências

* [O formato de arquivo da classe](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

