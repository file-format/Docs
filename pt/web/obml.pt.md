{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo OBML - Arquivo de página da Web salvo do Opera Mini",
  "description" :"Saiba mais sobre o que é um arquivo OBML e APIs que podem criar e abrir um arquivo OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## O que é um arquivo OBML?

Um arquivo OBML (Opera Binary Markup Language) é uma versão offline de uma página da Web salva pelo navegador móvel Opera Mini. É uma versão compacta e independente dos arquivos [HTML](/pt/web/html/) que contém todos os elementos da página para exibição em dispositivos específicos enquanto estiver offline. O formato de arquivo OBML foi atualizado para várias versões com OBML15 e OBML16 sendo usados em geral. Um ponto importante a ser considerado é que cada versão do Opera Mini é compatível apenas com um formato OBML. Assim, a atualização do Opera Mini deixará as páginas salvas anteriormente legíveis. Os arquivos OBML podem ser convertidos em HTML e [PDF](/pt/pdf/).

## Formato de arquivo OBML

O formato de arquivo OBML é salvo no formato de arquivo proprietário do Opera e suas especificações de formato de arquivo não estão disponíveis publicamente. No entanto, o [formato OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) foi submetido a engenharia reversa para decodificar sua estrutura da seguinte forma.

### Tipos de dados OBML

De acordo com os resultados da engenharia reversa, o OBML usa os seguintes tipos primitivos:

* `byte` – inteiro sem sinal (1 byte)
* `short` – inteiro assinado (2 bytes, big-endian)
* `medium` – inteiro assinado (3 bytes, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – um byte contendo um caractere ASCII
* `string` – um blob contendo texto codificado em UTF-8

### Cabeçalho OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Referências

* [formato OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

