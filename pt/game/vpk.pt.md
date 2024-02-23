{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo VPK do Unreal Static Meshes e APIs que podem criar e abrir arquivos VPK.",
  "title" : "Arquivo VPK - Arquivo de malhas estáticas irreais",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-pt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## O que é um arquivo .VPK?

Um arquivo .vpk é um formato de arquivo usado pelo **Source Engine**, um mecanismo de jogo desenvolvido pela Valve Corporation. Os arquivos VPK são usados para empacotar o conteúdo do jogo, como modelos, texturas e sons, e são comumente usados em jogos como Team Fortress 2, Left 4 Dead e Counter-Strike: Global Offensive. Os arquivos podem ser abertos e extraídos usando uma variedade de ferramentas, como GCFScape e VPK Tool.

## Formato de arquivo VPK – Mais informações

Os arquivos VPK são armazenados no disco como arquivos binários. Um único arquivo vpk pode fazer parte de um pacote VPK ou pode atuar como um arquivo VPK bruto independente. As informações que podem ser armazenadas dentro de um arquivo VPK incluem mapas, materiais, conteúdo de jogo e cenas coreográficas.

### Como criar um arquivo VPK?

Existem várias maneiras de criar um arquivo .vpk, dependendo das ferramentas disponíveis.

1. `Usando a ferramenta VPK:` Esta é uma ferramenta de linha de comando que pode ser usada para criar e extrair arquivos VPK. Um arquivo VPK pode ser criado usando o seguinte comando:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Isso criará um arquivo VPK a partir do diretório especificado e o salvará como o arquivo de saída especificado.

1. `Usando o Hammer Editor:` O Hammer Editor é uma ferramenta incluída no Source SDK que pode ser usada para criar e editar níveis para jogos que usam o motor Source. Também inclui a capacidade de criar arquivos VPK, clicando com o botão direito em uma pasta na guia Sistema de arquivos e selecionando Criar VPK

1. `Usando o criador VPK da Valve:` Esta é uma ferramenta desenvolvida pela Valve que é usada para empacotar e distribuir conteúdo de jogos. Esta ferramenta pode ser usada para criar arquivos VPK e também é a ferramenta oficial para criar arquivos VPK.

## Referências

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [Recursos para desenvolvedores VPK](https://developer.valvesoftware.com/wiki/GCF)

