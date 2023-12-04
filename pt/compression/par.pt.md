{
"data":"18/07/2023",
   "keywords":[
"PAR",
"Arquivo PAR",
"como abrir um arquivo par",
"arquivo",
"Extensão de arquivo PAR",
"extensão",
"arquivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"Formato de arquivo PAR - Arquivo de índice Parchive",
   "description":"Aprenda sobre o formato PAR e APIs que podem criar e abrir arquivos PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent" : "compression"
}
},
"último mod":"18/07/2023"
}

## O que é um arquivo .PAR?

Nos arquivos Parchive (PAR), um arquivo .par refere-se a um arquivo de índice que contém um grupo de volumes de paridade ou blocos de paridade. Este arquivo de índice é usado para fins de detecção e recuperação de erros quando um ou mais arquivos no arquivo são perdidos ou danificados.

Um arquivo Parchive normalmente consiste nos arquivos de dados originais e nos volumes de paridade correspondentes. Os volumes de paridade são criados usando algoritmos de correção de erros Reed-Solomon. Esses volumes de paridade contêm informações redundantes que podem ser usadas para recuperar os arquivos de dados originais.

O arquivo .par, também conhecido como conjunto de volumes de paridade, contém informações sobre a estrutura e localização dos volumes de paridade no arquivo. Serve como índice ou mapa para o processo de recuperação. Ao usar o arquivo .par, o software PAR especializado pode determinar quais volumes de paridade são necessários e como eles devem ser usados para reconstruir os arquivos ausentes ou danificados.

Quando um ou mais arquivos no arquivo Parchive ficam inacessíveis ou corrompidos, o arquivo .par pode ser utilizado em conjunto com os volumes de paridade disponíveis para recuperar os dados perdidos. O software PAR lê o arquivo .par, identifica os arquivos ausentes ou danificados e usa os volumes de paridade para reconstruí-los.

## Como abrir o arquivo PAR?

Para abrir e usar arquivos .par, você precisará de um software PAR especializado. Aqui estão algumas opções de software populares que podem lidar com arquivos .par:

- **QuickPar:** QuickPar é um software PAR amplamente utilizado para Windows. Ele permite criar, verificar e reparar arquivos PAR. Você pode abrir um arquivo .par no QuickPar para verificar sua integridade ou usá-lo para reparar arquivos danificados ou ausentes em um arquivo Parchive.

- **MultiPar:** MultiPar é outro software PAR popular disponível para Windows. Ele suporta os formatos de arquivo PAR e PAR2 e fornece recursos avançados para criar, verificar e reparar arquivos. MultiPar pode abrir arquivos .par e realizar operações de detecção e recuperação de erros com base nos volumes de paridade fornecidos.

- **MacPAR deLuxe:** MacPAR deLuxe é um software PAR projetado especificamente para macOS. Ele suporta formatos de arquivo PAR e PAR2 e fornece funcionalidade semelhante ao QuickPar e MultiPar. MacPAR deLuxe pode abrir arquivos .par e ajudar na verificação de arquivos e na recuperação de arquivos danificados ou ausentes.

## Formato de arquivo PAR - Mais informações

O formato de arquivo PAR, comumente referido como Parchive, é um formato de arquivo específico usado para criar dados de paridade e realizar detecção e recuperação de erros em arquivos compactados. O formato de arquivo PAR normalmente consiste em três tipos: PAR, PAR2 e PAR3.

- **PAR:** O formato de arquivo PAR original, também conhecido como PAR1, foi desenvolvido pelo projeto Parchive. Inclui dados de paridade gerados a partir dos arquivos de dados originais. Os arquivos PAR fornecem um nível básico de detecção e recuperação de erros, mas têm limitações em termos de recursos de correção de erros.

- **PAR2:** PAR2 é uma versão melhorada do formato de arquivo PAR. Ele oferece recursos de correção de erros mais avançados e recursos de recuperação aprimorados. Os arquivos PAR2 são normalmente usados para criar dados de paridade que podem recuperar arquivos perdidos ou danificados dentro de um arquivo. Os arquivos PAR2 fornecem melhor proteção contra corrupção de dados e são amplamente utilizados para fins de arquivamento de arquivos.

- **PAR3:** PAR3 é a versão mais recente do formato de arquivo PAR e oferece melhorias adicionais na correção e recuperação de erros. Ele oferece níveis ainda mais altos de redundância e recursos de correção de erros em comparação com PAR2. Os arquivos PAR3 são projetados para fornecer opções mais robustas de proteção e recuperação para dados armazenados em arquivos.

Os formatos de arquivo PAR2 e PAR3 são amplamente suportados pelo software PAR e oferecem a capacidade de verificar a integridade dos arquivos dentro de um arquivo e recuperar dados perdidos ou danificados. Os arquivos PAR e PAR2 ainda são comumente usados, enquanto os arquivos PAR3 estão gradualmente ganhando adoção devido aos seus recursos aprimorados de correção de erros.

## Referências
* [Parquivo](https://en.wikipedia.org/wiki/Parchive)

