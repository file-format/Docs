{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo HDMP - Formato de arquivo de despejo de heap do Windows",
  "description":"Saiba mais sobre o formato de arquivo HDMP e APIs que podem criar e abrir arquivos HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## O que é um arquivo HDMP?

O arquivo HDMP é um despejo de memória não compactado quando um aplicativo ou programa trava devido a um erro. Ele é criado apenas pelo Windows XP/Vista e contém um dump do status do aplicativo quando ele foi travado. Sendo descompactados, os arquivos HDMP ocupam mais espaço no disco em comparação com os arquivos Minidump [MDMP](/pt/system/mdmp/) que são compactados para fins de relatório.

Os aplicativos que podem ser usados para **abrir** ou analisar arquivos HDMP incluem o Microsoft Visual Studio com ferramentas de depuração para Windows.

## Formato de arquivo HDMP

Os arquivos HDMP são armazenados em disco como arquivos binários e não oferecem nenhum benefício se abertos sem os aplicativos apropriados. Eles contêm dados relevantes do sistema registrados quando o erro ocorreu.

### Diferença entre os formatos de arquivo HDMP e MDMP

HDMP são arquivos de despejo de memória não compactados. Por outro lado, MDMP são arquivos de mini despejo compactados para redução no tamanho do arquivo e enviados à Microsoft para relatar o problema.

## Referência ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

