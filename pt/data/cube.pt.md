{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo CUBE - Arquivo Cubo Gaussiano - O que é arquivo .cube e como abri-lo?",
  "description" : "Aprenda sobre o Arquivo Cubo Gaussiano e como abri-lo.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-pt-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## O que é um arquivo CUBE?

O formato de arquivo CUBE, também conhecido como arquivo Cubo Gaussiano (.cube) é usado em química computacional para armazenar dados moleculares, particularmente informações de densidade eletrônica resultantes de cálculos de química quântica. Este formato é comumente associado ao **pacote de software gaussiano**, que é amplamente utilizado para realizar cálculos de estrutura eletrônica ab initio.

Os arquivos do Cubo Gaussiano armazenam dados tridimensionais, normalmente representando a densidade eletrônica ou outras propriedades das moléculas, obtidos por meio de cálculos de química quântica. O arquivo contém seção de cabeçalho com metadados (como origem, número de pontos de dados ao longo de cada eixo e espaçamento), seguido por uma grade de valores numéricos que representam propriedades de interesse (por exemplo, densidade eletrônica) em cada ponto da grade no espaço.

O arquivo Gaussian Cube (.cube) é um arquivo de texto simples com estrutura específica. O cabeçalho contém informações sobre o sistema molecular e a grade de dados, e os valores dos dados são organizados em formato de grade tridimensional. Arquivos Gaussian Cube são frequentemente usados para visualizar propriedades moleculares usando software de visualização molecular. Programas como **VMD (Visual Molecular Dynamics)** ou **PyMOL** podem ler arquivos de Cubo Gaussiano para exibir superfícies moleculares, densidade de elétrons ou outras propriedades calculadas.

## Exemplo simplificado de arquivo Cubo Gaussiano:

```
Exemplo de arquivo cúbico
Gerado por Gaussiano
   0 1 0 0 0 0 0 0 0 0
   0,000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,100000000000000E+01 0,000000000000000E+00 0,0000000000000000E+00
  50 0,000000000000000E+00 0,100000000000000E+01 0,0000000000000000E+00
  50 0,000000000000000E+00 0,000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (valores de dados para densidade eletrônica em cada ponto da grade)
```

## Sobre Gaussiano

Gaussian é um conjunto de aplicativos de software para química quântica e química computacional. O foco principal do Gaussiano está nos métodos de química quântica ab initio, que são abordagens altamente precisas, mas computacionalmente intensivas, para estudar a estrutura eletrônica das moléculas. O software é amplamente utilizado em pesquisas e ambientes acadêmicos para diversas aplicações, incluindo previsão de propriedades moleculares, estudo de mecanismos de reação e exploração de estruturas moleculares.

## Sobre NWChem

NWChem é um software de química computacional de código aberto projetado para simulações de química quântica de alto desempenho. Ele emprega métodos ab initio, como Hartree-Fock e teoria do funcional de densidade, suporta computação paralela para cálculos eficientes em clusters e encontra aplicações em diversos campos científicos, incluindo química computacional, bioquímica e ciência de materiais. NWChem é conhecido por sua versatilidade, permitindo aos pesquisadores estudar vários sistemas químicos, e sua natureza de código aberto incentiva contribuições e customização da comunidade.

## Sobre o VMD

VMD, que significa Visual Molecular Dynamics, é um programa de visualização molecular poderoso e amplamente utilizado para exibir, analisar e animar trajetórias de dinâmica molecular (MD), bem como estruturas moleculares estáticas. É particularmente popular nas áreas de química computacional, biologia molecular e bioinformática estrutural. O VMD é excelente na visualização de estruturas moleculares, fornecendo renderizações 3D de moléculas e complexos moleculares de alta qualidade. Ele suporta vários formatos de arquivo molecular.

## Sobre PyMOL

PyMOL é um sistema de visualização molecular e ferramenta de software usado para visualização tridimensional de estruturas moleculares. É particularmente popular nas áreas de biologia estrutural, bioinformática e química computacional. PyMOL fornece renderizações 3D de estruturas moleculares de alta qualidade, permitindo aos usuários visualizar e explorar formas, superfícies e interações de macromoléculas biológicas.

## Como abrir o arquivo CUBE?

O arquivo CUBE pode ser aberto e referenciado usando os seguintes programas.

- **NWChem** (gratuito) para (Windows, MAC, Linux)

## Referências
* [Formato de arquivo do cubo gaussiano](https://paulbourke.net/dataformats/cube/)
