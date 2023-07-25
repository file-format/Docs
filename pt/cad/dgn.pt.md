{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Arquivo", "Formato", "Abrir", "Ler", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Formato de arquivo de design MicroStation CAD",
  "description" :"Saiba mais sobre o formato de arquivo DGN e APIs que podem criar e abrir arquivos DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## O que é um arquivo DGN?

Um arquivo com extensão .dgn (Design) é um arquivo de desenho criado e suportado por aplicativos CAD, como MicroStation e Intergraph Interactive Graphics Design System. Ele é usado para criar e salvar projetos para projetos de construção, como rodovias, pontes e edifícios. O formato é semelhante ao formato de arquivo [DWG](/pt/cad/dwg/) da Autodesk e é considerado seu concorrente. Os arquivos DNG podem ser salvos como Intergraph Standard File Format ou V8 DGN. DGN pode ser convertido para vários outros formatos, como DWG, [BMP](/pt/image/bmp/), [JPEG](/pt/image/jpeg/), [PDF](/pt/pdf/), [GIF](/pt/image/ gif/) e outros. Ele pode ser aberto com Autodesk AutoCAD, Bentley View e Bentley Systems MicroStation, além de outros aplicativos de software, como as versões Corel PaintShop Photo Pro e IMSI TurboCAD Deluxe.

## Formato de arquivo V8 DGN

Um arquivo MicroStation V8 DGN é composto por um ou mais modelos. Um modelo é um contêiner para elementos. O V8 DGN remove todas as restrições baseadas em formato de arquivo que estavam presentes nas versões anteriores do MicroStation. A seguir está uma lista de melhorias no formato de arquivo DGN.

* O limite no número de níveis em um arquivo DGN foi removido e cada nível é nomeado e armazenado como um elemento.
* O tamanho físico máximo do arquivo DGN não tem nenhuma limitação e é limitado apenas pelo sistema operacional (como o limite do NT é 4 GB)
* O tamanho máximo de um único elemento é 128 KB.
* Não há limite para o tamanho máximo de uma célula.
* Os nomes das células estão limitados a aproximadamente 500 caracteres.
* Não há limite para o número de referências que podem ser anexadas a um arquivo DGN.
* Uma linha, forma ou curva de ponto pode ter até 5.000 vértices.
* Não há limite para o número de componentes em uma cadeia complexa ou forma complexa.
* Não há limite para o número de grupos gráficos em um arquivo DGN.
* A cerca é paralela à vista em que está colocada.
* Uma única linha de texto pode conter 65.535 caracteres.
* Não há limite para o tamanho máximo de um nó de texto.
* Não há limite para o número de nós de texto em um arquivo DGN.
* Cada elemento tem um identificador exclusivo de 64 bits que não muda durante o ciclo de vida do elemento.
* Cada elemento tem um carimbo de hora que indica a hora da alteração mais recente.

## Referências

* [DNG - Por Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [Formato de arquivo DGN MicroStation V8](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

