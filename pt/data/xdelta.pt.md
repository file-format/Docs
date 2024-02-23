{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo XDELTA - Arquivo diferencial xdelta - O que é arquivo .xdelta e como abri-lo?",
  "description" : "Aprenda sobre o arquivo diferencial xdelta e como abri-lo.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-pt",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## O que é um arquivo .XDELTA?

O formato de arquivo XDELTA contém as diferenças binárias entre dois outros arquivos e é gerado pela ferramenta xdelta, um utilitário de linha de comando para codificação delta, que envolve calcular as diferenças entre dois arquivos e codificar essas diferenças em um formato compacto. Os arquivos XDELTA armazenam dados binários que representam alterações ou diferenças entre o arquivo original e o arquivo atualizado. Os dados binários em um arquivo XDELTA representam as alterações necessárias para transformar um arquivo (o original) em outro arquivo (a versão atualizada ou corrigida).

Os arquivos XDELTA são frequentemente usados na comunidade de jogos para distribuir modificações (mods) para videogames. Esses mods podem incluir desde mudanças cosméticas até alterações significativas na mecânica de jogo. Os arquivos XDELTA permitem que os usuários apliquem essas modificações às instalações do jogo, corrigindo os arquivos originais do jogo com as alterações especificadas no arquivo XDELTA.

## xdelta

`xdelta` é um utilitário de linha de comando usado para codificação e decodificação delta; é empregado principalmente para criar e aplicar patches binários, geralmente chamados de patches delta ou patches xdelta, entre dois arquivos; esses patches representam diferenças entre o arquivo original e a versão modificada ou atualizada, permitindo a distribuição eficiente de atualizações, principalmente em cenários onde a largura de banda ou o espaço de armazenamento são limitados.

Aqui está uma breve visão geral das principais funcionalidades do `xdelta`:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` é comumente usado em vários cenários, como distribuição de atualizações de software, correção de videogames e atualização de arquivos de sistema em dispositivos incorporados ou dispositivos de rede. Ele fornece uma maneira flexível e eficiente de gerenciar atualizações de arquivos, minimizando o uso de largura de banda e os requisitos de armazenamento.

## xdeltaui

xdeltaui é um aplicativo de interface gráfica do usuário (GUI) para gerenciar e aplicar patches XDELTA. xdelta gui fornece uma interface amigável para os usuários interagirem com os arquivos XDELTA e aplicá-los aos arquivos originais correspondentes, corrigindo-os ou atualizando-os de forma eficaz.

Ao contrário da versão de linha de comando do xdelta, que opera por meio de comandos baseados em texto, o xdeltaui oferece uma maneira mais intuitiva de lidar com arquivos XDELTA, especialmente para usuários que não estão familiarizados com interfaces de linha de comando ou preferem ferramentas gráficas.

Com o xdeltaui, os usuários normalmente podem executar tarefas como selecionar o arquivo original, selecionar o arquivo de patch XDELTA e aplicar o patch para gerar o arquivo atualizado. Isso pode ser particularmente útil para instalar mods ou atualizações para videogames ou outros aplicativos de software.

## Baixar xdelta

Em sistemas Linux, você pode usar gerenciadores de pacotes como `apt`, `yum` ou `dnf` para instalar o `xdelta`. Por exemplo, no Ubuntu, você pode usar o seguinte comando:

```
sudo apt-get install xdelta3
```

## Como usar o xdelta

Para usar `xdelta`, normalmente você precisa seguir estas etapas gerais:

1.  **Baixe e instale**: Primeiro, certifique-se de ter o `xdelta` instalado em seu sistema. Você pode baixá-lo de seu site oficial, gerenciadores de pacotes ou outras fontes confiáveis.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Criando um patch**:
    
- Abra sua interface de linha de comando (terminal ou prompt de comando).
- Use o comando `xdelta` com opções apropriadas para criar um patch. A sintaxe básica é:
               
```
xdelta delta<original_file><updated_file><patch_output_file>
```
        
Substitua `<original_file> ` com caminho para o arquivo original, `<updated_file> ` com caminho para o arquivo atualizado e `<patch_output_file> ` com o nome desejado para o arquivo de patch.
- Exemplo:
               
```
xdelta delta arquivo_original atualizado_arquivo patch.xdelta
```
        
4.  **Aplicando um patch**:
    
- Certifique-se de ter o arquivo original e o arquivo de patch disponíveis.
- Abra sua interface de linha de comando.
- Use o comando `xdelta` com opções apropriadas para aplicar o patch. A sintaxe básica é:
        
      
```
patch xdelta<original_file><patch_file><output_file>
```
        
Substitua `<original_file> ` com caminho para o arquivo original, `<patch_file> ` com o caminho para o arquivo de patch e `<output_file> ` com o nome desejado para o arquivo de saída.
- Exemplo:
                
```
patch xdelta arquivo_original patch.xdelta arquivo_atualizado
```
        
5.  **Visualizando Ajuda**: Se precisar de ajuda com opções ou comandos específicos, você pode usar o comando `xdelta` com a opção `--help` para exibir informações de uso e opções disponíveis.
    
## Como abrir um arquivo XDELTA

Os arquivos XDELTA não se destinam à abertura direta. Se desejar aplicar um patch XDELTA a um jogo ou outro arquivo, você tem a opção de usar o xdelta, que é compatível com várias plataformas, ou a interface do usuário xdelta, projetada especificamente para usuários do Windows.

## Referências
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


