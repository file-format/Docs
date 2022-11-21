{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo fnt", "formato de arquivo fnt", "o que é um arquivo fnt", "arquivo", "exemplo de fnt", "extensão de arquivo fnt", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Arquivo de fontes do Windows",
  "description":"Saiba mais sobre o formato de arquivo FNT e APIs que podem criar e abrir arquivos FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## O que é um arquivo FNT?

Um arquivo com extensão .fnt é um arquivo de fonte que armazena informações genéricas sobre fontes em sistemas operacionais Windows. Os arquivos FNT foram substituídos principalmente pelos formatos de arquivo TrueType (.TTF) e OpenType (.OTF), e é um formato de arquivo de fonte obsoleto a partir de agora. Esses arquivos podem armazenar um único avaliador ou fonte vetorial. Todos os drivers de dispositivo suportam as fontes do Windows 2.x. No entanto, nem todos os drivers de dispositivo
suporte a versão do Windows 3.0.

## Formato de arquivo FNT

Os arquivos FNT são capazes de armazenar uma única fonte raster ou vetorial. Os formatos vetoriais são usados com mais frequência pelo GDI em comparação com o raster onde o glifo de cada carta é definido usando um pequeno bitmap. A razão óbvia para a substituição de .fnt por .ttf e .otf é seu formato raster.

### Cabeçalho do arquivo de fonte
O início dos arquivos de fonte raster e vetorial é comum, seguido por informações diferentes para cada tipo de arquivo. O cabeçalho do arquivo de fonte inclui para Windows 3.0 inclui seis novos campos, conforme a seguir, que são definidos como zero para garantir a compatibilidade com versões futuras do Windows.

* dFlags
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReservado1

Para obter informações detalhadas sobre os cabeçalhos para Windows 3.0 e 2.0, visite o [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referências
* [Formato de arquivo de fonte](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Como instalar ou remover uma fonte no Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

