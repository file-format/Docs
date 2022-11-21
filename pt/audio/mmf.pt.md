{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "arquivo", "extensão", "formato", "áudio", "smaf", "extensão mmf", "arquivos mmf", "arquivo de música móvel", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo MMF e APIs que podem criar e abrir arquivos MMF.",
  "title" :"MMF - Formato de arquivo de música móvel",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## O que é um arquivo MMF?

MMF é uma extensão de arquivo associada a um arquivo SMAF. O MMF significa Arquivo de Música Móvel, enquanto o SMAF significa Formato de Aplicativo Móvel de Música Sintética. Os arquivos MMF dentro de um smartphone contêm toques do sistema, som e também podem conter gráficos e exibição de texto. O MMF contém ainda três tipos de parâmetros de instrumento, incluindo FM, PCM e Stream PCM. Esses formatos de arquivo são compatíveis com a plataforma do sistema Windows. Os arquivos MMF são categorizados como arquivos de dados. Normalmente, o Microsoft Mail oferece suporte a arquivos MMF. O arquivo com o sufixo MMF pode ser copiado para qualquer dispositivo móvel ou plataforma do sistema.

Além disso, esses arquivos são muito menores em tamanho em comparação com os arquivos de formato MIDI padrão. Os arquivos [WAV](/pt/audio/wav/) e [MID](/pt/audio/mid/) podem ser convertidos para o formato MMF que pode ser compartilhado e distribuído como conteúdo de áudio. Esses arquivos podem ser recebidos via e-mail diretamente para telefones e PC.


## Breve História do Formato de Arquivo MMF

A Yamaha desenvolveu ferramentas SMAF como arquivos de som para que os smartphones possam armazenar um número maior de toques exclusivos. A Yamaha introduziu o SMAF com a produção de seus chips de som MA-1, MA-2, MA-3, MA-5 e MA-7 LSI. Todos esses formatos se tornaram bastante familiares entre os telefones celulares no mercado do Leste Asiático no início de 2000.

A nível internacional, o formato MMF foi autorizado pela Samsung. Com a ajuda do formato MMF, a Samsung conseguiu projetar uma ampla gama de toques polifônicos para serem usados em smartphones Samsung.

A Yamaha queria tornar o formato ainda mais popular e assim nos arquivos oficiais Yamaha SMAF, publicou mais ferramentas compatíveis com este formato. Com isso, os usuários agora podem reproduzir facilmente arquivos MMF em seus computadores.


## Especificações de formato de arquivo MMF ##

Os arquivos MMF são categorizados em seções de dados. Uma estrutura prefixada em torno de 8 bytes é usada para descrever cada segmento.
O rótulo de 4 bytes inclui CNTI, OPDA, MSTR, MTR e ATR. O tamanho dos dados mais 8 bytes é o tamanho do bloco; o tamanho total do arquivo é calculado pela soma de todos os tamanhos dos blocos. Se um arquivo não foi danificado, o tamanho do arquivo somado deve ser igual ao tamanho do cabeçalho principal.

### Cabeçalho ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Aqui está um exemplo de arquivo MMF:

![](../mmf.png)

## Referências

* [MMF - Por Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

