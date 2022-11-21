{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo de backup de dados de jogos do Steam CSD e APIs.",
  "title" :"Formato de arquivo CSD - Arquivo de backup de dados do jogo Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## O que é um arquivo CSD?

Um arquivo CSD é um arquivo de backup de jogo gerado pelo serviço de jogos **Steam** que permite aos usuários baixar e gerenciar jogos da **Valve**. Ele contém os dados de backup relacionados aos jogos que podem ser usados para restaurar um jogo excluído. O Steam só pode restaurar o jogo de um arquivo CSD se o jogo tiver sido baixado, instalado e corrigido pelo Steam. Para restaurar o jogo do arquivo CSD, use a opção Steam → Backup and Restore Gamesteam e selecione o arquivo.

## Formato de arquivo CSD - Mais informações

A estrutura interna do formato de arquivo CSD não está disponível publicamente e suas especificações de formato de arquivo não estão disponíveis para referência do desenvolvedor. Os arquivos CSD são acompanhados pelos arquivos CSM e ISS, que também são formatos de arquivo do jogo Steam.

### Onde encontrar arquivos de backup do Steam?

Todos os arquivos de backup do Steam podem ser encontrados nos seguintes locais:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \:
* \cfg\ - Configurações personalizadas e scripts de configuração
* \downloads\ - Conteúdo personalizado para jogos multiplayer
* \maps\ - Mapas personalizados que foram instalados ou baixados durante jogos multiplayer
* \materiais\ - Texturas e skins personalizadas
* \SAVE\ - Jogos salvos para um jogador

No entanto, a localização dos jogos criados por terceiros pode ser diferente e é determinada pelo desenvolvedor do jogo.

### Restaurando do arquivo de backup CSD

Instale o Steam e faça login na conta Steam correta (consulte Instalando o Steam para obter mais instruções)
* Inicie o Steam
* Clique em "Steam" no canto superior esquerdo do aplicativo Steam
* Selecione "Fazer backup e restaurar jogos..."
* Selecione "Restaurar um backup anterior"
* Navegue até o local dos arquivos de backup do jogo
* Continue pelas janelas do Steam para instalar os jogos necessários.

## Referências

* [Usando o recurso Steam Backup](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

