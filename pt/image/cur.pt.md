{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extensão", "arquivo", "formato", "imagem", "Bitmap independente do dispositivo", "Formato de arquivo do cursor", "Cursor", "Windows", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Formato de arquivo do cursor",
  "description":"Saiba mais sobre o formato de arquivo CUR e APIs que podem criar e abrir arquivos CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo CUR? ##

Um arquivo CUR é um formato de arquivo de cursor estático do Microsoft Windows. Basicamente, são imagens estacionárias idênticas aos arquivos ICO (ícone) em todos os sentidos, exceto na extensão. Ambos CUR e [ICO](/pt/image/ico/) são estabelecidos com base na especificação Device-Independent Bitmap [DIB](/pt/image/dib/) (Device-Independent Bitmap). O padrão, bem como o cursor personalizado, como o ponteiro do mouse do Windows para o sistema operacional Windows, são armazenados em arquivos CUR. Pode ser uma seta para uso normal, uma ampulheta giratória para demonstrar os períodos de espera ou uma barra I para edição de texto. Os arquivos CUR vêm junto com o pacote de instalação dos temas personalizados da área de trabalho para garantir que o cursor do Windows corresponda ao tema personalizado da área de trabalho.

## Especificação técnica ##

Os arquivos CUR são arquivos de sistema binários que podem ser encontrados em dispositivos que funcionam no sistema operacional Microsoft Windows. As imagens de ponteiro CUR vêm em diferentes tamanhos padrão, como 16×16, 32×32, etc. Os arquivos CUR são muito semelhantes aos arquivos ICO; ambos consistem em pequenas imagens estacionárias. Apenas a extensão dos arquivos CUR e ICO são diferentes. Além disso, a explicação de um hotspot no cabeçalho do arquivo CUR é diferente do arquivo ICO. O ponto de acesso interpreta o deslocamento de pixel do canto superior esquerdo até o local onde você está apontando o mouse. Os sistemas Windows ainda estão usando os arquivos CUR, mas agora os cursores animados geralmente têm a extensão de arquivo ANI em vez de CUR.

## Breve história ##

O arquivo CUR é feito a partir do arquivo ICO. O primeiro formato de arquivo CUR foi incorporado ao sistema operacional Windows 1.0 da Microsoft em 1981 para facilitar o uso comercial. Logo mais cursores interativos foram introduzidos, permitindo que os usuários alterassem suas preferências de cursor a partir das opções pré-instaladas disponíveis. No entanto, é fácil editar um arquivo CUR por conta própria, mesmo que você tenha conhecimento técnico insuficiente.


## Exemplo CUR ##

Os arquivos CUR podem ser encontrados em *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Formato de arquivo CUR" >}}

