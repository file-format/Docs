{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo AML - Arquivo de linguagem de máquina ACPI",
  "description":"Saiba mais sobre o formato de arquivo ACPI AML e APIs que podem criar e abrir arquivos AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## O que é um arquivo AML?

Um arquivo AML é um arquivo de sistema criado com a linguagem ACPI (Advanced Configuration and Power Interface) usada para configurar as propriedades de hardware. Ele contém código de byte independente da máquina que é usado para configurar o hardware mesmo para operações simples, como desligar um computador. Os arquivos AML podem conter instruções dependendo da finalidade para a qual serão instalados na máquina. A implementação dos padrões ACPI permite aprimorar a funcionalidade de gerenciamento de energia e uma interface robusta para configurar dispositivos da placa-mãe, como as placas-mãe P55.

## Formato de arquivo ACPI AML

Os arquivos AML são salvos como arquivos binários em disco com conteúdo escrito em código de byte. As especificações de formato de arquivo do padrão ACPI estão disponíveis em [uefi](https://uefi.org/). A linguagem foi projetada para oferecer estabilidade e compatibilidade com versões anteriores, exigindo menos reescritas ou reconstruções da pilha de aplicativos.

## Especificações de formato de arquivo AML

Um arquivo AML é composto por tabelas DSDT e SSDT. O código de byte AML é lido e analisado desde o início de cada uma dessas tabelas. Isso fornece informações sobre as definições de dispositivos e objetos no namespace ACPI. Usando essas informações, o interpretador AML pode gerar uma lista de todos os dispositivos disponíveis no sistema e suas propriedades e funções suportadas.

### Exemplo de código ASL para um DSDT

Um exemplo de código ASL para um DSDT é o seguinte.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Referências

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

