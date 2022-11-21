{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo PYC e APIs que podem criar e abrir arquivos PYC.",
  "title" :"PYC File Format - Python Compiled File",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## O que é um arquivo PYC?

Um arquivo PYC é um arquivo de saída compilado gerado a partir do código-fonte escrito na linguagem de programação Python. Quando o arquivo PY é executado usando o interpretador Python, ele é convertido em bytecode para execução. Ao mesmo tempo, o bytecode compilado também é salvo como arquivo .pyc para reutilização do cache posteriormente, se aplicável.

## Estrutura do formato de arquivo PYC

Os arquivos PYC estão em bytecode e suas especificações de formato de arquivo não estão disponíveis publicamente. No entanto, a investigação de algumas fontes mostra que a [estrutura de um arquivo PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshaled%20code%20object.) consiste em:

* `Um número mágico de quatro bytes`r - Simplesmente dois bytes que mudam com cada alteração no código de empacotamento e, em seguida, dois bytes de 0d0a.
* `Um carimbo de data/hora de modificação de quatro bytes` - carimbo de data/hora de modificação Unix do arquivo de origem que gerou o .pyc, para que possa ser recompilado se a origem for alterada.
* `Um objeto de código empacotado` - a saída de marshal.dump do objeto de código que é resultado da compilação do arquivo de origem.

## Referências

* [A estrutura dos arquivos .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshaled%20code%20object.)

