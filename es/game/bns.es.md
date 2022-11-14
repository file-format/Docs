{
  "date" : "2021-10-20",
  "keywords" :[ "archivo bns", "formato de archivo bns", "qué es un archivo bns", "archivo", "ejemplo de bns", "extensión de archivo de script de mapas de bonificación del portal", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo BNS de Bonus Map Script ortal y las API que pueden crear y abrir archivos BNS",
  "title" :"BNS - Archivo de secuencia de comandos del mapa de bonificación del portal",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## ¿Qué es un archivo BNS?

Un archivo con extensión .bns es un archivo de script de juego creado con el juego de resolución de rompecabezas Portal Map desarrollado por Valve. Contiene secuencias de comandos de texto para definir información sobre un mapa del Portal que se almacena como archivo .bsp. Los archivos BNS se utilizan como referencia a este archivo de mapa real y contienen una lista de desafíos que deben completarse. Además, contiene el nombre del mapa, comentarios sobre el mapa y referencias de archivos de imágenes en miniatura. Un archivo BNS se puede abrir en cualquier editor de texto, como Notepad ++, textEdit y Notepad.

## Formato de archivo BNS

Los archivos BNS se guardan como archivos de texto sin formato que son legibles por humanos. Estos pueden abrirse en editores de texto y editarse también. Sin embargo, estos deben editarse cuidadosamente para evitar errores en el script.

## Ejemplo de formato de archivo BNS

Un archivo BNS puede tener un aspecto similar al siguiente cuando se abre en un editor de texto como Notepad++.

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

## Partes de un archivo BNS

En el ejemplo anterior,

* `#Bonus_Map_Challenges` - Representa el nombre del mapa.
* `mapa`: representa el nombre del mapa que se colocará en la carpeta de mapas del juego
* `chapter` - Representa el capítulo al que pertenece el mapa. Todos los archivos de capítulos se ubican en el archivo VPK agregando el nombre del mapa en el formato `map your_map_name`
* `Imagen`: contiene la miniatura del mapa y se almacena en la ruta raíz steam\steamapps\common\portal\portal\materials\VGUI.
* `Comentario` - Texto descriptivo sobre el mapa creado.

## Referencias

* [Guión del desafío del portal](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

