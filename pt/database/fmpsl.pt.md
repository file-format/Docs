{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo FMPSL e APIs que podem criar e abrir arquivos FMPSL.",
  "title" :"Formato de arquivo FMPSL - Arquivo de link de instantâneo do FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## O que é um arquivo FMPSL?

Um arquivo FMPSL é um arquivo de instantâneo do banco de dados criado com o FileMaker Pro 12. Ele armazena os resultados consultados do banco de dados junto com outras informações, como layout visual e informações visíveis. O arquivo FMPSL pode ser usado para restaurar todos esses dados em outra instância do banco de dados do FileMaker Pro. Esse formato de arquivo foi introduzido com o lançamento do FileMaker Pro v 12. Antes desta versão, os links de instantâneos foram introduzidos como formato de arquivo FPSL no FileMaker Pro v 11. Os arquivos FMPSL podem ser abertos com o software FileMaker Pro Advanced. Outros formatos de arquivo suportados pelo FileMaker Pro incluem [FP5](/pt/database/fp5/), [FP7](/pt/database/fp7/) e [FMP12](/pt/database/fmp12/).

## Formato de arquivo FMPSL

Os detalhes do formato de arquivo interno dos arquivos FMPSL não estão disponíveis publicamente para referência do desenvolvedor.

### Como salvar registros como arquivo FMPSL?

Os dados do banco de dados do FileMaker Pro podem ser salvos como arquivo de link de instantâneo usando as etapas a seguir.

1. Pesquise os registros do banco de dados que devem ser salvos como um arquivo de link de instantâneo.
1. Usando a opção Send Record As Snapshot Link do menu, salve o arquivo digitando um nome de arquivo.
1. Use os Registros pesquisados para salvar todo o conjunto de registros encontrado.

O arquivo de instantâneo gerado será salvo no disco com o nome especificado.

## Referências

* [Converter versões anteriores dos formatos de arquivo do FileMaker Pro para o formato de arquivo FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Salvar registros como um arquivo de link de instantâneo](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

