{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PDF/X",
  "description":"Saiba mais sobre o formato de arquivo PDF/X e APIs que podem criar e abrir arquivos PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# O que é arquivo PDF/X? #

PDF/X é um padrão ISO 15930 publicado em 2001 com um subconjunto de funcionalidades de PDF. O padrão foi estabelecido e publicado com base em requisitos específicos das indústrias de impressão e publicação. Os requisitos para este padrão foram todos concebidos de acordo com as diversas necessidades das indústrias de impressão e publicação. O PDF/X requer que os arquivos em conformidade sejam completos, ou seja, independentes. Isso requer que elementos como fontes usadas na página façam parte do documento. Conteúdos como 3D ou vídeo não podem fazer parte de um documento PDF/X. As informações contidas no documento PDF/X exigem que sejam precisas.

## Padrões e Revisões PDF/X ##

A família de padrões PDF/X é composta por várias versões, cada uma projetada para um resultado especializado. O desenvolvimento desses padrões visava atender às diversas necessidades das indústrias de impressão e publicação.

* `PDF/X-1a` - Também conhecido como o primeiro padrão da família PDF/X, o PDF/X-1a requer que todo o conteúdo faça parte do documento PDF para poder ser impresso. Elementos de documentos como fontes, formulários, proteção por senha e anotações visíveis não são permitidos. O PDF/X-1a tem seus próprios requisitos específicos, bem como aqueles relativos à transparência e camadas são permitidas. Isso também exige que os elementos de impressão usem apenas cores CMYK, escala de cinza ou cores exatas, resultando no não uso de RGB ou espaços de cores independentes de dispositivo. é para trocas nas quais todos os arquivos devem ser entregues em CMYK (e/ou cores exatas), sem dados RGB ou gerenciados por cores. PDF/X-1a também é referido como Troca Completa devido à integridade das informações exigidas pelo
* `PDF/X-3` - foi introduzido em 2002 e eliminou muitas restrições do PDF/X-1a. Isso permitiu que os gráficos em um PDF/X-3 usassem espaços de cores baseados em CMYK, grescale, RGB, Lab e ICC. Na verdade, é baseado nos padrões PDF 1.3 com [perfil ICC](https://en.wikipedia.org/wiki/ICC_Profile). Também é conhecido como Gerenciamento de Cores devido à flexibilidade e às regras que introduz em relação às cores incluídas em um documento PDF.
* `PDF/X-4` - suporta transparências, então o PDF-X/4 contém todos os dados necessários para saída sem achatamento.
* `PDF/X-5` - é baseado em PDF/X-4, adicionando suporte para gráficos externos por meio de XObjects de referência, bem como perfis n-colorantes externos para intenção de renderização. Use-o para troca parcial de dados de impressão usando PDF versão 1.6

## Referências ##

* [PDF/X - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

