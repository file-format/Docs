{
  "date" : "2022-03-21",
  "keywords" :[ "arquivo xpr", "formato de arquivo xpr", "o que é um arquivo xpr", "arquivo", "exemplo xpr", "extensão de arquivo xpr", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo XPR - Arquivo gráfico do Microsoft Expression Design",
  "description":"Saiba mais sobre o formato de arquivo XPR e APIs que podem criar e abrir arquivos XPR.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## O que é um arquivo XPR?

Um arquivo XPR é um arquivo de imagem vetorial criado com o software Microsoft Expression Graphics (EGD) agora descontinuado. Ele contém informações gráficas que podem ser usadas como maquete da interface do usuário. Os arquivos XPR foram posteriormente substituídos por arquivos .design no Microsoft Expression Design. Os arquivos XPR podem ser abertos com o Microsoft Expression Studio, que foi descontinuado há algum tempo.

## Vulnerabilidade de formato de arquivo XPR

Os arquivos XPR foram identificados para beneficiar uma vulnerabilidade no Microsoft Expression Design, permitindo a execução de código remoto. No problema relatado, se um usuário abrisse um arquivo .xpr legítimo localizado no diretório de rede junto com o arquivo DLL (biblioteca de vínculo dinâmico), o Microsoft Expression Design poderia tentar carregar o arquivo DLL e executar o código contido nele. Isso foi corrigido posteriormente pela Microsoft em uma atualização de segurança.

## Referências

* [A vulnerabilidade no design da expressão pode permitir a execução remota de código (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

