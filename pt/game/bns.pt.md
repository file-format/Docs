{
  "date" : "2021-10-20",
  "keywords" :[ "arquivo bns", "formato de arquivo bns", "o que é um arquivo bns", "arquivo", "exemplo bns", "extensão de arquivo do Portal Bonus Map Script","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo BNS do Bonus Map Script e APIs que podem criar e abrir arquivos BNS.",
  "title" :"BNS - Arquivo de script de mapa de bônus do portal",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## O que é um arquivo BNS?

Um arquivo com extensão .bns é um arquivo de script de jogo criado com o jogo de resolução de quebra-cabeça Portal Map, desenvolvido pela Valve. Ele contém script de texto para definir informações sobre um mapa do Portal que é armazenado como arquivo .bsp. Os arquivos BNS são usados como referência a esse arquivo de mapa real e contêm uma lista de desafios que devem ser concluídos. Além disso, contém o nome do mapa, comentários sobre o mapa e referências de arquivo de imagem em miniatura. Um arquivo BNS pode ser aberto em qualquer editor de texto, como Notepad++, textEdit e Notepad.

## Formato de arquivo BNS

Os arquivos BNS são salvos como arquivos de texto simples que podem ser lidos por humanos. Estes podem ser abertos em editores de texto e editados também. No entanto, eles devem ser cuidadosamente editados para evitar erros no script.

## Exemplo de formato de arquivo BNS

Um arquivo BNS pode se parecer com o seguinte quando é aberto em um editor de texto como o Notepad++.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## Partes de um arquivo BNS

No exemplo acima,

* `#Bonus_Map_Challenges` - Representa o nome do mapa.
* `map` - Representa o nome do mapa a ser colocado na pasta de mapas do jogo
* `chapter` - Representa o capítulo ao qual o mapa pertence. Todos os arquivos de capítulos estão localizados no arquivo VPK adicionando o nome do mapa no formato `map your_map_name`
* `Image` - Contém a miniatura do mapa e é armazenado no caminho raiz steam\steamapps\common\portal\portal\materials\VGUI.
* `Comentário` - Texto descritivo sobre o mapa criado.

## Referências

* [Script de desafio do portal](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

