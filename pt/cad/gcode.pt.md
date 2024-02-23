{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Arquivo GCODE - O que é um arquivo .gcode e como abri-lo?",
   "description":"Aprenda sobre o formato de arquivo GCODE e APIs que podem criar e abrir arquivos GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-pt",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## O que é um arquivo .GCODE?

Um **arquivo GCODE** é um arquivo de texto simples que contém instruções para controlar máquinas-ferramentas computadorizadas e impressoras 3D; O código G, ou Código Geométrico, é uma linguagem usada para controlar movimentos e ações de máquinas **CNC (Controle Numérico Computadorizado)**; As máquinas CNC incluem fresadoras, tornos, roteadores e impressoras 3D.

Os comandos do código G são escritos em uma sintaxe específica que normalmente consiste em letras e números; cada comando instrui a máquina a executar ações específicas, como mover a ferramenta para uma posição específica, trocar a ferramenta ou ajustar a velocidade.

O código G é frequentemente gerado por software **CAM (Computer-Aided Manufacturing)**; O software CAM pega um modelo 3D ou projeto 2D e gera caminhos de ferramenta correspondentes e instruções de código G; o arquivo de código G é então carregado em uma máquina CNC ou impressora 3D para execução.

Os arquivos de código G normalmente têm extensão de arquivo .nc” ou .gcode”, por exemplo, program.nc” ou print.gcode”.

## Estrutura do arquivo GCODE:

Os arquivos GCODE são arquivos de texto simples com cada linha contendo um comando específico; esses comandos vão desde o controle do movimento da máquina até o ajuste da temperatura, velocidade e outros parâmetros cruciais para a fabricação de um objeto.

A sintaxe do GCODE envolve combinação de letras e números; cada um representando ação ou parâmetro distinto; comandos comuns incluem G0 e G1 para movimento, M3 e M5 para controle do fuso e S e F para ajustes de velocidade e taxa de avanço, respectivamente.

## Geração GCODE:

Softwares de fatiamento, como **Simplify3D** e **Slic3r**, traduzem desenhos de design auxiliado por computador (CAD) em GCODE; O software CAD é usado para criar modelos 3D, que são exportados em formatos como STL; o software de fatiamento pega esses modelos e gera um arquivo GCODE especificando detalhes como altura da camada, velocidade de impressão e configurações de temperatura.

## Exemplo de GCODE

Aqui está um exemplo simples de código G para mover uma máquina CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Como abrir o arquivo GCODE?

Para abrir um arquivo de código G você pode usar diferentes tipos de software dependendo de suas necessidades.

Se você gerou código G para impressora 3D; você pode abri-lo usando o software que acompanha sua impressora 3D ou um software de fatiamento dedicado; exemplos incluem **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** ou **Repetier-Host**; esses programas geralmente possuem uma interface amigável que permite carregar e visualizar o código G.

Os arquivos GCODE são de texto simples, então você pode abri-los com qualquer editor de texto; editores de texto comuns incluem **Notepad (no Windows)**, **TextEdit (no macOS)** ou **Gedit (no Linux)**; simplesmente **clique com o botão direito** no arquivo de código G, escolha **Abrir com** e selecione um editor de texto.

