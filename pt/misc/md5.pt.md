{
  "date" : "2021-07-29",
  "keywords" :[ "arquivo md5", "formato de arquivo md5", "o que é um arquivo md5", "arquivo", "exemplo md5", "extensão de arquivo md5","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Arquivo de soma de verificação MD5",
  "description":"Saiba mais sobre o arquivo MD5 e APIs que podem criar e abrir arquivos MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## O que é um arquivo MD5?

Um arquivo MD5 é um arquivo de soma de verificação usado para verificar a integridade de um arquivo. É semelhante a uma impressão digital para o arquivo associado e é gerado exclusivamente usando um algoritmo que usa o número de bits no arquivo. Ele é usado para verificar o arquivo com software como [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Uma vantagem de usar arquivos MD5 é verificar se os arquivos baixados não estão corrompidos.

## Formato de arquivo MD5 - Mais informações

Normalmente, um arquivo MD5 é salvo com o mesmo nome do arquivo original, mas com a extensão .md5. Por exemplo, se o nome do arquivo associado for `abc_987_123456.grb`, o nome do arquivo MD5 correspondente será `abc_987_123456.grb.md5`. Os arquivos MD5 ajudam a identificar que um arquivo recebido ou baixado não está corrompido ou afetado por conteúdo malicioso. Em suma, os arquivos MD5 garantem a integridade de um arquivo.


## Como verificar a soma de verificação MD5?

Um único arquivo pode ser verificado/verificado para MD5 usando a ferramenta [md5sum](https://en.wikipedia.org/wiki/Md5sum) como segue.

```
md5sum -c abc_987_123456.grb.md5
```

## Referências

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

